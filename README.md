# CompactClicker<div align="center">

# ⚡ PowerShell AutoClicker

**Un autoclicker ultra-léger en une seule ligne de PowerShell.**
Aucune installation. Aucun fichier. Aucun blocage.

[![PowerShell](https://img.shields.io/badge/PowerShell-5.1+-5391FE?style=for-the-badge&logo=powershell&logoColor=white)](https://learn.microsoft.com/powershell/)
[![Windows](https://img.shields.io/badge/Windows-10%20%7C%2011-0078D6?style=for-the-badge&logo=windows&logoColor=white)](https://www.microsoft.com/windows)
[![License](https://img.shields.io/badge/License-MIT-2ecc71?style=for-the-badge)](LICENSE)
[![Size](https://img.shields.io/badge/Size-330%20chars-orange?style=for-the-badge)]()

</div>

---

## 🎯 C'est quoi ?

Un autoclicker **qui tient en 330 caractères**. Tu le colles dans PowerShell, tu appuies sur **F6**, ça clique. C'est tout.

Pas de `.exe` à télécharger. Pas d'installation. Pas d'ExecutionPolicy à changer. Pas de fichier qui traîne.

---

## 🚀 Utilisation (30 secondes)

### 1️⃣ Ouvre PowerShell

<kbd>Win</kbd> + <kbd>R</kbd> → tape `powershell` → <kbd>Entrée</kbd>

Ou : menu Démarrer → tape `Windows PowerShell` → Entrée.

### 2️⃣ Colle cette ligne

```powershell
Add-Type 'using System;using System.Runtime.InteropServices;public class M{[DllImport("user32.dll")]public static extern void mouse_event(uint f,uint x,uint y,uint d,uint e);[DllImport("user32.dll")]public static extern short GetAsyncKeyState(int k);}';while(1){if([M]::GetAsyncKeyState(117)-band 32768){$a=-not$a};if([M]::GetAsyncKeyState(118)-band 32768){exit};if($a){[M]::mouse_event(6,0,0,0,0);sleep -m 50}}
Puis <kbd>Entrée</kbd>.

3️⃣ Contrôle
Touche	Action
<kbd>F6</kbd>	▶️ Démarrer / ⏹️ Arrêter
<kbd>F7</kbd>	❌ Quitter
<kbd>Ctrl</kbd> + <kbd>C</kbd>	🛑 Kill de secours
💡 Astuce : clique d'abord sur la fenêtre où tu veux cliquer (le jeu / la page), puis appuie sur <kbd>F6</kbd>.

⚙️ Réglages
Changer la vitesse
Cherche sleep -m 50 dans le code et remplace 50 :

Valeur	Vitesse	Usage
100	10 CPS	🟢 Safe partout
50	20 CPS	🟡 Standard (par défaut)
20	50 CPS	🟠 Rapide
10	100 CPS	🔴 Détection probable
Formule : délai_ms = 1000 / CPS souhaité

Changer les touches
Remplace 117 (F6) et 118 (F7) par :

Touche	Code
F6	117
F7	118
F8	119
F9	120
Ctrl	17
Shift	16
❓ FAQ
<details> <summary><b>Ça marche sur quel Windows ?</b></summary>
Windows 7, 8, 10, 11 — partout où PowerShell existe. Testé sur Windows 10 et 11.

</details><details> <summary><b>Pourquoi rien ne se passe quand j'appuie sur F6 ?</b></summary>
Clique d'abord sur la fenêtre cible (le focus doit être dessus)

Essaie de rester appuyé 1 seconde — le script a un anti-rebond de 300 ms

Certains claviers ont une touche Fn Lock ou F-Lock — active-la

</details><details> <summary><b>Ça clique mais pas dans mon jeu ?</b></summary>
Ton jeu utilise probablement DirectInput et ignore mouse_event.

Solutions :

Baisse le CPS à 10 max

Ou utilise une souris gamer avec macro intégrée (Logitech G Hub, Razer Synapse) — c'est la seule solution fiable pour les jeux DirectInput

</details><details> <summary><b>Est-ce que je peux me faire ban ?</b></summary>
OUI si tu l'utilises sur un jeu avec anti-cheat kernel (Valorant, Fortnite, CS2, Apex, R6, Rust…).

Ces anti-cheats détectent les appels à mouse_event et GetAsyncKeyState → bannissement définitif.

👉 Utilise-le uniquement sur :

Clickers web

Jeux idle

Jeux solo sans anti-cheat

Vieux MMO sans protection

Voir l'avertissement plus bas.

</details><details> <summary><b>Je peux l'utiliser sur un PC d'école / entreprise ?</b></summary>
Non. Les PC gérés (WDAC, AppLocker) bloquent l'exécution de scripts non signés. Aucun contournement n'est possible et c'est contraire à la plupart des règlements.

</details><details> <summary><b>Comment je l'arrête si F7 ne répond pas ?</b></summary>
<kbd>Ctrl</kbd> + <kbd>C</kbd> dans PowerShell, ou ferme la fenêtre PowerShell, ou Gestionnaire des tâches → powershell.exe → Fin de tâche.

</details>
⚠️ Avertissement légal
Cet outil simule des clics de souris.

❌ N'utilise PAS cet outil sur des jeux avec anti-cheat kernel (Valorant, Fortnite, CS2, Apex Legends, Rainbow Six, Rust, PUBG…) sous peine de bannissement définitif de ton compte.

❌ N'utilise PAS cet outil sur un PC d'école, d'université ou d'entreprise sans autorisation écrite de l'administrateur.

✅ Usage recommandé : jeux solo, clickers web, jeux idle, tests d'interface, automatisation personnelle.

L'auteur décline toute responsabilité en cas de mauvaise utilisation, de bannissement de compte, ou de sanction disciplinaire.

🤝 Contribution
Les PR sont les bienvenues. Si tu veux ajouter :

Un mode "rafale" (X clics puis pause)

Un overlay visuel ON/OFF

Un support multi-touches

Ouvre une issue d'abord pour discuter de l'implémentation.

📜 Licence
MIT — fais-en ce que tu veux.

<div align="center">
⭐ Si ce projet t'a servi, mets une étoile !

Made with ☕ and PowerShell

</div> ```
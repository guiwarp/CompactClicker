<div align="center">

# ⚡ PowerShell AutoClicker

**Un autoclicker ultra-léger en une seule ligne de PowerShell.**
Aucune installation. Aucun fichier. Aucun blocage.

![Windows](https://img.shields.io/badge/Windows-10_|_11-0078D6?style=for-the-badge&logo=windows&logoColor=white)
![PowerShell](https://img.shields.io/badge/PowerShell-5.1+-5391FE?style=for-the-badge&logo=powershell&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-2ecc71?style=for-the-badge)
![Size](https://img.shields.io/badge/Size-~380_chars-orange?style=for-the-badge)

</div>

---

## 🎯 C'est quoi ?

Un autoclicker **qui tient en une seule ligne**. Tu la colles dans PowerShell, tu appuies sur **F6**, ça clique. C'est tout.

Pas de `.exe` à télécharger. Pas d'installation. Pas d'ExecutionPolicy à changer. Pas de fichier qui traîne.

---

## 🚀 Utilisation (30 secondes)

### 1️⃣ Ouvre PowerShell

`Win + R` → tape `powershell` → `Entrée`

### 2️⃣ Colle cette ligne

```powershell
Add-Type 'using System;using System.Runtime.InteropServices;public class M{[DllImport("user32.dll")]public static extern void mouse_event(uint f,uint x,uint y,uint d,uint e);[DllImport("user32.dll")]public static extern short GetAsyncKeyState(int k);}';$a=$false;$l=0;while(1){$t=[Environment]::TickCount;if(([M]::GetAsyncKeyState(117)-band 32768)-and($t-$l-gt 300)){$a=-not$a;$l=$t;Write-Host $(if($a){"ON "}else{"OFF"}) -ForegroundColor $(if($a){"Green"}else{"Red"})};if([M]::GetAsyncKeyState(118)-band 32768){exit};if($a){[M]::mouse_event(6,0,0,0,0);Start-Sleep -Milliseconds 50}}
```

Puis `Entrée`.

### 3️⃣ Contrôle

| Touche | Action |
|:------:|:-------|
| `F6` | ▶️ Démarrer / ⏹️ Arrêter |
| `F7` | ❌ Quitter |
| `Ctrl + C` | 🛑 Kill de secours |

> 💡 **Astuce** : clique d'abord sur la fenêtre cible (le jeu, la page web), puis appuie sur `F6`.

---

## ⚙️ Réglages

### Changer la vitesse

Cherche `Start-Sleep -Milliseconds 50` dans le code et remplace `50` :

| Valeur | Vitesse | Usage |
|:------:|:-------:|:------|
| `100` | 10 CPS | 🟢 Safe partout |
| `50` | 20 CPS | 🟡 Standard (par défaut) |
| `20` | 50 CPS | 🟠 Rapide |
| `10` | 100 CPS | 🔴 Détection probable |

**Formule** : `délai_ms = 1000 / CPS souhaité`

### Changer les touches

Remplace `117` (F6) et `118` (F7) par :

| Touche | Code |
|:------:|:----:|
| F6 | `117` |
| F7 | `118` |
| F8 | `119` |
| F9 | `120` |
| Ctrl | `17` |
| Shift | `16` |

---

## ❓ FAQ

<details>
<summary><b>🖥️ Ça marche sur quel Windows ?</b></summary>

Windows 7, 8, 8.1, 10, 11 — partout où PowerShell existe. Testé sur Windows 10 et 11.
</details>

<details>
<summary><b>🤔 Rien ne se passe quand j'appuie sur F6</b></summary>

1. Clique d'abord **sur la fenêtre cible** — le focus doit être dessus
2. Reste appuyé **1 seconde** — anti-rebond de 300 ms intégré
3. Vérifie que **Fn Lock** / **F-Lock** est activé sur ton clavier
</details>

<details>
<summary><b>🎮 Ça clique mais pas dans mon jeu</b></summary>

Ton jeu utilise probablement **DirectInput** et ignore `mouse_event`.

**Solutions** :
- Baisse le CPS à **10 max**
- Ou utilise une **souris gamer avec macro intégrée** (Logitech G Hub, Razer Synapse) — seule solution fiable pour DirectInput
</details>

<details>
<summary><b>🚫 Est-ce que je peux me faire ban ?</b></summary>

**OUI** sur les jeux avec anti-cheat kernel :

> Valorant · Fortnite · CS2 · Apex · R6 · Rust · PUBG

Ces anti-cheats détectent `mouse_event` et `GetAsyncKeyState` → **ban définitif**.

**✅ Usage safe** : clickers web, jeux idle, jeux solo, vieux MMO.
</details>

<details>
<summary><b>🏫 Je peux l'utiliser à l'école / au travail ?</b></summary>

**Non.** Les PC gérés (WDAC, AppLocker) bloquent les scripts non signés. **Aucun contournement possible** et c'est contraire à la plupart des règlements.
</details>

<details>
<summary><b>🛑 Comment l'arrêter si F7 ne répond pas ?</b></summary>

`Ctrl + C` dans PowerShell, ou ferme la fenêtre, ou Gestionnaire des tâches → `powershell.exe` → Fin de tâche.
</details>

---

## ⚠️ Avertissement

> **Cet outil simule des clics de souris.**
>
> ❌ **N'utilise PAS** cet outil sur des jeux avec anti-cheat kernel (Valorant, Fortnite, CS2, Apex Legends, Rainbow Six, Rust, PUBG) sous peine de **bannissement définitif** de ton compte.
>
> ❌ **N'utilise PAS** cet outil sur un PC d'école, d'université ou d'entreprise sans autorisation écrite de l'administrateur.
>
> ✅ **Usage recommandé** : jeux solo, clickers web, jeux idle, tests d'interface, automatisation personnelle.
>
> L'auteur décline toute responsabilité en cas de mauvaise utilisation, de bannissement de compte, ou de sanction disciplinaire.

---

## 🤝 Contribution

Les PR sont les bienvenues. Idées d'amélioration :

- Mode rafale (X clics puis pause)
- Overlay visuel ON/OFF
- Support multi-touches configurable
- Mode "human-like" (délais aléatoires)

Ouvre une **issue** avant d'attaquer une grosse feature.

---

## 📜 Licence

[MIT](LICENSE) — fais-en ce que tu veux.

---

<div align="center">

**⭐ Si ce projet t'a servi, mets une étoile !**

`Made with ☕ and PowerShell`

</div>
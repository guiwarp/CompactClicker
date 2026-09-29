<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=6,11,20&height=200&section=header&text=CompactClicker&fontSize=75&fontAlignY=35&desc=by%20guiwarp&descAlignY=60&descSize=22&animation=fadeIn" width="100%"/>

<br>

<a href="#-démarrage-rapide">
  <img src="https://img.shields.io/badge/⚡_DÉMARRAGE-2ecc71?style=for-the-badge&labelColor=000000" alt="Démarrage">
</a>
<a href="#️-configuration">
  <img src="https://img.shields.io/badge/⚙️_CONFIG-3498db?style=for-the-badge&labelColor=000000" alt="Config">
</a>
<a href="#-avertissement">
  <img src="https://img.shields.io/badge/⚠️_WARNING-e74c3c?style=for-the-badge&labelColor=000000" alt="Warning">
</a>
<a href="LICENSE">
  <img src="https://img.shields.io/badge/📜_MIT-5865F2?style=for-the-badge&labelColor=000000" alt="License">
</a>

<br><br>

<img src="https://img.shields.io/badge/Windows-10_|_11-0078D6?style=flat-square&logo=windows&logoColor=white"/>
<img src="https://img.shields.io/badge/PowerShell-5.1+-5391FE?style=flat-square&logo=powershell&logoColor=white"/>
<img src="https://img.shields.io/badge/Taille-~380_caractères-orange?style=flat-square"/>
<img src="https://img.shields.io/badge/Dépendances-0-brightgreen?style=flat-square"/>
<img src="https://img.shields.io/badge/Installation-Aucune-success?style=flat-square"/>

<br>

<img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&size=18&duration=2500&pause=800&color=2ECC71&center=true&vCenter=true&width=520&lines=Une+seule+ligne.+Aucun+fichier.;Aucune+installation.+Aucun+blocage.;F6+%3D+Start.+F7+%3D+Quit." alt="Typing"/>

</div>

---

<div align="center">

```
╔═════════════════════════════════════════════════════════════════╗
║                                                                 ║
║    ██████╗ ██████╗ ███╗   ███╗██████╗  █████╗  ██████╗████████╗ ║
║   ██╔════╝██╔═══██╗████╗ ████║██╔══██╗██╔══██╗██╔════╝╚══██╔══╝ ║
║   ██║     ██║   ██║██╔████╔██║██████╔╝███████║██║        ██║    ║
║   ██║     ██║   ██║██║╚██╔╝██║██╔═══╝ ██╔══██║██║        ██║    ║
║   ╚██████╗╚██████╔╝██║ ╚═╝ ██║██║     ██║  ██║╚██████╗   ██║    ║
║    ╚═════╝ ╚═════╝ ╚═╝     ╚═╝╚═╝     ╚═╝  ╚═╝ ╚═════╝   ╚═╝    ║
║                                                                 ║
║   ██████╗██╗     ██╗ ██████╗██╗  ██╗███████╗██████╗              ║
║  ██╔════╝██║     ██║██╔════╝██║ ██╔╝██╔════╝██╔══██╗             ║
║  ██║     ██║     ██║██║     █████╔╝ █████╗  ██████╔╝             ║
║  ██║     ██║     ██║██║     ██╔═██╗ ██╔══╝  ██╔══██╗             ║
║  ╚██████╗███████╗██║╚██████╗██║  ██╗███████╗██║  ██║             ║
║   ╚═════╝╚══════╝╚═╝ ╚═════╝╚═╝  ╚═╝╚══════╝╚═╝  ╚═╝             ║
║                                                                 ║
║               >>  One line. Zero install. Pure power.  <<       ║
║                                                                 ║
║                        — by guiwarp —                           ║
║                                                                 ║
╚═════════════════════════════════════════════════════════════════╝
```

</div>

---

## 📖 Table des matières

<div align="center">

| | | |
|:-:|:-:|:-:|
| [⚡ Démarrage rapide](#-démarrage-rapide) | [🎮 Contrôles](#-contrôles) | [⚙️ Configuration](#️-configuration) |
| [❓ FAQ](#-faq) | [⚠️ Avertissement](#️-avertissement) | [📜 Licence](#-licence) |

</div>

---

<div align="center">

## ⚡ Démarrage rapide

</div>

<table>
<tr>
<td width="33%" align="center" valign="top">

### 1️⃣ Ouvrir

`Win` + `R`

tape

`powershell`

`Entrée`

</td>
<td width="33%" align="center" valign="top">

### 2️⃣ Coller

Copie la ligne ci-dessous

`Ctrl` + `V`

`Entrée`

</td>
<td width="33%" align="center" valign="top">

### 3️⃣ Lancer

`F6` ▶️

`F6` ⏹️

`F7` ❌

</td>
</tr>
</table>

<div align="center">

### 📋 La ligne magique

</div>

```powershell
Add-Type 'using System;using System.Runtime.InteropServices;public class M{[DllImport("user32.dll")]public static extern void mouse_event(uint f,uint x,uint y,uint d,uint e);[DllImport("user32.dll")]public static extern short GetAsyncKeyState(int k);}';$a=$false;$l=0;while(1){$t=[Environment]::TickCount;if(([M]::GetAsyncKeyState(117)-band 32768)-and($t-$l-gt 300)){$a=-not$a;$l=$t;Write-Host $(if($a){"ON "}else{"OFF"}) -ForegroundColor $(if($a){"Green"}else{"Red"})};if([M]::GetAsyncKeyState(118)-band 32768){exit};if($a){[M]::mouse_event(6,0,0,0,0);Start-Sleep -Milliseconds 50}}
```

<div align="center">

> 💡 **Astuce** — Clique d'abord sur la fenêtre cible, puis `F6`.
>
> 🎯 **Compatible** — Windows PowerShell 5.1 et PowerShell 7+

</div>

---

<div align="center">

## 🎮 Contrôles

</div>

<div align="center">

| `F6` | `F7` | `Ctrl + C` |
|:---:|:---:|:---:|
| ▶️ **Start / Stop** | ❌ **Quitter** | 🛑 **Kill de secours** |

</div>

---

<div align="center">

## ⚙️ Configuration

</div>

### 🚀 Vitesse — Cherche `Start-Sleep -Milliseconds 50`

```
                    LENT                                   RAPIDE
                      │                                       │
    ┌─────────────────┼───────────────────────────────────────┼─────┐
    │                 │                                       │     │
   100                50                                      20    10
    │                 │                                       │     │
  10 CPS           20 CPS                                  50 CPS  100 CPS
    │                 │                                       │     │
    🟢               🟡                                      🟠     🔴
  SAFE           STANDARD                                  RAPIDE  DANGER
```

**Formule** : `délai_ms = 1000 / CPS souhaité`

### ⌨️ Touches — Cherche `117` (F6) et `118` (F7)

<div align="center">

| Touche | Code | Touche | Code |
|:------:|:----:|:------:|:----:|
| `F6` | `117` | `F9` | `120` |
| `F7` | `118` | `Ctrl` | `17` |
| `F8` | `119` | `Shift` | `16` |

</div>

---

<div align="center">

## ❓ FAQ

</div>

<details>
<summary><b>🖥️ Ça marche sur quel Windows ?</b></summary>
<br>

Windows 7 · 8 · 8.1 · 10 · 11 — **partout où PowerShell existe**. Testé sur Windows 10 et 11.

</details>

<details>
<summary><b>🤔 Rien ne se passe quand j'appuie sur F6</b></summary>
<br>

1. **Clique sur la fenêtre cible** — le focus doit être dessus
2. Reste appuyé **1 seconde** — anti-rebond de 300 ms intégré
3. Vérifie que **Fn Lock** / **F-Lock** est activé sur ton clavier

</details>

<details>
<summary><b>🎮 Ça clique mais pas dans mon jeu</b></summary>
<br>

Ton jeu utilise **DirectInput** et ignore `mouse_event`.

**Solutions :**
- Baisse le CPS à **10 max**
- Ou passe à une **souris gamer** avec macro intégrée (Logitech G Hub, Razer Synapse) — seule solution fiable pour DirectInput

</details>

<details>
<summary><b>🚫 Est-ce que je peux me faire ban ?</b></summary>
<br>

**OUI** sur les jeux avec anti-cheat kernel :

> Valorant · Fortnite · CS2 · Apex · R6 · Rust · PUBG

Ces anti-cheats détectent `mouse_event` et `GetAsyncKeyState` → **ban définitif**.

**✅ Usage safe** : clickers web, jeux idle, jeux solo, vieux MMO.

</details>

<details>
<summary><b>🏫 Je peux l'utiliser à l'école / au travail ?</b></summary>
<br>

**Non.** Les PC gérés (WDAC, AppLocker) bloquent les scripts non signés. **Aucun contournement possible** et c'est contraire à la plupart des règlements.

</details>

<details>
<summary><b>🛑 Comment l'arrêter si F7 ne répond pas ?</b></summary>
<br>

1. `Ctrl` + `C` dans PowerShell
2. Ferme la fenêtre PowerShell
3. Gestionnaire des tâches → `powershell.exe` → **Fin de tâche**

</details>

---

<div align="center">

## ⚠️ Avertissement

</div>

<div align="center">

```
┌─────────────────────────────────────────────────────────────┐
│                                                             │
│   ⚠️  UTILISATION À TES RISQUES                             │
│                                                             │
│   Cet outil simule des clics de souris.                     │
│                                                             │
└─────────────────────────────────────────────────────────────┘
```

</div>

<table>
<tr>
<td width="50%" valign="top">

### ❌ À NE PAS FAIRE

- Utiliser sur un jeu avec **anti-cheat kernel**
  *→ ban définitif*
- Lancer sur un PC d'**école / entreprise**
  *→ violation du règlement*
- Vendre l'outil comme "indétectable"
  *→ mensonge*

</td>
<td width="50%" valign="top">

### ✅ USAGE RECOMMANDÉ

- Jeux **solo** sans anti-cheat
- **Clickers web** (Cookie Clicker…)
- **Jeux idle** (Clicker Heroes…)
- **Automatisation** personnelle
- **Tests d'interface** UI

</td>
</tr>
</table>

<div align="center">

**L'auteur décline toute responsabilité** en cas de mauvaise utilisation, de bannissement de compte, ou de sanction disciplinaire.

</div>

---

<div align="center">

## 🤝 Contribution

</div>

Les **PR sont les bienvenues** ! Idées d'amélioration :

<div align="center">

| 💡 Idée | 🎯 Difficulté |
|:--------|:-------------:|
| Mode rafale (X clics puis pause) | 🟢 Facile |
| Overlay visuel ON/OFF | 🟡 Moyen |
| Support multi-touches configurable | 🟡 Moyen |
| Mode "human-like" (délais aléatoires) | 🟠 Avancé |
| Compilation en `.exe` signé | 🔴 Difficile |

</div>

Ouvre une **issue** avant d'attaquer une grosse feature.

---

<div align="center">

## 📜 Licence

**MIT** — fais-en ce que tu veux, aucune restriction.

[![MIT](https://img.shields.io/badge/License-MIT-2ecc71?style=for-the-badge)](LICENSE)

---

## 🌟 Support

Si ce projet t'a servi, mets une **étoile** ⭐

[![Star](https://img.shields.io/github/stars/guiwarp/CompactClicker?style=social)](https://github.com/guiwarp/CompactClicker)
[![Fork](https://img.shields.io/github/forks/guiwarp/CompactClicker?style=social)](https://github.com/guiwarp/CompactClicker/fork)

<br>

<img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=6,11,20&height=120&section=footer&text=CompactClicker%20%E2%80%94%20by%20guiwarp&fontSize=22&fontAlignY=70&animation=fadeIn" width="100%"/>

</div>
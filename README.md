<!-- | By La-BaVuUr3-38 | -->

# 🖧 TSSR Révision — Application de révision tout-en-un

> Application web **monofichier**, **100 % hors-ligne**, pour la préparation au Titre Professionnel **TSSR** (Technicien Supérieur Systèmes et Réseaux — TP-01351 v02, RNCP niveau 5).

![Statut](https://img.shields.io/badge/statut-actif-brightgreen)
![Type](https://img.shields.io/badge/type-single--file%20HTML-blue)
![Offline](https://img.shields.io/badge/100%25-hors--ligne-orange)
![Dépendances](https://img.shields.io/badge/d%C3%A9pendances-aucune-success)
![Responsive](https://img.shields.io/badge/responsive-mobile%20%7C%20tablette%20%7C%20desktop-purple)
![Licence](https://img.shields.io/badge/licence-MIT-lightgrey)

---

## 📖 Description

**TSSR Révision** est un outil d'apprentissage complet regroupé dans **un seul fichier HTML** (`index.html`). Aucune installation, aucun serveur, aucune dépendance externe (pas de CDN) : il suffit d'ouvrir le fichier dans un navigateur, y compris **sans connexion Internet**.

Le projet couvre l'intégralité du **référentiel d'évaluation officiel** du titre TSSR, complété par des supports de cours (Linux, virtualisation, réseau Cisco, Windows Server) et des outils d'entraînement interactifs.

---

## ✨ Fonctionnalités principales

| Fonctionnalité | Description |
|---|---|
| 📝 **Examen blanc** | **873 questions** réparties en **31 catégories** (QCM + questions à saisir), tirage aléatoire, correction commentée |
| 🧮 **Calculateur réseau** | Générateur d'exercices **infinis** (sous-réseaux, wildcard, CIDR) + outil de calcul instantané (réseau, broadcast, masque, plage d'hôtes) |
| ⏱️ **Chronomètre** | Mode minuté optionnel (30/60/90 s) pour s'entraîner en conditions d'examen |
| 🔁 **Révision des erreurs** | Rejoue uniquement les questions ratées pour cibler ses faiblesses |
| 📊 **Suivi de progression** | Statistiques de maîtrise par catégorie (stockage local) |
| 🔍 **Recherche globale** | Barre de recherche avec **indexation automatique** de tout le contenu |
| 🎨 **Thème clair / sombre** | Bascule d'affichage, préférence mémorisée |
| 📱 **Responsive + menu hamburger** | Interface fluide sur mobile, tablette et desktop |

---

## 📚 Contenu pédagogique

L'application est organisée en **41 onglets thématiques**, dont un aide-mémoire complet :

- **Réseau** : Modèle OSI, TCP/IP, Adressage IPv4/IPv6, VLAN, Routage, NAT/PAT, WAN, Wi-Fi
- **Systèmes** : Administration Linux (commandes + fichiers essentiels), Windows Server, Active Directory, GPO, Virtualisation
- **Sécurité & Haute Dispo** : Pare-feu, IDS/IPS, VPN, **Infrastructure Hyperconvergée (HCI)**, PRA/PCA/PRI, sauvegarde (règle 3-2-1)
- **Services** : DNS/DHCP, Messagerie, VoIP, Conteneurs, Supervision, WDS/PXE, Stockage (RAID, iSCSI, NFS)
- **Aide-mémoire Windows** : commandes CMD/PowerShell, dossiers système, **raccourcis clavier** et commandes Exécuter (`Win+R` : `.msc`, `.cpl`…)
- **Transverse** : Anglais technique, Documentation d'exploitation, Méthodologie, Support/ITIL

### Répartition des questions par catégorie

| Catégorie | Questions | Catégorie | Questions |
|---|:---:|---|:---:|
| Linux | 87 | DNS/DHCP | 25 |
| Adressage | 44 | WDS/PXE | 25 |
| Sauvegarde | 39 | NAT/PAT | 25 |
| Pare-feu | 37 | Protocoles ↔ Couches | 25 |
| Haute Dispo | 37 | Anglais technique | 25 |
| Protocoles | 28 | GPO | 24 |
| Cisco IOS | 27 | Messagerie | 24 |
| Supervision | 26 | VoIP | 24 |
| Active Directory | 26 | Support | 24 |
| Stockage | 26 | Wi-Fi | 24 |
| PowerShell | 26 | Méthodologie | 22 |
| OSI | 25 | Doc exploitation | 14 |
| TCP/IP | 25 | Matériel | 14 |
| VLAN | 25 | | |
| Virtualisation | 25 | | |
| Conteneurs | 25 | | |
| Dépannage | 25 | | |
| IPv6 | 25 | **TOTAL** | **873** |

---

## 🚀 Installation & utilisation

Aucune installation requise. Le projet ne dépend d'**aucune** bibliothèque externe.

### Option 1 — Téléchargement direct

1. Télécharge le fichier [`index.html`](index.html)
2. Double-clique dessus (ou ouvre-le dans ton navigateur)
3. C'est prêt — y compris hors-ligne ✅

### Option 2 — Cloner le dépôt

```bash
git clone https://github.com/<ton-utilisateur>/<ton-repo>.git
cd <ton-repo>
```

Puis ouvre `index.html` dans ton navigateur :

```bash
# Linux
xdg-open index.html

# macOS
open index.html

# Windows (PowerShell)
start index.html
```

### 💡 Astuce mobile

Sur iOS/Android, via le menu du navigateur → **« Ajouter à l'écran d'accueil »** pour l'ouvrir en plein écran comme une application.

---

## 🛠️ Stack technique

- **HTML5** sémantique
- **CSS3** — Flexbox & Grid, media queries, variables CSS (thème clair/sombre)
- **JavaScript vanilla** (ES6+) — aucune dépendance, aucun framework
- **Stockage local** (`localStorage`) pour les préférences et statistiques
- **Architecture** : fichier unique auto-suffisant, exécution 100 % côté client

> ✅ **Zéro dépendance** — aucun `npm install`, aucun CDN, aucun serveur. L'ensemble du code (HTML/CSS/JS) tient dans un seul fichier portable.

---

## 🔐 Sécurité & bonnes pratiques

Le projet applique plusieurs bonnes pratiques de développement web sécurisé (OWASP) :

- **Validation des entrées** — le calculateur réseau valide chaque saisie (format IP, bornes `0–255`) avant traitement
- **Prévention XSS** — les zones dynamiques n'injectent que des **valeurs calculées** (jamais la saisie brute de l'utilisateur telle quelle)
- **Aucune ressource distante** — pas de CDN ni de requête réseau : surface d'attaque minimale, aucune fuite de données, aucun traçage tiers
- **Fonctionnement local** — toutes les données (progression, préférences) restent sur la machine de l'utilisateur via `localStorage`

> ⚠️ **Note de transparence** : s'agissant d'une application **monofichier côté client**, l'intégralité du code (dont les réponses aux questions) est par nature accessible dans le navigateur. Ce projet est un **outil de révision ouvert**, pas un système d'examen sécurisé — aucune donnée sensible n'y est stockée.

---

## 📱 Compatibilité

| Plateforme | Statut |
|---|:---:|
| 🖥️ Desktop (Chrome, Firefox, Edge, Safari) | ✅ |
| 📱 Mobile (iOS / Android) | ✅ |
| 📟 Tablette | ✅ |
| 🌐 Hors-ligne (sans connexion) | ✅ |

Interface **responsive** testée sans débordement de **360 px** à **1280 px+**, avec **menu hamburger** sur mobile.

---

## 🗺️ Feuille de route

- [ ] Mode **VLSM** dans le calculateur (découpage d'un réseau en N sous-réseaux)
- [ ] Support **IPv6** (compression / expansion d'adresses)
- [ ] Export des statistiques de progression (JSON / CSV)
- [ ] Surlignage du terme exact trouvé lors d'une recherche

---

## 🤝 Contribution

Les suggestions et corrections sont les bienvenues. Ouvre une *issue* ou une *pull request*.

---

## 📄 Licence

Ce projet est distribué sous licence **MIT** — voir le fichier [`LICENSE`](LICENSE) pour les détails.

Tu es libre de l'utiliser, le modifier et le partager, y compris à des fins pédagogiques ou commerciales, sous réserve de conserver la mention de licence.

---

## 👤 Auteur

Développé dans le cadre d'une formation **TSSR**.

**| By La-BaVuUr3-38 |**

---

<p align="center">
  <sub>⭐ Si ce projet t'aide dans ta révision TSSR, n'hésite pas à laisser une étoile !</sub>
</p>

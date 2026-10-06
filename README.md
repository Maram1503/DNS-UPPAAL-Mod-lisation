# 🔐 Modélisation et vérification du protocole DNS avec UPPAAL

Modélisation du protocole **DNS** sous forme d'automates temporisés avec **UPPAAL**, et vérification formelle de sa sécurité face à des attaques par empoisonnement de cache (attaque **Kaminsky** et attaque sur le **CRC32**).

## 🎯 Objectif
Représenter le fonctionnement d'une résolution DNS, modéliser le comportement d'un attaquant, puis vérifier avec le model checker d'UPPAAL si les propriétés de sécurité sont respectées (et dans quels cas elles sont violées).

## 📁 Contenu du dépôt

| Fichier | Description |
|---|---|
| `modele/main.xml` | Modèle principal du protocole DNS |
| `modele/safe.xml` | Version sécurisée du modèle |
| `modele/Kaminsky_attack.xml` | Modèle de l'attaque Kaminsky (empoisonnement du cache DNS) |
| `modele/crc32_attack.xml` | Modèle de l'attaque exploitant le CRC32 |
| `rapport/Rapport_DNS_UPPAAL.pdf` | Rapport complet du projet |

> À vérifier : adaptez la colonne « Description » si le rôle exact d'un fichier est différent.

## 🧩 Modèle
Décrivez ici en 4 ou 5 lignes :
- les **entités** modélisées (client, résolveur, serveur de noms, attaquant...) ;
- les **canaux** et messages échangés (requête, réponse...) ;
- les **variables et horloges** importantes (identifiant de requête, délai de réponse...).

## ✅ Propriétés vérifiées

| Propriété | Requête UPPAAL | Modèle | Résultat |
|---|---|---|---|
| Absence de blocage | `A[] not deadlock` | `main.xml` | Satisfaite |
| Cache non empoisonné | `A[] ...` | `safe.xml` | À compléter |
| Empoisonnement possible | `E<> ...` | `Kaminsky_attack.xml` | À compléter |
| Attaque via CRC32 | `E<> ...` | `crc32_attack.xml` | À compléter |

## 🚀 Utilisation
1. Télécharger et installer [UPPAAL](https://uppaal.org).
2. Ouvrir un fichier du dossier `modele/` avec **File > Open**.
3. Utiliser l'onglet **Simulator** pour observer les exécutions.
4. Utiliser l'onglet **Verifier** pour lancer les requêtes de vérification.

## 📸 Aperçu
<!-- Ajoutez vos captures dans docs/ puis décommentez : -->
<!-- ![Automate du résolveur](docs/resolveur.png) -->
<!-- ![Résultats du vérificateur](docs/verification.png) -->

## 📄 Rapport
Le rapport détaille la démarche de modélisation, les hypothèses retenues et l'analyse des résultats : [`rapport/Rapport_DNS_UPPAAL.pdf`](rapport/Rapport_DNS_UPPAAL.pdf).

## 👩‍💻 Auteure
**Maram Othmani**
- GitHub : [@Maram1503](https://github.com/Maram1503)
- LinkedIn : [votre profil](https://www.linkedin.com/in/votre-nom)

Projet réalisé dans un cadre pédagogique.

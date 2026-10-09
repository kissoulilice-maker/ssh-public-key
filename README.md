# Projet CS Cybersecurité — Démonstration SSH avec GitHub

## Présentation du projet

Ce projet permet de découvrir et de tester l'authentification SSH pour sécuriser les échanges entre un ordinateur Windows et GitHub.

## Objectifs

- Comprendre le fonctionnement des clés SSH.
- Générer une paire de clés avec l'algorithme Ed25519.
- Ajouter la clé publique au compte GitHub.
- Tester l'authentification SSH.
- Envoyer des fichiers vers un dépôt distant avec Git.

## Fonctionnement des clés SSH

Une paire de clés SSH comprend deux fichiers :

- **Clé publique** : `id_ed25519.pub`. Elle est ajoutée aux paramètres SSH de GitHub.
- **Clé privée** : `id_ed25519`. Elle doit rester secrète et ne doit jamais être publiée.

## Commandes utilisées

### 1. Vérifier la version du client SSH

```bash
ssh -V
```

### 2. Afficher la clé publique

```bash
cat ~/.ssh/id_ed25519.pub
```

### 3. Tester l'authentification GitHub

```bash
ssh -T git@github.com
```

### 4. Vérifier le dépôt distant

```bash
git remote -v
```

### 5. Envoyer les modifications sur GitHub

```bash
git push
```

## Résultat

La connexion SSH permet de s'authentifier auprès de GitHub pour envoyer et récupérer du code sans saisir le mot de passe du compte à chaque opération Git.

Une phrase secrète peut toutefois être demandée pour déverrouiller la clé privée.

##  Sécurité

- Ne jamais publier la clé privée.
- Protéger la clé privée avec une phrase secrète.
- Partager uniquement la clé publique lorsque nécessaire.
- Ne pas ajouter de mots de passe, de jetons ou d'autres secrets au dépôt.

## Environnement utilisé

- Système : Windows
- Terminal : Git Bash
- Client SSH : OpenSSH
- Gestion de versions : Git
- Hébergement du code : GitHub

## 🎓 Contexte pédagogique

Projet réalisé dans le cadre de la formation CIEL  
**Cybersécurité, Informatique et réseaux, Électronique.**

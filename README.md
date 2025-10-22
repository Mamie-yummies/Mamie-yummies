## Hi there 👋

<!--
**Mamie-yummies/Mamie-yummies** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
#!/bin/bash
# Script Termux pour installer Node.js, Git et déployer le projet ma-mie-yummies

# Mettre à jour Termux et les packages
pkg update -y
pkg upgrade -y

# Installer Node.js et Git
pkg install nodejs git -y

# Vérifier l'installation
echo "Versions installées :"
node -v
npm -v
git --version

# Cloner le dépôt GitHub (remplacer tonpseudo par ton vrai nom GitHub)
REPO_URL="https://github.com/tonpseudo/ma-mie-yummies.git"
DIR_NAME="ma-mie-yummies"

if [ ! -d "$DIR_NAME" ]; then
    echo "Clonage du dépôt..."
    git clone $REPO_URL
else
    echo "Le dossier $DIR_NAME existe déjà, mise à jour..."
    cd $DIR_NAME
    git pull
    cd ..
fi

# Aller dans le dossier du projet
cd $DIR_NAME

# Installer les dépendances Node
echo "Installation des dépendances..."
npm install

# Lancer le script deploy
echo "Déploiement du projet..."
npm run deploy

echo "✅ Projet déployé avec succès !"

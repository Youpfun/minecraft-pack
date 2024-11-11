# Installation du Pack de Ressources sur Aternos

Ce guide vous explique comment installer et configurer un pack de ressources sur un serveur Minecraft Aternos en utilisant Google Drive pour l'hébergement du pack.

## Prérequis

Avant de commencer, assurez-vous d'avoir :
- Un pack de ressources Minecraft compressé en fichier `.zip`.
- Un compte Google Drive pour héberger le fichier.
- L'accès au tableau de bord de votre serveur Minecraft sur **Aternos**.

## Étapes d'Installation

### 1. Héberger le Pack de Ressources sur Google Drive

1. **Téléchargez votre pack de ressources** (au format `.zip`).
2. **Téléversez le pack de ressources** sur votre **Google Drive**.
   - Allez sur [Google Drive](https://drive.google.com/).
   - Cliquez sur le bouton **"+ Nouveau"**, puis sélectionnez **"Téléverser un fichier"**.
   - Sélectionnez votre fichier `.zip` et attendez qu'il soit téléchargé.

3. **Rendre le fichier public** :
   - Cliquez droit sur le fichier que vous avez téléchargé, puis sélectionnez **"Obtenir le lien"**.
   - Changez l'accès pour que **"Tout le monde ayant le lien"** puisse visualiser le fichier.
   
4. **Obtenez le lien de partage** :
   - Une fois le fichier téléchargé et partagé, vous verrez un lien comme celui-ci :
     ```
     https://drive.google.com/file/d/ID_DU_FICHIER/view?usp=sharing
     ```

   - L'ID du fichier est la partie après `/d/` et avant `/view`. Par exemple, dans le lien ci-dessus, l'ID est `ID_DU_FICHIER`.

5. **Transformez le lien en un lien de téléchargement direct** :
   - Remplacez l'ID dans l'URL de partage par `https://drive.google.com/uc?export=download&id=`.
     Par exemple :
     ```
     https://drive.google.com/uc?export=download&id=ID_DU_FICHIER
     ```

### 2. Configurer le Serveur Aternos

1. **Accédez à votre tableau de bord Aternos**.
   - Connectez-vous sur [Aternos](https://aternos.org/).
   - Allez dans la page d'accueil de votre serveur.

2. **Accédez aux options du serveur** :
   - Cliquez sur **"Options"** dans le menu du serveur.

3. **Modifier le fichier `server.properties`** :
   - Recherchez la ligne **`resource-pack`**.
   - Remplacez la valeur par l'URL de téléchargement direct que vous avez obtenue précédemment. Par exemple :
     ```properties
     resource-pack=https://drive.google.com/uc?export=download&id=ID_DU_FICHIER
     ```

4. **Enregistrer et redémarrer le serveur** :
   - Sauvegardez les changements effectués dans `server.properties`.
   - Redémarrez votre serveur Aternos pour appliquer les modifications.

### 3. Vérification et Téléchargement du Pack

1. **Rejoignez votre serveur Minecraft** :
   - Lancez Minecraft et connectez-vous à votre serveur.
   
2. **Invitez les joueurs à télécharger le pack** :
   - Lorsqu'un joueur rejoint le serveur, il recevra une invite lui demandant s'il souhaite télécharger le pack de ressources.
   - Ils devront accepter pour que le pack s'applique.

### 4. Résolution des Problèmes

- **Le pack ne se télécharge pas ?**  
  Vérifiez que l'URL du pack est correcte et que le fichier est public sur Google Drive.
  
- **Les joueurs ne peuvent pas voir le pack ?**  
  Assurez-vous que le fichier `.zip` contient bien les textures et ressources nécessaires et qu'il est bien formaté pour Minecraft.

---

## Conclusion

En suivant ces étapes simples, vous pouvez facilement héberger et configurer un pack de ressources personnalisé pour votre serveur Minecraft Aternos. Si vous avez des questions ou rencontrez des problèmes, n'hésitez pas à consulter la documentation d'Aternos ou à demander de l'aide dans les forums.

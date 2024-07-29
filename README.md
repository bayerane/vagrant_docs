# vagrant
## Installation de vagrant sous linux ubuntu
Pour installer Vagrant sur Ubuntu, suivez ces étapes :

- Mettre à jour votre liste de paquets :
```bash
sudo apt update
```

- Installer les dépendances nécessaires :
```bash
sudo apt install -y curl gnupg2 software-properties-common
```

- Ajouter le dépôt officiel de HashiCorp (éditeur de Vagrant) :
```bash
curl -fsSL https://apt.releases.hashicorp.com/gpg | sudo apt-key add -
sudo apt-add-repository "deb [arch=amd64] https://apt.releases.hashicorp.com $(lsb_release -cs) main"
```

- Mettre à jour la liste des paquets à nouveau :
```bash
sudo apt update
```

- Installer Vagrant :
```bash
sudo apt install vagrant
```

- Vérifier l'installation de Vagrant :
```bash
vagrant --version
```

## Desinstaller vagrant sous ubuntu
Pour désinstaller Vagrant de votre système Ubuntu, suivez ces étapes :

- Supprimer Vagrant :
```bash
sudo apt remove --purge vagrant
```

- Supprimer les fichiers de configuration inutiles :
```bash
sudo apt autoremove
sudo apt clean
```

- Supprimer les fichiers résiduels de Vagrant, si nécessaire :

Vous pouvez vérifier et supprimer manuellement les dossiers liés à Vagrant, si nécessaire. Par défaut, les fichiers Vagrant se trouvent généralement dans votre répertoire utilisateur `~/.vagrant.d`.
```bash
rm -rf ~/.vagrant.d
```

## Installer Vagrant sous windows
### Télécharger Vagrant :
Allez sur le site de [Vagrant](https://www.vagrantup.com/) et téléchargez la version pour Windows.

### Installer Vagrant :
Exécutez le fichier d'installation téléchargé et suivez les instructions pour installer Vagrant.

### Vérifier l'installation
- Ouvrir une invite de commandes :
Appuyez sur `Win + R`, tapez cmd et appuyez sur Entrée.

- Vérifier l'installation de Vagrant :
Dans l'invite de commandes, tapez :
```bash
vagrant --version
```
Vous devriez voir la version de Vagrant installée.

### Utiliser Vagrant
- Créer un répertoire de projet :
Par exemple, créez un répertoire `vagrant_project` sur votre bureau :
```bash
mkdir C:\Users\<votre_nom_utilisateur>\Desktop\vagrant_project
cd C:\Users\<votre_nom_utilisateur>\Desktop\vagrant_project
```

- Initialiser un nouveau projet Vagrant :
Dans le répertoire créé, initialisez un nouveau projet Vagrant :
```bash
vagrant init hashicorp/bionic64
```
Cela créera un fichier Vagrantfile dans le répertoire.

- Démarrer la machine virtuelle :
Toujours dans le répertoire de votre projet, lancez la machine virtuelle :
```bash
vagrant up
```

- Accéder à la machine virtuelle :
Pour vous connecter à la machine virtuelle, utilisez :
```bash
vagrant ssh
```
Si vous utilisez une invite de commande Windows qui ne supporte pas ssh, vous pouvez utiliser une application comme PuTTY pour vous connecter.

## Desinstaller Vagrant sous windows
### Désinstaller Vagrant
- Ouvrir le Panneau de configuration :
Appuyez sur `Win + R`, tapez `ctrl`, et appuyez sur `Entrée`.

- Accéder à la section Programmes :
Cliquez sur `Désinstaller un programme` sous la section `Programmes`.

- Trouver Vagrant dans la liste :
Faites défiler la liste des programmes installés et trouvez `Vagrant`.

- Désinstaller Vagrant :
Cliquez sur `Vagrant` pour le sélectionner, puis cliquez sur `Désinstaller` en haut de la liste.
Suivez les instructions de désinstallation.

### Supprimer les fichiers de configuration (facultatif)
Si vous souhaitez supprimer complètement tous les fichiers de configuration de Vagrant, vous pouvez également supprimer les dossiers de configuration :

- Supprimer le dossier `.vagrant.d` :

Ouvrez l'explorateur de fichiers et allez dans le répertoire utilisateur (`C:\Users\<votre_nom_utilisateur>`).
Trouvez et supprimez le dossier `.vagrant.d.`

- Supprimer les dossiers de projet Vagrant :
Si vous avez des répertoires de projets Vagrant, supprimez-les manuellement.

## documentation
### Qu'est-ce que Vagrant ?
- Définition de Vagrant
- Objectif principal : faciliter la
gestion des environnements de
développement
- [https://www.vagrantup.com/](https://www.vagrantup.com/) 

### Installation de Vagrant
- Prérequis : VirtualBox ou autre
fournisseur de virtualisation
- Étapes d'installation pour différents
systèmes d'exploitation (Windows,
macOS, Linux)
- [https://www.vagrantup.com/docs/installation](https://www.vagrantup.com/docs/installation)

### Utilisation de base de Vagrant
- Initialisation d'un projet Vagrant
```sh
vagrant init
```
- Lancement de l'environnement
```sh
vagrant up
```

- Connexion à la machine virtuelle
```sh
vagrant ssh [Nom_VM]
```
[https://www.vagrantup.com/docs/getting-started](https://www.vagrantup.com/docs/getting-started) 

### Gestion des environnements avec Vagrant
- Configuration de Vagrantfile
- Gestion des plugins
- Commandes utiles (`vagrant halt`, `vagrant destroy`, etc.)
- [https://www.vagrantup.com/docs/vagrantfile](https://www.vagrantup.com/docs/vagrantfile)

### Cas d'utilisation et exemples pratiques
- Exemples de projets utilisant
Vagrant (développement web, tests
d'intégration)
- Avantages de l'utilisation de
Vagrant en équipe
- [https://www.vagrantup.com/docs/why-vagrant](https://www.vagrantup.com/docs/why-vagrant)

### Ressources et liens utiles
- Documentation officielle
- Communauté et forums
- Autres outils complémentaires
(`Ansible`, `Docker`)
- [https://www.vagrantup.com/docs](https://www.vagrantup.com/docs)
- [https://www.vagrantup.com/community](https://www.vagrantup.com/community)

#### Commandes utiles de Vagrant
- **`vagrant init`** : Initialise un nouveau
projet Vagrant en créant un fichier Vagrantfile
- **`vagrant up`** : Démarre l'environnement
Vagrant (crée et configure la machine virtuelle)
- **`vagrant ssh`** : Se connecte à la machine virtuelle via SSH
- **`vagrant halt`** : Arrête la machine virtuelle
- **`vagrant destroy`** : Détruit la machine
virtuelle.
- **`vagrant reload`** : Redémarre la machine
virtuelle et recharge la configuration Vagrantfile.
- **`vagrant provision`** : Applique les scripts de provisionnement à la machine virtuelle.
- **`vagrant status`** : Affiche l'état actuel de la machine virtuelle.
- **`vagrant suspend`** : Suspende la machine virtuelle.
- **`vagrant resume`** : Reprend la machine virtuelle suspendue.
- **`vagrant box`** : Gère les boxes (boîtes) vagrant.
- **`vagrant plugin`** : Gère les plugins Vagrant.
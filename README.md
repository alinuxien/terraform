# VM Infra as Code

## Intêret
Création d'une machine virtuelle Linux outillée pour faire de l'Infrastructure As Code.

## Nécessite :
Vagrant

## Installe :
Terraform, Ansible et Docker dans une VM base Ubuntu Bionic 64

Autocomplétion pour terraform.

AWS CLI V2

## Usage
Dans un terminal : 

Clonez ce dépôt : `git clone https://github.com/alinuxien/terraform.git` 

Allez dans le dossier terraform : `cd terraform`

Lancez la construction : `vagrant up`

Lorsque c'est terminé, connectez-vous à la VM : `vagrant ssh`

Une fois connecté, il ne reste plus qu'à configurer vos identifiants Amazon : `aws configure`

( [Plus d'infos sur les identifiants Amazon](https://console.aws.amazon.com/iam/home?#security_credential) )

Et voilà! Enjoy...

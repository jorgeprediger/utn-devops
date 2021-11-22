# Crear una cuenta en github
# Agregar nuestra llave publica
# Crear el repositorio utn-devops
# Instalar Ansible
# Ubuntu/Debian
apt install ansible
# Instalar entorno
ansible-playbok utn-devops_install_environment.yml
# Crear repositorio git, Parado sobre el directorio unidad-1-vagrant
git init
# Configurar git, quitar --global si solo se desea configurar el repositorio actual
git config --global user.email "%youremailaddress@domain.com%"
git config --global user.name "%youruser%"

echo '.vagrant' > .gitignore
git status
git add .gitignore
git add README.md
git add utn-devops_install_environment.yml
git commit -m "Primer commit"
git branch -M unidad-1-vagrant
ssh -T git@github.com
git remote add origin git@github.com:%youruser%/utn-devops.git
git push -u origin unidad-1-vagrant
# Crear el archivo de configuracion Vagrantfile
vagrant init

git add Vagrantfile

# Realizar el primer commit
git commit
# Editar Vagrantfile

# Iniciar la maquina virtual
vagrant up

vagrant ssh

vagrant halt

vagrant destroy

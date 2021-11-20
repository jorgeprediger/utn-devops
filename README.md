# Instalar entorno
ansible-playbok utn-devops_install_environment.yml
# Crear repositorio git, Parado sobre el directorio unidad-1-vagrant
git init
# Configurar git, quitar --global si solo se desea configurar el repositorio actual
git config --global user.email "jorgeprediger@gmail.com"
git config --global user.name "jorgeprediger"
echo '.vagrant' > .gitignore

git status
git add .gitignore
git add README.md
git add utn-devops_install_environment.yml
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

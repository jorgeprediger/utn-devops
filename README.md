# Pasos para la practica 1
* Crear una cuenta en github
* Agregar nuestra llave publica en github
* Crear el repositorio utn-devops en github
* Instalar Ansible en nuestra PC
Ejemplo para distros Ubuntu/Debian
`apt install ansible`
* Instalar entorno en nuestra PC (git,vagrant,virtualbox)
`ansible-playbok utn-devops_install_environment.yml`
* Crear repositorio git en nuestra PC
```
mkdir ${HOME}/UTN-DevOps
cd ${HOME}/UTN-DevOps
git init
```
* Configurar git
Quitar --global si solo se desea configurar el repositorio actual)
```
git config --global user.email "%youremailaddress@domain.com%"
git config --global user.name "%youruser%"
ssh -T git@github.com
git remote add origin git@github.com:%youruser%/utn-devops.git
```

* Agregar archivos y hacer un push a github
```
echo '.vagrant' > .gitignore
git add .gitignore
touch README.md
git add README.md
git add utn-devops_install_environment.yml
git commit -m "Primer commit"
git branch -M unidad-1-vagrant
git push -u origin unidad-1-vagrant
```
* Crear el archivo de configuracion Vagrantfile
```
vagrant init
git add Vagrantfile
```

* Realizar el primer commit
`git commit -a -m "Add Vagrantfile"`

* Editar Vagrantfile

* Iniciar la maquina virtual
```
vagrant up
vagrant ssh
```

* Apagar maquina virtual y destruirla
```
vagrant halt
vagrant destroy
```

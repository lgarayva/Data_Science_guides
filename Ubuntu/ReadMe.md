
# Guia de usuarios para configurar Ubuntu para DataScience

Lo primero que hacemos es actualizar las librerías y paqueterías que nos ayudarán a configurar nuestra máquina. Para esto corremos las siguientes instrucciones en la terminal Ctrl+Alt+terminal

```
sudo apt-get update
sudo apt-get upgrade
```

Preparación:

```
sudo apt-get install gdebi-core
sudo apt-get install gnome-tweak-tool
sudo apt-get install libcurl4-openssl-dev 
sudo apt-get install libxml2-dev

```


## Docker

Instalamos Docker

```
sudo apt-get install docker.io
```

 
y verificamos que se instaló correctamente

```
docker --version
```

Lo siguiente que haremos es añadir a docker al grupo de usarios sudo con las siguientes instrucciones:

```
sudo groupadd docker
sudo usermod -aG docker $USER
```

Para verificar que se añadió correctamente corre la siguiente instrucción:

```
docker run hello-world 
```

Puede ser que sea necesario cerrer y volver a abrir la terminal.


Los siguientes son unos dockers que pueden ser útiles para Ciencia de Datos:

```

docker pull ubuntu
docker pull jupyter/pyspark-notebook
docker pull jupyter/datascience-notebook
docker pull jupyter/tensorflow-notebook
docker pull jupyter/all-spark-notebook
docker pull datascienceworkshops/data-science-at-the-command-line
docker pull pytorch/pytorch

```


## git

Instalamos git

```
sudo apt-get install git
```

y verificamos la instalación

```
git --version
```

Para cinfigurar el usuario de git es necesario utilizar el siguiente comando:

```
git config --global user.name "tu_usuario"
```

```
git config --global user.email "tucorreo@servidor.com"
```

## htop

Para ver el comsumo de recursos de la máquina podemos hacer uso de htop, es necesario instalarlo:

```
sudo apt-get install htop
```

```
htop
```

Para instalar R, Rstudio y Anaconda se necesitan ciertas paqueterías y será necesario descargarlas con la siguiente instrucción:

```
sudo apt-get install libgl1-mesa-glx libegl1-mesa libxrandr2 libxrandr2 libxss1 libxcursor1 libxcomposite1 libasound2 libxi6 libxtst6
```

## R y Rstudio

```
sudo apt-get install curl 
sudo apt-get install libssl-dev 
sudo apt-get install libcurl4-openssl-dev 
sudo apt-get install libxml2-dev

```

Para instalar R:

```
sudo apt-get install r-base
```


Para instalar Rstudio:

```
sudo apt-get install gdebi-core
wget https://download1.rstudio.org/desktop/bionic/amd64/rstudio-1.3.1093-amd64.deb
sudo gdebi rstudio-1.3.1093-amd64.deb
```


Para instalar Rstduio Server (opcional):

``` 
sudo apt-get install gdebi-core
wget https://download2.rstudio.org/server/xenial/amd64/rstudio-server-1.3.1093-amd64.deb
sudo gdebi rstudio-server-1.3.1093-amd64.deb
```

Si quieres instalar otra versión deberás visitar: https://rstudio.com/products/rstudio/download/#download

## Anaconda

Ahora procederemos a instalar Anaconda:

```
wget https://repo.anaconda.com/archive/Anaconda3-2020.07-Linux-x86_64.sh

bash Anaconda3-2020.07-Linux-x86_64.sh 

```

Posteriormente desplegará la licencia y pedirá que la aceptes.

Deberás aceptartla y posterimente correr la siguiente isntrucción:

```
source ~/.bashrc

```

Para poder utilizar anaconda será necesario que cierres y vuelvas a abrir la terminal.

Con el siguiente comando podrás actualizar conda:

```
conda update --all
```

## Redshift

Si utilizas bantante la computadora es recomendable intstalar la redshift.

```
sudo apt-get install redshift redshift-gtk
```

## PostgreSQL

Para instalar PostgreSQL:

```
sudo apt install postgresql postgresql-contrib
```

Posteriomente puedes ingresar con el usuario postrgres para realizar la configuración:

```
sudo -u postrges psql
```

Para salir de PostgreSQL

```

\q
```

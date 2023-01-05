+++
title = "Bievenidos"
chapter = true
weight = 5
pre = "<b>1. </b>"
+++

## Creación de un Blog y Subirlo a github Pages.

#### Requisitos

- Tener instalado hugo

#### Inicializar el proyecto con hugo

inicializamos el proyecto con el siguiente comando:

```bash
hugo new site <nombre_proyecto>
```

#### Ingresamos al directorio del proyecto

Para ingresar al directorio del proyecto utilizamos el siguiente comando.

```bash
cd <nombre_proyecto>
```

#### Inicializar git con el proyecto

inicializamos el repo con el siguiente comando:

```bash
git init
```

#### Agregar un submodulo del tema

comando:

```bash
git submodule add <link_repo_del_tema> themes/<nombre del tema>
```

comando utilizando el tema de ejemplo relearn

```bash
git submodule add https://github.com/McShelby/hugo-theme-relearn.git themes/relearn
```

#### Agregamos ese tema al config.toml, y cambiaremos el directorio donde se crean nuestros estáticos para que Github pages lo reconozca sin problema.

El archivo **config.toml** debería quedar de la siguiente manera:

```bash
languageCode = 'en-us'
title = 'Docuemntaciones'
theme = 'relearn'
publishDir = 'docs'
```

Ahora para agregar una publicación, nos dirigimos al adirectorio **content** y ahi creamos una publicación.

## Iniciar Servidor

Para iniciar el servidor ejecutamos el siguiente comando en la carpeta raiz de nuestro proyecto.

```bash
hugo server -D
```

> La ruta para visualizar nuestro proyecto en locas es: **localhost:1313**

## Configuración Github Pages

#### Creamos el respositorio en github

Una vez creado el repositorio en github, procedemos a ingresar los siguientes comandos en nuestro proeycto local:

- Inicializamos el repo.

```bash
git init
```

```bash
git remote add origin https://github.com/Luis-Salinas-SD/docs-2022.git
```

- Agergamos los archivos

```bash
git add .
```

- Ahora usamos el comando hugo para crear los estáticos en una carpeta llamada /docs

```bash
hugo
```

- Lo siguiente que haremos es crear un commit y subirlo a nuestro repositorio

```bash
git commit -m 'init proyect';

```

- Realizamos el push al repo.

```bash
git push origin master
```

## Subir cambios a git

Generar los estaticos

```bash
hugo
```

Agregamos los archivos al state

```bash
git add .
```

Agregamos los archivos al state

```bash
git commit -m 'comentario'
```

Agregamos los archivos al state

```bash
git push origin master
```

## Archivo config.toml

El archivo final quedaría de la siguiente manera:

```toml
themeVariant = 'relearn-dark'
baseURL = 'https://luis-salinas-sd.github.io/docs-2022/'
languageCode = 'en-us'
title = 'Mis Documentaciones'
theme = 'relearn'
publishDir = 'docs'
```

## Apps imprescindibles<a name="id4"></a>
* [Sublime (Package Control y LiveReload)](https://www.sublimetext.com)<br>
* [Visual Studio Code](https://code.visualstudio.com/)
    * Live Sass Compiler (compila Sass/Scss a css)
    * Live Server (lanza un servidor local que se autorefresca)
    * ESLint (https://johnserrano.co/blog/configurar-eslint-con-vscode-para-javascript y ejecutar ESLint al guardar un fichero: https://medium.com/@netczuk/even-faster-code-formatting-using-eslint-22b80d061461)
    * eCSStractor(https://marketplace.visualstudio.com/items?itemName=diz.ecsstractor-port).
* [Koala App(compilador de Sass y Less gratuito)](http://koala-app.com)
* [Prepros (compilador de Sass y Less)](https://prepros.io)
* Suite Adobe (Photoshop, Illustrator, Acrobat, Indesign)
* [Google Web Designer](https://webdesigner.withgoogle.com)
* Sketch
* Microsoft Word
* [Spotify](https://www.spotify.com/es/)
* [FontBase](https://fontba.se/)
* [Skype](https://www.skype.com/es/get-skype/)

## Utilidades
* [carbon](https://carbon.now.sh)
* [GiphyCapture](https://giphy.com/apps/giphycapture)

## Links
* [Links de ayuda y/o consulta](https://github.com/pixel-y-trama/cajon-desastre/blob/master/links.md#links-de-ayuda-yo-consulta)


## Configurar Github

<details>
<summary>Algunos comandos que se usan</summary>

```
Operaciones locales:
working directory -> staging area -> git repository
```

### Crear rama en local

```
# Situarte en la rama desde donde quieres crear la rama
git checkout develop

# Comprobar que se tienen los últimos cambios
git fetch
git pull

# Crear la rama
git checkout -b feat/new-feature
```

### Añadir al `staging area` todos los ficheros

```
# Ver el estado actual de los cambios (qué está en el índice para subir)
git status

# Comprobar en VS Code las diferencias de los ficheros para asegurar que lo que subes es lo que quieres subir

git add .
```

### Quitar un fichero del `staging area`

```
git reset HEAD -- <file>
```

### Deshacer cambios de los ficheros que están en el `working directory` (todavía no subidos al `staging area`)

```
git checkout .
```

### Commit para subir ficheros del `staging area` al `git directory`
```
git commit -m "Commit message"
```

### Subir a la misma rama en remoto

```
git push origin HEAD
```

### Rebase de master a tu rama

```
# Asegurarte que estás en tu rama

git status

# Sincronizarte con el remoto

git fetch

git rebase origin/master

# resolver conflictos si los hubiera

git add .

git rebase —continue

# subir la rama rebasada a remoto con -f

git push origin "feature-branch" -f
```

### Squash

http://gitready.com/advanced/2009/02/10/squashing-commits-with-rebase.html

Ejemplo: Combinar los últimos 4 commits tuyos en el primer commit de la lista:
```
git rebase -i HEAD~4

# Ejemplo (:wq al final para guardar como en vi)
pick 01d1124 Adding license
squash 6340aaa Moving license into its own file
squash ebfd367 Jekyll has become self-aware.
squash 30e0ccb Changed the tagline in the binary, too.

git add <file1> <file2>  # si conflictos

git rebase —continue # si conflictos

git push origin <branchname> -f
```

### Git amend

Ejemplo: quieres añadir algo al último commit

```
# Haces los cambios

git add <file1> <file2>

git commit --amend

git push origin <branchname> -f

```

### Dejar tu rama como en remoto

```
git reset —hard origin/rama
```

ó

```
git checkout -B master origin/master
```

### Borrar rama remota y local

```
git push -d origin feat/feature-branch
git branch -D feat/feature-branch
```

### Borrar todas las ramas locales excepto master

```
git branch | grep -v "master" | xargs git branch -D
```

### Cambiar rama local y remota

https://multiplestates.wordpress.com/2015/02/05/rename-a-local-and-remote-branch-in-git/

```
git branch -m feat/MHF-725-params
git push origin :feat/MHF-841-params feat/MHF-725-params
git push origin -u  feat/MHF-725-params
```

### Guardar cambios en stash y recuperarlos

```
# Guardar
git stash

# Recuperar borrando el stash
git stash pop

# Recuperar manteniendo el stash
git stash apply
```

### Buscar git commit por mensaje

```
git log --all --grep='Build 0051'
```

### Borrar tags

```
# Remote:
git push --delete origin tagname

# Local:
git tag --delete tagname
```

### Crear tags

```
git tag -a 3.26.0 -m "Version 3.26.0”

git push origin 3.26.0
```
</details>

## Configurar Chrome<a name="id4"></a>
* [ColorZilla](https://chrome.google.com/webstore/detail/colorzilla/bhlhnicpbhignbdhedgjhgdocnmhomnp?hl=es): cuentagotas web.
* [Full Page Screen Capture](https://chrome.google.com/webstore/detail/full-page-screen-capture/fdpohaocaechififmbbbbbknoalclacl): realiza capturas fullscreen de una web.
* [Wappalyzer](https://chrome.google.com/webstore/detail/wappalyzer/gppongmhjkpfnbhagpmjfkannfbllamg?hl=es): analiza las tecnologías que usa una web.
* [Save to Pocket](https://chrome.google.com/webstore/detail/save-to-pocket/niloccemoadcdkdjlinkgdfekeahmflj?hl=es): guarda enlaces web para leer luego.
* [30 seconds of knowledge](https://30secondsofknowledge.com/): snipeds nuevos en nuevas pestañas para ir aprendiendo código.

# my-first-package-danCG
Random string messages

## Install

```npm
npm i 021.2-my-first-package-dancg
```

## Usage

```bash
my-first-package-danCG
```

## Crear un paquete

1. Lo primero es verificar que el nombre del repositorio no esta
en [npm](https://www.npmjs.com/), para no tener conflictos a la hora de publicar.

2. Ya con nuestro repositorio en GitHub o la plataforma que usemos
clonamos el repositorio en nuestro entorno local.

    - `git clone HTTPS/SSHDelRepo`

3. Iniciamos la configuración inicial de npm.

    - `npm init -y`

4. Dentro de la crapeta src tenemos la función que inprime el msg
y la exportamos.

    - [Random-msg-funnyCommit](http://https://github.com/dan33pro/my-first-package-danCG/blob/main/src/index.js "Random-msg-funnyCommit")

5. Dentro de la carpeta bin tenemos la base del proyecto y del
comando de npm, donde nuestro archivo `.js` tiene:

    [Base-del-package-npm](https://github.com/dan33pro/my-first-package-danCG/blob/main/bin/global.js)

    - Una instrucción que indica que corre del lado del server.
    - El import del modulo que creamos.
    - La ejecución de la función importada.

6. Ahora en el [package.json](https://github.com/dan33pro/my-first-package-danCG/blob/main/package.json) debajo de "homepage" agregamos

    ````
    "bin": {
        "my-first-package-danCG": "./bin/global.js"
    },
    "preferGlobal": true
    ```

    Este sirve para indicarle el nombre del paquete y donde se encuentra el
    archivo global que va a ejecutar. al final indicamos que va a ser un paquete
    global.

## Publicar un paquete

1. Corremos el comando `sudo npm link` que crea un enlace simbolico
para reconocer el paquete dentro del listado de paquetes de npm.

> Sin publicarlo aun

2. Ahora vamos a probarlo, para esto necesitamos el `path` del proyecto.

    - `pwd`
    
    Simulamos la instalación, luego ya deberiamos poder probar el paquete 
    en mi caso con `my-first-package-danCG`.

    - `npm install -g /home/daniel/personalProjects/021.2-My-first-package-danCG`

3. Es necesario añadir nuestro usuario de npm, lo podemos hacer con:

    - `npm adduser`

    Y agregamos nuestras credenciales, sigue las instrucciones.

4. Ahora si pasamos a publicar con:

    - `npm publish`

## Versiones

Para cambiar de versiones debes tener en cuenta [Versionado Semántico](https://semver.org/lang/es/), hacemos
un commit y subismos cambios, luego corremos con la versión que consideres:

```npm
npm version 1.0.1
```

Y volvemos a usar `npm publish`
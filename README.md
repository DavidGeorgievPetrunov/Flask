# Flask

Para comenzar con el tutorial hay que instalar flask. 
![foto1](/FotosFlask/Foto1.png)

Despues de tener flask instalado y configurar el entorno creamos un fichero app.py.
![foto2](/FotosFlask/Foto2.png)

Para poder inicializar este fichero primero hay que inicializar el entorno virtual con el siguente comando.
![foto3](/FotosFlask/Foto3.png)

Despues de esto si utilizamos el commando python -m flask run desde el entorno se inicializara app.py como podemos ver:
![foto4](/FotosFlask/Foto4.png)

Cuando clickamos la ip nos lleva a la pagina web que hemos creado con el app.py
![foto5](/FotosFlask/Foto5.png)

Ahora lo que hacemos es añadir un trozo de codigo que hara que la pagina realize otra funcion cuando cambiamos su url.
![foto6](/FotosFlask/Foto6.png)

Ademas configuramos el launch.json del debugger de vscode para que podamos inicializar app.py sin utilizar la consola.
![foto7](/FotosFlask/Foto7.png)

En esta imagen ademas de salir el codigo como en una imagen un poco mas arriba podemos ver que el debugger sale como Python:Flask demostrando que el archivo launch.json ha sido creado.
![foto8](/FotosFlask/Foto8.png)

Ahora si utilizamos el debugger se inicializa app.py.
![foto9](/FotosFlask/Foto9.png)

Cambiando la url a la siguente mientras estamos debuggeando desde donde saldra en una imagen posteror se inicializaran las variables en python donde podremos interactuar con ellas mientras el programa esta debuggeandose, por si el programa no realiza lo que queremos asi podemos tocar las variables para ver si lo logramos hacer que funcione para luego modificarlo.
![foto10](/FotosFlask/Foto10.png)
![foto11](/FotosFlask/Foto11.png)

Si no nos interesa esto podemos acabar de debuggear y ahora que la pagina esta cargada si ponemos en la url /hello/nombre lo que este en nombre saldra por pantalla con el siguente texto.
![foto12](/FotosFlask/Foto12.png)

Ahora empezaremos a crear templates, el primero sera el hello_there.html
![foto13](/FotosFlask/Foto13.png)

Donde insertaremos el siguente codigo.
![foto14](/FotosFlask/Foto14.png)

Ahora para poder llamar a este codigo lo que realizaremos sera importar "from flask import render_template" en la app.py y cambiar la ruta hello que teniamos a la siguente.

@app.route("/hello/")
@app.route("/hello/<name>")
def hello_there(name = None):
    return render_template(
        "hello_there.html",
        name=name,
        date=datetime.now()
    )

Ahora si ejecutamos lap pagina el resultado es el siguente.
![foto15](/FotosFlask/Foto15.png)

Ahora crearemos la carpeta static donde meteremos site.css
![foto16](/FotosFlask/Foto16.png)

En el site.css insertaremos el css, tambien habra que cambiar el html para que sea de la clase del css, configurar la stylesheet y cambiaremos el strong a un span en el html.
![foto17](/FotosFlask/Foto17.png)

El resultado es el siguente.
![foto18](/FotosFlask/Foto18.png)

Ahora crearemos un data.json en el static en el cual insertaremos este codigo.
![foto19](/FotosFlask/Foto19.png)

Configuraremos la ruta en el app.py.
![foto20](/FotosFlask/Foto20.png)

Si utilizamos esta url desde la pagina el resultado es el siguente.
![foto21](/FotosFlask/Foto21.png)

Ahora empezaremos a crear multiples htmls para la pagina, primero necesitaremos un layout.html que sera la base de la pagina y desde donde llamaremos a los otros html.
![foto22](/FotosFlask/Foto22.png)

Cambiaremos el css para que la pagina sea mejor.
![foto23](/FotosFlask/Foto23.png)

Configuraremos unos snippets para poder luego realizar el codigo mas rapidamente.
![foto24](/FotosFlask/Foto24.png)
![foto25](/FotosFlask/Foto25.png)

Ahora crearemos home.html donde utilizaremos el snippet para crear este mismo ademas añadiremos una linea de codigo debajo del title que sera <p>Home page for the Visual Studio Code Flask tutorial.</p>.
![foto26](/FotosFlask/Foto26.png)

Aqui esta el about.html.
![foto27](/FotosFlask/Foto27.png)

Aqui esta el contact.html. 
![foto28](/FotosFlask/Foto28.png)

Este es el resultado final en cada uno de los htmls, primero home, luego about y finalmente contact, el nombre de la pestaña cambia con cada uno de ellos demostrando que me he movido.
![foto29](/FotosFlask/Foto29.png)
![foto30](/FotosFlask/Foto30.png)
![foto31](/FotosFlask/Foto31.png)
![foto32](/FotosFlask/Foto32.png)

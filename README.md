# Flask

Para comenzar con el tutorial hay que instalar flask. 
![foto1](/FotosFlask/Flask1.jpg)

Despues de tener flask instalado y configurar el entorno creamos un fichero app.py.
![foto2](/FotosFlask/Flask2.jpg)

Para poder inicializar este fichero primero hay que inicializar el entorno virtual con el siguente comando.
![foto3](/FotosFlask/Flask3.jpg)

Despues de esto si utilizamos el commando python -m flask run desde el entorno se inicializara app.py como podemos ver:
![foto4](/FotosFlask/Flask4.jpg)

Cuando clickamos la ip nos lleva a la pagina web que hemos creado con el app.py
![foto5](/FotosFlask/Flask5.jpg)

Ahora lo que hacemos es añadir un trozo de codigo que hara que la pagina realize otra funcion cuando cambiamos su url.
![foto6](/FotosFlask/Flask6.jpg)

Ademas configuramos el launch.json del debugger de vscode para que podamos inicializar app.py sin utilizar la consola.
![foto7](/FotosFlask/Flask7.jpg)

En esta imagen ademas de salir el codigo como en una imagen un poco mas arriba podemos ver que el debugger sale como Python:Flask demostrando que el archivo launch.json ha sido creado.
![foto8](/FotosFlask/Flask8.jpg)

Ahora si utilizamos el debugger se inicializa app.py.
![foto9](/FotosFlask/Flask9.jpg)

Cambiando la url a la siguente mientras estamos debuggeando desde donde saldra en una imagen posteror se inicializaran las variables en python donde podremos interactuar con ellas mientras el programa esta debuggeandose, por si el programa no realiza lo que queremos asi podemos tocar las variables para ver si lo logramos hacer que funcione para luego modificarlo.
![foto10](/FotosFlask/Flask10.jpg)
![foto11](/FotosFlask/Flask11.jpg)

Si no nos interesa esto podemos acabar de debuggear y ahora que la pagina esta cargada si ponemos en la url /hello/nombre lo que este en nombre saldra por pantalla con el siguente texto.
![foto12](/FotosFlask/Flask12.jpg)

Ahora empezaremos a crear templates, el primero sera el hello_there.html
![foto13](/FotosFlask/Flask13.jpg)

Donde insertaremos el siguente codigo.
![foto14](/FotosFlask/Flask14.jpg)

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
![foto15](/FotosFlask/Flask15.jpg)

Ahora crearemos la carpeta static donde meteremos site.css
![foto16](/FotosFlask/Flask16.jpg)

En el site.css insertaremos el css, tambien habra que cambiar el html para que sea de la clase del css, configurar la stylesheet y cambiaremos el strong a un span en el html.
![foto17](/FotosFlask/Flask17.jpg)

El resultado es el siguente.
![foto18](/FotosFlask/Flask18.jpg)

Ahora crearemos un data.json en el static en el cual insertaremos este codigo.
![foto19](/FotosFlask/Flask19.jpg)

Configuraremos la ruta en el app.py.
![foto20](/FotosFlask/Flask20.jpg)

Si utilizamos esta url desde la pagina el resultado es el siguente.
![foto21](/FotosFlask/Flask21.jpg)

Ahora empezaremos a crear multiples htmls para la pagina, primero necesitaremos un layout.html que sera la base de la pagina y desde donde llamaremos a los otros html.
![foto22](/FotosFlask/Flask22.jpg)

Cambiaremos el css para que la pagina sea mejor.
![foto23](/FotosFlask/Flask23.jpg)

Configuraremos unos snippets para poder luego realizar el codigo mas rapidamente.
![foto24](/FotosFlask/Flask24.jpg)
![foto25](/FotosFlask/Flask25.jpg)

Ahora crearemos home.html donde utilizaremos el snippet para crear este mismo ademas añadiremos una linea de codigo debajo del title que sera <p>Home page for the Visual Studio Code Flask tutorial.</p>.
![foto26](/FotosFlask/Flask26.jpg)

Aqui esta el about.html.
![foto27](/FotosFlask/Flask27.jpg)

Aqui esta el contact.html. 
![foto28](/FotosFlask/Flask28.jpg)

Este es el resultado final en cada uno de los htmls, primero home, luego about y finalmente contact, el nombre de la pestaña cambia con cada uno de ellos demostrando que me he movido.
![foto29](/FotosFlask/Flask29.jpg)
![foto30](/FotosFlask/Flask30.jpg)
![foto31](/FotosFlask/Flask31.jpg)
![foto32](/FotosFlask/Flask32.png)

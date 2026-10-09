# Visor + Gemini (Jarvis para tus libros)

Fusión de **Visor de documentos** (DjVu plugin) y **Gemini Voice Chat** en un solo plugin.

## Instalación

1. Copia la carpeta `visor-gemini` a `TU_BOVEDA/.obsidian/plugins/visor-gemini` (en el celular también: desde la v2.6 funciona ahí; si sincronizas la bóveda, basta con activarlo).
2. **Desactiva los plugins viejos** "Visor de documentos" y "Gemini Voice Chat" (si no, se pelean por las extensiones y los atajos).
3. Reinicia Obsidian → Ajustes → Plugins de la comunidad → activa **Visor + Gemini**.

El `data.json` ya trae juntos tus ajustes de ambos plugins (API keys, voz, micrófono, páginas recordadas).

## Qué hace

### 📲 Sincronizar solo: el computador recibe siempre y los archivos (y los plugins) van solos (v2.20)
Ya no hay que abrir *Transferir archivos* cada vez. Viene **todo encendido**; cada cosa se apaga en Ajustes → *Transferir archivos*. Hay que tener la 2.20 en los dos dispositivos.
- **El computador recibe siempre.** Empieza solo al abrir Obsidian y sigue todo el día, sin apagarse por falta de uso; si algo lo detiene, vuelve a recibir solo al minuto. Abajo, en la barra de estado, dice «⇄ Recibiendo» (un clic abre *Transferir*). Obsidian tiene que quedar abierto (minimizado sirve) y el computador sin suspenderse. La primera vez, Windows pregunta si Obsidian puede recibir conexiones: acepta.
- **El celular se sincroniza solo** con el computador emparejado (el código se escribe una sola vez y queda aunque se reinicien): al abrir Obsidian, al volver a la app, unos segundos después de cada cambio y, si algo cambió en el computador, al minuto. Gana el más nuevo y lo que se reemplaza queda en la Papelera. Si el computador no está a la vista (otra red, apagado), lo vuelve a intentar solo, cada vez más espaciado, sin molestar; si la dirección cambió, prueba las otras que conoce. Comando: *Sincronizar ahora con el computador*.
- **Límite de Android:** el celular congela las apps que no están en pantalla, así que sincroniza mientras Obsidian está abierto, y apenas lo abres o vuelves a él. Ningún plugin puede correr con Obsidian cerrado.
- **También los plugins.** Los plugins instalados en un lado aparecen en el otro, ya activos (sin reiniciar). Activar, desactivar o desinstalar uno en un lado hace lo mismo en el otro (gana el cambio más reciente; una desinstalación se confirma en la pasada siguiente). Si llega una versión nueva de un plugin activo, se recarga solo, y nunca se baja de versión aunque las fechas de los archivos digan otra cosa. Los ajustes de un plugin viajan solo cuando el otro lado no lo tiene; después, cada uno con los suyos. Los plugins que solo funcionan en computador no se copian al celular, y uno que no carga en el celular no se reintenta en cada pasada. **Visor + Gemini se actualiza también así**: actualízalo en el computador y al celular le llega; aparece un aviso con *Usarla ahora*. Sus ajustes (tus API keys y el emparejamiento) nunca viajan ni se pueden pedir.
- **Borrar también en el otro lado.** Lo que borras o cambias de nombre en un lado se borra en el otro (queda 30 días en su Papelera). Solo cuenta lo borrado mientras la sincronización está encendida. Si se borran muchos archivos de una vez, no se borra nada sin preguntar: aparece un aviso con *Borrarlos también allá*. Una carpeta solo se quita si quedó vacía de verdad (con archivos ocultos, como `.git`, se queda).
- **Cuidados:** una nota que se está editando mientras llega otra versión no se pisa (se revisa en la pasada siguiente); una nota abierta que se actualiza cambia en pantalla en vez de cerrarse; lo que recuperas de la Papelera no se vuelve a borrar, y una nota movida o renombrada a un nombre que el otro lado había borrado se queda.
- *Transferir archivos* muestra arriba el estado («Al día con «PC» (14:32): 2 recibidos») y *Sincronizar ahora*. Comparar y elegir archivos a mano sigue igual.
- Ojo: quien tenga el emparejamiento puede instalar plugins en el otro dispositivo. Si alguien más vio el código, usa *Cambiar el código* en el computador.

### 🖼 Las imágenes nuevas van a la carpeta «imagenes» (v2.19)
- Toda imagen nueva que pegues, arrastres, adjuntes o saques con la cámara del celular queda en la carpeta **`imagenes`** de la bóveda (se crea sola), sin configurar nada en Obsidian. Viene encendido.
- Solo imágenes (PNG, JPG, GIF, WEBP, SVG, HEIC…): un PDF o un audio adjunto siguen yendo donde diga Obsidian en Ajustes → *Archivos y enlaces*.
- Las imágenes que ya tenías no se mueven, y los enlaces a las nuevas funcionan igual (`![[Pasted image….png]]`).
- Se apaga, o se cambia el nombre de la carpeta, en Ajustes → *Acceso y apariencia* → *Imágenes nuevas*.

### 🗂 Buscar archivos ordenados por carpeta, en todos los buscadores (v2.17–v2.18)
El buscador de Obsidian muestra una lista plana con archivos de todas las carpetas mezclados. Este los muestra como el explorador: carpeta → subcarpeta → archivo, en orden alfabético natural (Clase 2 antes que Clase 10), con el número de archivos que calzan en cada carpeta y lo buscado resaltado.
- Busca en los nombres de archivos **y de carpetas**, sin importar tildes: «calculo pdf» encuentra los PDF que están dentro de Cálculo. Con «Dentro de las notas» busca también en el texto y muestra la línea donde aparece.
- Filtro por tipo: Todo, Notas, Documentos, Imágenes u Otros (se recuerda). Sin escribir nada muestra tus archivos recientes y todas las carpetas plegadas; una carpeta se abre o se cierra con un toque.
- Si lo que escribiste no existe, la última fila (o Mayús + Enter) crea esa nota, como «Abrir rápido».
- **Está en todos los buscadores de archivos:**
  - **«Abrir rápido» de Obsidian (Ctrl + O)** y **«Buscar en todos los archivos» (Ctrl + Shift + F)** abren este buscador; el segundo, con «Dentro de las notas» marcado y lo que tengas seleccionado. Los atajos son los mismos. Se devuelven al de Obsidian en Ajustes → *Acceso y apariencia* (o al desactivar el plugin).
  - **Pestaña «Buscar por carpetas»** en la barra lateral, al lado de Archivos y Buscar; en el celular, una pestaña más del menú izquierdo. Se pone sola la primera vez; si la cierras, vuelve con Ajustes → *Mostrarla* o el comando *Buscar archivos: pestaña en la barra lateral*.
  - En el celular, la **lupa al lado del botón naranja** (pantalla completa).
  - Los selectores del plugin: «Elige un libro o documento…» (mapa, prueba, resumen, chat, Cambiar) y la nota para sacar tarjetas en Repaso de ramos.
- Lo que Obsidian sigue mostrando a su manera: la pestaña «Buscar» propia de Obsidian (que conserva filtros como `tag:` o `path:`; un clic en una etiqueta la sigue usando) y las sugerencias al escribir `[[`.
- El centro de funciones muestra la versión instalada (por ejemplo «v2.18.0»). **Después de reemplazar los archivos del plugin hay que reiniciar Obsidian** (o desactivarlo y activarlo): si no, sigue corriendo la versión anterior.

### 🟧 Botón naranja, centro de funciones y demos «?» (v2.16)
- **Botón naranja** al pie de la barra lateral izquierda (en el celular, la que aparece al deslizar desde el borde izquierdo). Dice cuántas cartas tienes para repasar hoy y abre el centro de funciones. Por defecto se ve en el celular y la tablet; en Ajustes → *Acceso y apariencia* se puede ver también en el computador o esconder.
- **Centro de funciones**: una hoja a pantalla completa (no es una nota) con todas las funciones como tarjetas, en seis grupos: Gemini y documentos, Clases, Inglés, Repaso de ramos, Archivos y Herramientas. Cada grupo lleva un color sobrio, solo en el ícono, y el resto es neutro. Tiene buscador (sin importar tildes; Enter abre la primera), botones para saltar a un grupo y lo pendiente sobre el ícono (cartas para repasar, errores, fragmentos sin transcribir). Se cierra con ✕ o con el botón Atrás. También lo abren el ícono de la grilla de la barra lateral (con clic derecho sale el menú rápido de antes) y el comando *Centro de funciones*.
- **Demos «?»**: un «?» pequeño dentro de cada función y en cada tarjeta del centro. Recorre la función paso a paso: oscurece la pantalla, resalta la parte real (un campo, un botón, una lista) y explica para qué sirve.
  - Dónde está: al lado del título en cada sección de Inglés y de Repaso de ramos, en Transferir, Cuota de hoy y Registro; en la cabecera del panel Gemini (la demo cambia según la pestaña: chat, mapa, prueba, resumen o documentos), en la barra del visor y del mapa mental, en el panel de voz, en Gemini Voice Chat, en Grabar clase y en el buscador de los ajustes.
  - Se adapta a lo que hay en pantalla: en un repaso en curso muestra la carta y las respuestas; antes de empezar, cómo empezar y qué viene después.
  - Si la función necesita un documento y no hay uno abierto, la demo se cuenta sin resaltar y al final ofrece elegir uno.
  - Anterior y Siguiente (o las flechas del teclado); se sale con ✕, Esc, Atrás o tocando fuera. Comando: *Demo: cómo se usa lo que tengo abierto*. Se apagan en Ajustes → *Botones «?» con demos*.
- En el panel Gemini del celular, «Documentos trabajados» queda solo con 🗂, para que se lea el nombre del libro.

### 🇬🇧 Inglés: una sección aparte para aprender (v2.9, reordenada en v2.10)
Menú rápido → *Inglés* (o comando *Inglés: abrir la sección*). Trae al plugin lo que hacía `vocabulario_maestro.py`, enfocado en inglés, más escritura y las imágenes de palabra clave.

**Todo se guarda** en la bóveda, en `Visor + Gemini/Inglés/` (`datos-ingles.json`, `imagenes/`, `audio/`): mazos, cartas, avance del repaso, historiales, conversaciones y hasta el borrador de escritura. No va en la carpeta del plugin, así que no se pierde al actualizarlo. Antes de la primera escritura de cada sesión queda un respaldo (`datos-ingles.respaldo.json`); si el archivo se daña, se carga solo.

| Sección | Qué hace |
|---|---|
| **Inicio** | Cartas para repasar hoy, racha, avance por nivel CEFR (A1 a C2) y actividad de 14 días. |
| **Repasar** | Repaso espaciado (SM-2) con cuatro respuestas; cada botón dice cuándo vuelve la carta. Tres modos: ver la palabra, ver el significado o escucharla. Teclado: Espacio y 1 a 4. El día cambia a las 4 am. |
| **Mazos y cartas** | Los mazos (crear, renombrar, activar, borrar, exportar para Anki o como nota), **todas sus cartas** con filtros por mazo, nivel y estado, y el **buscador**: busca por palabra, traducción, definición o ejemplo (sin tildes). Si la palabra no está en tus cartas, responde el **diccionario en línea** (definición, pronunciación y audio, sin gastar IA) con un botón para agregarla. |
| **Agregar palabras** | Pega una lista (también en español: busca su equivalente). Dice antes cuántas peticiones cuesta. Abajo está el **dado** 🎲: X palabras al azar para un nivel CEFR y un tema opcional, sin repetir las que ya tienes; eliges cuáles se vuelven cartas. |
| **Practicar con la IA** | Conversación, quiz o juego de rol con las palabras que más te cuestan; corrige cada mensaje y marca las palabras que ya usaste. También escribe un diálogo con tus palabras. |
| **Completar la oración** | Cloze: falta una palabra de tu mazo; acepta sus formas (cooked, cooking) y explica por qué era esa. |
| **Pronunciación** | Grabas, Gemini escucha y da un puntaje de 0 a 100 con el sonido a corregir. |
| **Dictado** | Escuchas una frase y la escribes; marca palabra por palabra. |
| **Reading** | Texto de tu nivel con cronómetro y palabras por minuto, «¿qué entendiste?», cinco verdadero/falso, historial y análisis. Tocas las palabras que no conoces y van al mazo. |
| **Writing** | Consigna por tipo y nivel (o tema libre), editor con conteo y borrador que no se pierde; la corrección muestra tu texto con los cambios, cada error explicado, puntaje por criterio y nivel estimado. |

**La carta** tiene pronunciación (IPA y audio), tipo, nivel, definición en inglés, traducción, dos ejemplos traducidos, nota de uso y palabras parecidas. Cómo se arma:
1. **Diccionarios** (gratis, sin key): Free Dictionary, WordNet (por Datamuse) y Wiktionary. De ahí sale la **garantía**: A dos fuentes coinciden, B una la registra, C ninguna (queda estudiable), D una contradice a la IA en categoría o pronunciación.
2. **La IA escribe la ficha** (modelo principal; hasta 12 palabras por petición).
3. **Cruce automático**: otro modelo la revisa y corrige solo (Mistral si hay key; si no, Gemma). Nunca el mismo que la escribió. Si una carta quedó sin revisar (el revisor falló o no había cuota), se revisa sola en segundo plano mientras la sección está abierta: una petición por cada 12 cartas, hasta 3 intentos por carta. En *Mazos y cartas* se ve cuántas quedaron de acuerdo, corregidas o en duda, y un clic las filtra. Se apaga en Ajustes → Inglés.

**Diccionarios en línea**: además de la consulta integrada, puedes agregar los tuyos (Nombre + dirección con `{palabra}` donde va la palabra). Vienen Cambridge y WordReference. Aparecen como botones en el buscador y en cada carta, y abren la palabra en tu navegador. Se agregan desde el buscador (*+ Agregar diccionario*) o en Ajustes → Inglés.

Un número donde iba texto no entra como definición ni traducción (el defecto que tenía el script).

**Imagen con el método de la palabra clave**: en cada carta, *Generar imagen con palabra clave* busca una palabra en español que suene parecido a cómo se pronuncia la inglesa, arma una escena que la une con el significado y la dibuja. Después: *Otra imagen* (misma escena), *Otra palabra clave* (no repite las ya probadas), *Escribirla yo* o *Pegar imagen*. Si el dibujo falla, la palabra clave y la escena igual quedan guardadas.
- Los modelos de imagen de Gemini no tienen plan gratis, por eso se prueban en orden: **Pollinations** (gratis, sin key; puede limitar o pedir pago), **AI Horde** (gratis, con cola de espera) y un **dibujo simple hecho por la IA de texto** (siempre disponible, gasta una petición). Se elige en ajustes.

**Audio**: grabación del diccionario si existe (queda guardada), si no la voz de Google (la misma de gTTS) y, si no hay internet, la voz del sistema.

**Cuánto gasta**: crear cartas, 2 peticiones por cada 12 palabras; palabra clave, 1 petición chica. Chat, cloze, lectura, dictado y consignas son llamadas chicas (van a Gemma 4). Escritura y pronunciación usan el modelo principal.

### ⚡ Todo a mano, colores sobrios y buscador de ajustes (v2.15)
- **Menú rápido.** Un solo ícono nuevo en la barra lateral (la grilla) o el comando *Menú rápido: todas las secciones del plugin*. Lleva a Inglés, Repaso de ramos, Banco de errores, Transferir, Papelera, Grabar una clase, Chat/mapa/prueba/resumen, Cuota de hoy y Ajustes, y muestra cuánto tienes pendiente para repasar.
- **Menos íconos.** Los íconos propios de Inglés, Repaso de ramos y Transferir quedan apagados; se prenden en Ajustes → *Acceso y apariencia* → *Un ícono por sección*.
- **De una sección a otra.** Al pie de la navegación de Inglés y de Repaso de ramos hay enlaces directos a las otras secciones.
- **Un color sobrio por menú.** Cada menú conserva su color, pero apagado y de a uno: solo el título (una línea fina), el ítem activo y los botones de esa sección lo llevan. La navegación ya no muestra los diez colores juntos. Verde y rojo de acierto/error también son más suaves. Para usar los colores de tu tema: Ajustes → *Colores de las secciones* → *Los del tema de Obsidian*.
- **Textos cortos.** Subtítulos y ayudas de Inglés, Repaso de ramos, Transferir y sus ajustes quedaron en una línea.
- **Buscador en los ajustes.** Arriba de los ajustes del plugin: escribe (sin importar tildes ni mayúsculas) y quedan solo los ajustes que calzan; si calza el título de una sección, se ve la sección completa. `Esc` limpia.
- **Arreglos (revisión completa de lo nuevo).** Para Transferir hay que **actualizar el plugin en los dos dispositivos**: una versión anterior y esta no se entienden, y lo dicen con un mensaje.
  - *Transferir.* Cada respuesta del computador va atada a un número al azar que elige quien pide, así que una respuesta grabada antes en la red no sirve de nada. Se rechazan los nombres cortos de Windows (`OBSIDI~1` es otra forma de escribir `.obsidian`) y los nombres con caracteres invisibles. Si falla la escritura de un archivo, la versión anterior vuelve a su lugar. Si la conexión se corta a mitad de un archivo, se copia de nuevo desde el comienzo (antes podía quedar mezclado). La papelera ya no pierde archivos de vista si se usa mientras llega una copia, y se limpia sola a los 30 días aunque no se abra. Mientras copia, lo único que se puede tocar es *Cancelar*; después de cancelar hay que comparar de nuevo. «Listo: N archivos» cuenta solo lo copiado.
  - *Repaso de ramos.* Dos preguntas que se diferencian en un signo (`$x > 0$` y `$x < 0$`) ya no se toman por la misma. *Responder de nuevo* no duplica las cartas si renombraste el ramo. Repetir una prueba el mismo día no estira los intervalos. Las respuestas escritas se corrigen con más cuidado: `(a+b)^2` no es `a+b^2` y `≠` no es `=`. Fallar una pregunta de completar y salir por el menú la deja anotada. Enter sobre un botón enfocado aprieta ese botón. Las tarjetas pedidas a la IA no se pierden si sigues usando la sección mientras llegan. El menú rápido no bota la prueba que estás respondiendo. Responder una prueba no gasta las «preguntas nuevas por día».
  - *Otros.* Renombrar un archivo ya no lo deja marcado como borrado. Íconos que no aparecían en versiones antiguas de Obsidian tienen reemplazo. El buscador de ajustes encuentra también los bloques de Gemini Voice (por ejemplo «pool») y deja a la vista el resultado de *Probar*.

### 🎓 Repaso de ramos y banco de errores (v2.14)
Menú rápido → *Repaso de ramos* (o el comando *Repaso de ramos: abrir*). Usa el mismo repaso espaciado de la sección de inglés, ahora para tus ramos.

- **Las pruebas se responden.** Antes una prueba era solo una nota; ahora: clic derecho en la nota → *Responder esta prueba* (o desde *Agregar*). Sale pregunta por pregunta: selección múltiple (con las opciones barajadas), verdadero o falso, completar y desarrollo. Al final, tu puntaje. Sirve también para las pruebas que ya tenías. **No gasta IA.**
- **Cada pregunta queda como carta** de su ramo (lo propone según la carpeta del documento) y vuelve cuando toca: lo acertado al día siguiente, a los 3 días, y cada vez más lejos; lo fallado, a los 10 minutos.
- **Banco de errores.** Lo que fallas queda guardado y sale del banco al acertarlo **2 veces seguidas**. *Practicar mis errores* se puede repetir cuanto quieras: no mueve las fechas del repaso.
- **Tarjetas con IA desde una nota** (resumen, clase transcrita, apuntes): definiciones, teoremas y fórmulas como pregunta y respuesta, con LaTeX. Una petición chica por nota (va a Gemma si cabe); tú eliges cuáles entran. Clic derecho en la nota → *Sacar tarjetas de repaso con la IA*.
- **Tarjetas a mano**, y edición de cualquier carta (pregunta, opciones, respuesta, ramo).
- **Completar**: acepta mayúsculas, tildes y los signos `$`. Si escribiste una fórmula equivalente y no calzó, *Mi respuesta estaba bien* la cuenta como acierto. **Desarrollo**: ves la pauta y te calificas tú (No la sabía / A medias / La sabía).
- Teclado: `a`-`d` o `1`-`4` eligen opción, `v`/`f` en verdadero o falso, Enter pasa a la siguiente.
- Todo se guarda en la bóveda (`Visor + Gemini/Estudio/datos-estudio.json`, con respaldo), así que viaja con *Transferir archivos*. Ajuste: preguntas nuevas por día (15).

### 🗑️ Borrar en un lado no borra en el otro, y hay papelera (v2.13)
- **Los borrados no se propagan** al transferir a mano. (Desde la v2.20, «Sincronizar solo» con «Borrar también en el otro lado» sí los propaga, a la Papelera del otro lado; ver arriba.)
- **Tampoco vuelven solos.** El plugin anota lo que borras o renombras en cada dispositivo. Al comparar, esos archivos salen aparte («Borrados aquí, siguen en el computador» / «Borrados en el computador, siguen aquí»), **sin marcar**: si fue un accidente, los marcas y los traes de vuelta; si fue a propósito, los dejas así. Si el otro lado modificó el archivo después de que lo borraste, se ofrece como archivo nuevo.
- **Papelera** (pestaña en *Transferir archivos*, o comando *Papelera: recuperar archivos reemplazados o borrados*):
  - *Reemplazados por una transferencia*: cuando llega una versión más nueva, la anterior se guarda 30 días con su ruta original. **Recuperar** la devuelve a su lugar o, si ya hay otro archivo ahí, como «nombre (recuperado)»; nunca pisa nada. Si no se puede guardar la versión anterior, el archivo no se reemplaza.
  - *Borrados en Obsidian en este dispositivo*: lo que Obsidian guardó en su papelera (`.trash`), con **Recuperar** a la carpeta de donde se borró. Si Obsidian está mandando lo borrado a la papelera del sistema, se recupera desde ahí; si está borrando para siempre, la ventana lo avisa y ofrece cambiarlo.
- Cada dispositivo tiene su propia papelera (carpeta oculta `.visor-papelera` de la bóveda); no se transfiere.
- Límite: solo se anota lo que borras **dentro de Obsidian**. Un archivo borrado desde el explorador de archivos con Obsidian cerrado se ofrece para traer como cualquier archivo que falta.

### 📲 Transferir archivos entre el celular y el computador (v2.12)
Sin Syncthing, sin nube y sin cuentas. Menú rápido → *Transferir archivos*, o el comando *Transferir archivos entre el celular y el computador*.

**Cómo se usa**
1. En el computador: *Transferir archivos* → **Empezar a recibir**. Muestra una dirección (por ejemplo `192.168.1.23:47800`) y un código de 12 caracteres.
2. En el celular: *Transferir archivos*, escribe la dirección y, solo la primera vez, el código.
3. **Comparar** muestra qué falta o cambió en cada lado (toda la bóveda o una carpeta) sin copiar nada. Después **Traer**, **Mandar** o **Hacer las dos cosas**; se pueden desmarcar archivos.

Gana el archivo más nuevo. **Nada se borra**: si un archivo reemplaza a otro, el anterior queda en la Papelera del plugin (ver v2.13). Dos archivos del mismo tamaño y distinta fecha se comparan por contenido, para no copiar lo que ya es igual. Los archivos conservan su fecha. Hasta la v2.19 se hacía solo cuando tú lo pedías; desde la v2.20, con «Sincronizar solo», va solo y también propaga borrados (ver arriba). Tope: 400 MB por archivo.

**Seguridad (pensada también para redes públicas)**
- Todo viaja cifrado y firmado (AES-256-GCM) con una clave que sale del código (PBKDF2). Quien esté en la misma red no puede leer nombres ni contenido, ni alterar o repetir una petición.
- Sin el código, el computador solo responde un saludo con un número al azar. No sirve archivos ni páginas.
- Lo que empieza con punto nunca se lista, se lee ni se escribe, salvo los plugins (`.obsidian/plugins`) con «Incluir los plugins» (v2.20). Los ajustes de Visor + Gemini (tus API keys y el emparejamiento) nunca. Tampoco se puede salir de la bóveda.
- Desde la v2.20 el computador recibe todo el día mientras Obsidian esté abierto («Recibir siempre», se apaga en Ajustes); sin eso, se apaga solo a los 20 minutos sin uso. 20 intentos fallidos bloquean esa dirección por 5 minutos.
- El celular guarda la clave derivada, no el código. **Cambiar el código** en el computador desempareja todo.

**Si no conecta**
- Windows pregunta la primera vez si Obsidian puede recibir conexiones: acepta (también para redes públicas, si estás en una).
- Muchas redes públicas (universidad, cafés) no dejan que dos aparatos se hablen entre sí. En ese caso comparte internet desde el celular y conecta el computador a esa red: funciona igual y la red es tuya.
- El computador es el que recibe y el celular el que se conecta; al revés no se puede (un plugin en el celular no puede recibir conexiones). Entre dos computadores también funciona.

### 🎨 Colores en la sección de inglés (v2.11, reemplazados por la paleta sobria de la v2.15)
Cada parte tiene su color, como una caja de plumones: Inicio naranja, Repasar amarillo, Mazos turquesa, Agregar verde lima, Practicar con la IA rosado, Completar la oración violeta, Pronunciación coral, Dictado azul, Reading celeste y Writing lila. El color de la sección tiñe su título (subrayado con plumón), sus botones, casillas y barras; la navegación muestra los diez. Además: lo de hoy en un bloque de color, mazos con lomo de color como carpetas, niveles CEFR en fichas de color lleno, cartas sin imagen con su inicial, y las cuatro respuestas del repaso como teclas de color. Funciona en tema claro y oscuro, y el texto sobre color siempre va con contraste suficiente. Para volver a los colores de tu tema: Ajustes → Inglés → *Colores de la sección* → *Del tema de Obsidian*.

### ⌨️ Arreglo: no se podía escribir en varios campos (v2.10)
En la 2.9 no se podía escribir en el tópico de **Reading**, la respuesta de **Completar la oración**, el **Dictado**, el nombre de un **mazo nuevo** ni al renombrar un mazo: el manejador de la tecla Enter descartaba todas las demás teclas. Arreglado en todos, y ahora hay una prueba que escribe con teclado real en cada campo. De paso: las teclas de *Repasar* (Espacio, 1 a 4) ya no quedan activas en otras secciones.

### 🚦 Mistral: de a una petición por segundo (v2.9.1)
El plan gratis de Mistral limita las **peticiones por segundo** (y los tokens por minuto y por mes) para toda la cuenta. Si se pasa, responde `429 Rate limit exceeded`.
- **Probar Mistral** ahora prueba los modelos **de a uno y con pausa** (antes salían juntos, con la misma key). Si igual responde 429, espera 3 s y reintenta una vez: si funciona, era el tope por segundo; si no, la cuenta no tiene cupo y se muestra **qué límite saltó** (leyendo las cabeceras de la respuesta) y qué revisar en console.mistral.ai → Limits.
- En los trabajos, las peticiones a Mistral salen con al menos 1,25 s entre una y otra. Un 429 suelto hace una pausa corta, se reintenta y se dejan más separadas las siguientes; al segundo seguido ese modelo se deja 2,5 minutos y el error dice por qué.
- Si Gemini ya no tiene cuota y Mistral tampoco puede, el mensaje dice las dos cosas (y a qué hora vuelve Gemini).

### 🔧 Probar las keys ya no se queda cargando (v2.9)
- Los botones **Probar** (Gemini y Mistral) mandan una petición corta y directa por key y modelo, con plazo de 20 s, y muestran bajo el botón qué funciona y por qué falla lo que falla (cuota del día, tope por minuto, key inválida, sin conexión).
- Antes, si Mistral contestaba «sin capacidad» (pasa en su plan gratis) o no contestaba, la prueba esperaba varios minutos sin decir nada. Ahora ninguna llamada espera en silencio: hay aviso en pantalla y un tope de 90 s de espera por llamada.
- Mistral: si el navegador deja colgada la conexión, a los 15 s se pide por otra vía (sin streaming).

### 🔋 Cuota: que las keys duren (v2.8)
El plan gratis de Gemini no se acaba por tokens sino por **peticiones al día**, y ese tope es **por modelo y por proyecto** (dos keys del mismo proyecto comparten cuota). Los topes aproximados por key: Flash ~20 al día, Flash-Lite ~500, Gemma 4 ~14.400 (pero solo 16 mil tokens por minuto). Los de tu cuenta se ven en AI Studio.

- **Modo ahorro** (encendido por defecto): cada mapa, prueba o resumen se parte **por tamaño** (hasta ~40 páginas por petición), no por cantidad de keys. Con 3 keys:

  | Trabajo | Antes (2.7) | Ahora |
  |---|---|---|
  | Resumen o mapa de 10 páginas | 7 peticiones | **1** |
  | Resumen o mapa de 100 páginas | 7 peticiones | **3** + 1 chica a Gemma |
  | Prueba de 15 preguntas, 10 páginas | 6 (las mismas páginas a 5 redactores) | **1** |
  | OCR de 100 páginas | 34 | **13** |

  Como cada parte cubre más páginas, su tope de palabras crece en proporción (el resumen "Completo" no se acorta). Se apaga en ajustes si prefieres velocidad.
- **Modelo principal `gemini-3.1-flash-lite`** (~500 al día por key) con respaldos `gemini-3.5-flash-lite`, `gemini-3-flash-preview` y `gemini-2.5-flash`. Tus ajustes guardados se cambian solos una vez al actualizar.
- **Cuota por key y modelo**: si una key avisa que agotó **el día** de un modelo, no se le vuelve a pedir ese modelo hasta el reinicio, pero sigue trabajando con los demás; las otras keys siguen con el principal. Si el aviso es el **tope por minuto**, se espera cuando falta poco (hasta 25 s) o se usa el siguiente modelo. Ya no hay reintentos a ciegas ni keys "descansando" con cuota disponible. Si no queda nada, el error dice a qué hora vuelve.
- **Llamadas chicas a Gemma 4** (`gemma-4-31b-it`, cuota aparte): el chat con el libro, unir las partes de mapas/pruebas/resúmenes, la memoria del chat y "Explicar a fondo". Si la petición es grande para Gemma, lleva imágenes, o Gemma falla, va sola al modelo principal. Debajo de cada respuesta del chat se ve qué modelo contestó.
- **Batería 🔋 con la hora del reinicio**: en la barra de estado (abajo), bajo las pestañas del panel 🧠 (ahí la ves en el celular) y en ajustes. Muestra cuánto queda hoy en el modelo principal y sus respaldos sumando todas las keys, y a qué hora se reinicia (medianoche del Pacífico = 04:00 o 05:00 en Chile según la época). Un clic abre el detalle por key y modelo. Comando: *Ver la cuota de hoy*.
  Los contadores son de este dispositivo y los topes son estimados: se corrigen solos con el primer aviso de Google, o los fijas en *Límites diarios por modelo*.
- **Mistral de respaldo** (opcional): Ajustes → *API key de Mistral* (se saca en console.mistral.ai, plan gratis "Experiment"; también se lee de `api_keys.json`: `{"mistral": "..."}`). Cuando Gemini se queda sin cuota, mapas, pruebas, resúmenes y chat siguen con Mistral (`mistral-medium-latest`, luego `mistral-small-latest`). Opción *Primero en trabajos grandes* si prefieres gastar Mistral antes. Solo texto: OCR, voz y transcripción siguen con Gemini. Si el navegador bloquea el streaming, se pide sin streaming (la respuesta llega entera). En el plan gratis de Mistral tus textos pueden usarse para entrenar sus modelos.
- **Peticiones simultáneas por key: 3.** Con el modo ahorro ya no decide en cuántos pedazos se parte el trabajo, solo cuántos corren a la vez.

### 🆓 Transcripción gratis y sin internet (v2.7)
- Por defecto las clases se transcriben **en tu propio dispositivo**: gratis, sin internet y sin límite de horas (sirve para jornadas de 6 a 8 horas). Motor **sherpa-onnx** (libre) en WebAssembly: el mismo en el computador y en el celular, sin instalar programas.
- Se instala **una vez con un botón** (en *Grabar clase* o en Ajustes → 🎙 Grabar clases). Descarga, verifica la huella de lo descargado, descomprime y prueba el motor:
  - **Preciso** — Parakeet v3 de NVIDIA, ~490 MB. Recomendado en el computador (en el celular solo con 8 GB de RAM o más). Español con puntuación y números ("página 15").
  - **Liviano** — Moonshine en español, ~51 MB. Recomendado en el celular. Licencia de uso personal, no comercial.
- En el computador el modelo se guarda **fuera de la bóveda** (`~/.visor-gemini`), así no se sincroniza al teléfono.
- **Cada dispositivo elige** cómo transcribir: *Gratis en este dispositivo*, *Gemini* (agrega títulos por tema, gasta ~2 mil tokens por minuto) u *Otro dispositivo*: grabas en el celular y **el computador lo transcribe** cuando la bóveda se sincroniza (busca solo los fragmentos pendientes en las notas).
- Velocidad (1 núcleo): el Preciso tarda ~0,4× lo que dura el audio. Mientras grabas va al día; 8 horas grabadas en el celular se transcriben en ~3 horas de fondo en el computador.

### 🎙 Voz: arreglos (v2.7)
- **"Ve a la página quince"** ya no termina en la página 1: se entienden números en cifras, en palabras y dichos cifra por cifra ("uno cinco"); si Gemini pide otra página que la que dijiste, manda lo que dijiste; si no entiende el número, te pregunta.
- **Sin audífonos**: el micrófono se silencia mientras suena Gemini con un margen según la latencia real del parlante, y el botón **✋** la corta al tiro para que hables tú.

### ⏺ Grabar clase (v2.6, pensado para el celular)
- Botón **⏺** de la barra lateral (o **● Grabar** en el panel 🧠, o el comando *Grabar clase*): abre el **modo grabación** a pantalla completa. Escribe la asignatura (opcional) y toca el botón rojo.
- **Solo la voz del profesor, lo más limpia posible**: reducción de ruido del sistema + filtros de voz (fuera zumbidos de aire/proyector y siseo) + volumen parejo aunque se aleje. Gemini transcribe la voz principal e ignora conversaciones de fondo; las preguntas audibles de compañeros quedan como **Estudiante:**.
- **Audio liviano**: Opus mono a 16 kbps ≈ 7 MB por hora (ajustable). Una clase de 90 minutos ≈ 11 MB.
- **Se transcribe mientras grabas** (gratis, ver arriba), por fragmentos de 30 s a 1 min que se cortan **en las pausas** (nunca a mitad de palabra). La nota queda así:
  ```
  ## 12:30 · Flujo a través de una esfera
  Lo que dijo el profesor en ese minuto (fórmulas en LaTeX)…
  ![[…/012.webm]]   ← el audio exacto de ese texto
  ```
  Buscas una frase (buscador de Obsidian o el chat del 🧠) y escuchas justo dónde se dijo para corroborar.
- **⭐ Marcar**: “esto entra en la prueba” → ese fragmento queda con ⭐ en la nota.
- **Pantalla negra**: sigue grabando con la pantalla en negro (en OLED casi no gasta batería); toca para volver. La pantalla se mantiene encendida sola.
- **Sin internet no se pierde nada**: el audio se guarda igual y la transcripción queda en cola; se hace sola cuando vuelve la conexión (aunque hayas cerrado Obsidian). Comando: *Transcribir lo pendiente*.
- Si el micrófono se corta (llamada, otra app), la grabación sigue sola al volver; si hubo un hueco, la nota lo avisa.
- Arriba de la nota: **▶ Escuchar la clase completa** (fragmento tras fragmento, ⏮ ⏭, velocidad 1× a 2×).
- Si tienes el PDF de la clase abierto, cada fragmento anota **la página que estabas mirando**.
- Al terminar: **🧠 Chat, mapa, prueba o resumen de la clase** (la transcripción es una nota más).
- Se guarda en `Visor + Gemini/Clases/<Asignatura>/`.

### 🧠 Todo en un botón (v2.5)
- El **🧠 de la barra lateral izquierda** abre el panel **Gemini** a la derecha, con el documento abierto: **Chat · Mapa mental · Prueba · Resumen · Voz**. Si no hay documento abierto, pide elegir uno.
- Las páginas para mapa, prueba o resumen se eligen **dentro del panel** (ya no debajo del libro); el ＋ de cada página sigue funcionando. Lo elegido se guarda al cambiar de pestaña o de libro.
- Los botones de la barra del documento y de las notas quedan ocultos. Para verlos: Ajustes → *Botones de IA también en la barra del documento*, o ⋮ del panel.
- Clic derecho en el 🧠: el menú de antes.

### Visor
- **Abre los PDF por defecto** (reemplaza al visor nativo; al desactivar el plugin vuelve el nativo). Se puede apagar en ajustes.
- **Todas las páginas seguidas** con scroll continuo en PDF, DjVu y EPUB (Word, planillas y texto ya eran continuos). Solo se dibujan las páginas cercanas a la pantalla, así que libros de cientos de páginas no se comen la memoria.
- PDF con **texto seleccionable** (capa de texto), buscador con `Ctrl F`, zoom, recordar página.
- **Miniaturas** a la izquierda (PDF, DjVu; lista de capítulos en EPUB): clic para saltar, la actual resaltada, las elegidas con ✓. Botón ▯ de la barra para mostrar/ocultar.
- Los enlaces `[[libro.pdf#page=42]]` abren el libro en esa página.

### Botón de Gemini (arriba a la derecha de cada documento)
Usa **el mismo flujo de audio que Gemini Voice Chat** (micrófono al conectar, audio sin cortes aunque llegue una "interrupción" por eco, vúmetro liviano).
Al pulsarlo aparece en la barra superior un **vúmetro** que se mueve con tu voz (verde) y con la voz de Gemini (violeta), más un panel con la conversación.

- Si el documento **tiene texto seleccionable**, Gemini dice: *"¿Cuáles páginas o temas del libro quieres que trabajemos?"*
- Si **no lo tiene** (escaneo sin OCR), dice: *"No se detectó texto seleccionable en el libro, por lo que no puedo explicarte páginas de este"*.

Con texto, Gemini tiene herramientas para trabajar el libro:

| Herramienta | Para qué |
|---|---|
| leer_paginas | Lee rangos de páginas antes de explicar (no inventa) |
| buscar_en_documento | Encuentra en qué páginas aparece un tema |
| obtener_indice | Usa el índice del PDF/EPUB para ubicar capítulos |
| resaltar_texto / ir_a_pagina | Te muestra y resalta el pasaje que está explicando |
| leer_seleccion | "Explícame esto" sobre lo que seleccionaste |
| crear_nota | Resúmenes, glosarios, ejercicios… en la carpeta de trabajos del libro |
| generar_mapa_mental / generar_prueba | Lo mismo que el menú ✨, por voz |

Siempre cita la página ("esto está en la página 42"); en el panel esas citas son enlaces.
Atajo: `Ctrl Shift G`. Para terminar: botón ■, o decirle "chao".

### 💬 Chat con el libro (ahorro de tokens)
Botón **Chat** en la barra del libro (o comando *Chatear con el libro abierto*). Panel a la derecha.

- **Se indexa una vez** y queda guardado en `.obsidian/plugins/visor-gemini/indices/`: texto compactado (sin encabezados/pies repetidos ni guiones de corte), fragmentos por página, búsqueda por **palabras clave (BM25, local y gratis)** y por **significado (embeddings de Gemini, cuota aparte, en segundo plano y reanudable)**.
- **Cada pregunta manda solo lo relevante** con un tope (por defecto ~6000 tokens de libro ≈ 8 páginas). En un libro de 300 páginas, ~2 % de lo que costaría mandarlo entero.
- Entiende "página 40", "páginas 10 a 12", "esta página", "lo que seleccioné" y "capítulo 3" (usando el índice del PDF).
- Memoria: los últimos 6 mensajes van textuales y lo anterior se resume con un modelo liviano.
- Citas [p. N] enlazadas; debajo de cada respuesta, páginas consultadas y tokens gastados.
- **🗂 Documentos trabajados** (botón arriba en el chat, o comando): lista todos los documentos que trabajaste; al abrir uno aparecen sus resúmenes, mapas mentales, pruebas, chats y notas. Buscador, "Abrir documento", "Chatear" y "Carpeta". Si hay archivos del plugin en otras carpetas (versiones anteriores), ofrece traerlos.
- **📄 Crear resumen general**: escribe una **nota** `Resumen - <libro> - <fecha>` en la carpeta de trabajos (todas las keys a la vez, y al final se hila con introducción, puentes entre secciones, ideas clave y cierre). Se abre al lado del libro y el chat también la usa para preguntas del tipo "de qué trata el libro". Se puede cancelar.
- Las respuestas se dibujan como Markdown con fórmulas **mientras llegan** (nada de `$\mathbf{F}$` crudo). **■ Detener** corta una respuesta a mitad.
- El cuadro de texto y **Enviar** quedan por encima de la barra de estado de Obsidian.
- La voz también lo usa (herramienta `buscar_fragmentos_relevantes`).

### 🧠 Mapa mental, 📝 modo prueba y 📄 resumen
**Guía con demo:** ícono 🧠 de la barra lateral → *Guía y mapa de demostración* (también aparece una bienvenida la primera vez).

1. Abre un libro, o ícono 🧠 → *Mapa mental: elegir un libro…* (se abre en una pestaña).
2. Botón **Mapa mental** o **Prueba** en la barra del libro.
3. **Debajo del libro** aparece el panel del tipo elegido (solo dice *Mapa mental*, *Prueba* o *Resumen*; se cambia con los botones de la barra). Mientras bajas leyendo: **＋ Agregar página** (la visible; si ya está agregada aparece **− Quitar página**), **Rango desde–hasta**, o el **＋ Agregar página** en la esquina de cada página. Máximo 300.
4. **Generar**. El trabajo se reparte en *keys × peticiones por key* pedazos (con 3 keys: 6 a la vez, 2 por key) que se escriben **en paralelo**; las páginas se reparten por cantidad de texto, y con pocas páginas varios redactores se dividen el mismo tramo. Al final una llamada corta **hila** todo: la prueba queda en un orden con sentido, sin preguntas repetidas y con un solo título; el mapa se agrupa en ramas con un hilo; el resumen recibe introducción, puentes y cierre. La barra avanza con lo que Gemini va escribiendo (y mientras piensa). **✕ Cancelar** corta todas las partes al tiro. Si todo falla, reintenta con 150, 100 y 50 páginas. La nota se guarda en **Visor + Gemini/<documento>/** y se abre al lado del libro.
5. En esas notas, un clic en **p. N** abre el libro **a la izquierda** en esa página (si ya está abierto, solo salta de página).
6. **Resumen**: extensión *Completo (apuntes)* por defecto — cada concepto, fórmula y ejemplo desarrollado —, o *Normal* / *Breve*.

**En el mapa:**
- Fórmulas en LaTeX renderizadas con el MathJax de Obsidian (si alguna viene mal escrita, se muestra el código en vez de romperse).
- **Clic en un nodo** → panel inferior con explicación, cita textual, libro y página. **Arrastra sus bordes** (izquierdo, derecho, superior) para cambiar el tamaño.
- **✨ Explicar a fondo** → Gemini lee esa página del libro y la explica; queda guardado en la nota.
- **p.12 / Abrir y resaltar** → abre el libro al lado y resalta la cita.
- Círculo al costado → plegar/desplegar. **🎨** → color de fondo (por mapa o para todos).

### Gemini Voice Chat clásico
Sigue completo: ícono de micrófono en la barra lateral y `Ctrl Shift V`.

### 🗂 Panel derecho y notas .md (v2.3)
- **Lo generado se lee en el panel derecho** (el del plugin): mapas, resúmenes y pruebas se abren ahí, sin propiedades arriba, con botones para abrir el documento a la izquierda, recargar o abrir como nota para editar. Se desactiva en ajustes.
- **Notas .md con la barra del visor**: toda nota lleva arriba *Mapa mental · Prueba · Resumen · Chat · ✦ Gemini* y abajo el mismo panel de selección. En una nota, cada encabezado (#, ##, ###) es una **sección** (las cortas se juntan, las largas se parten). La nota se sigue editando con el editor de Obsidian. Los enlaces a secciones abren la nota a la izquierda en esa sección.
- **✨ Explicar a fondo** (mapa mental): la explicación aparece abajo mientras Gemini escribe, queda guardada en la misma nota (bloque `mapa-mental-explicaciones`, el JSON del mapa no se toca), el nodo se marca en dorado y no te saca de pantalla completa (si estás en pantalla completa se escribe al salir).

### 🎙 Voz, registro y OCR (v2.4)
- **Botón de modo voz** (micrófono con ondas + "Voz"); mientras la sesión está activa se llena de color y las ondas se mueven.
- **La voz responde más rápido y sin enredarse**: el asistente usa su propio VAD (300 ms de margen al empezar a hablar y 0,8 s de silencio para decidir que terminaste; ajustable: Rápido / Normal / Paciente), **anti-eco** (mientras Gemini habla no se manda tu micrófono, así su voz por los parlantes no la interrumpe; apágalo si usas audífonos), lecturas más cortas (6 páginas y ~20 mil caracteres por vez) y la herramienta *leer_pagina_visible* para "esta página".
- **📋 Registro (logs)**: comando *Ver registro*, botón en el panel de voz, en ⋮ del chat y en ajustes. Anota cada llamada a Gemini (modelo, key, tiempos, tokens), la sesión de voz paso a paso (conexión, cuándo empiezas y dejas de hablar, cuánto tarda Gemini en contestar, herramientas y su duración, transcripciones, cortes) y los errores. *Copiar todo* o *Guardar como nota* (`Visor + Gemini/_registros/`). Las API keys nunca aparecen.
- **🔍 OCR con Gemini** para PDF/DjVu escaneados: botón en el chat (aparece cuando el libro no tiene texto), en ⋮ del chat, en el menú ✨ o el comando *Reconocer texto del documento escaneado*. Gemini lee cada página como imagen (3 por petición, todas las keys a la vez), guarda el texto en la carpeta del plugin (`/ocr`) y desde ahí funcionan el chat, la voz, los mapas, las pruebas y los resúmenes. Se puede cancelar y retomar.
- **Fórmulas**: los blancos de *completar* (`____`) ya no van dentro de las fórmulas, se arreglan los `$` desparejos o con espacios, y el comando *Reparar fórmulas LaTeX de la nota abierta* (o la 🔧 del panel) corrige notas viejas.
- En el panel derecho, **"Ver respuesta" y "Pauta de corrección"** se despliegan con un clic.

## Carpeta de trabajos y base SQL
Todo lo que genera el plugin va a `Visor + Gemini/<documento>/` (en la raíz del vault; el nombre se cambia en ajustes). Cada archivo queda registrado en una base **SQLite** (sql.js, WebAssembly, incluido en `main.js`) guardada en `Visor + Gemini/.visor-gemini.sqlite`: tablas `documentos` y `trabajos`. La base sigue los renombres y borrados del vault, y si se pierde se reconstruye sola leyendo el frontmatter (`tipo` + `fuente`) de las notas.

## Ajustes importantes
- **Modelo principal**: `gemini-3.1-flash-lite` con respaldos `gemini-3.5-flash-lite, gemini-3-flash-preview, gemini-2.5-flash`. Botón "Probar" para verificar tus keys.
- **Modo ahorro**, **Límites diarios por modelo** y **Mistral**: ver "🔋 Cuota" arriba.
- **Razonamiento al generar**: "Mínimo" (lo más rápido), "Bajo" (por defecto) o "Normal".
- **Peticiones simultáneas por key**: 3 por defecto (todas las keys trabajan a la vez); bájalo si ves muchos avisos de tope por minuto.
- **Compresión de contexto en la voz**: permite sesiones largas. Si la sesión se cierra apenas conecta, apágala.

## Límites
- En el celular: deja **Obsidian abierto y la pantalla encendida** (o en negro) mientras grabas; si el teléfono se bloquea, el sistema pausa el micrófono (al volver sigue solo). En el celular los PDF los abre el visor de Obsidian.
- Ninguna app separa al 100 % la voz del profesor de otras voces cercanas: se reduce el ruido y Gemini transcribe la voz principal. Siéntate cerca.
- La transcripción gratis necesita memoria: el Preciso usa ~1,5 GB mientras trabaja (se libera solo a los 2 minutos sin uso). Con audio muy ruidoso (profesor lejos y sala bulliciosa) cualquier modelo falla: siéntate cerca.
- Con Gemini como motor, transcribir usa ~2 mil tokens por minuto de audio.
- Componentes descargados al instalar: sherpa-onnx (Apache 2.0), Parakeet v3 (CC-BY-4.0, NVIDIA), Moonshine español (Moonshine Community License, no comercial).
- Mapas mentales: la cita de un nodo solo aparece si está tal cual en el libro (si no, el botón abre la página igual).
- "Texto seleccionable" se detecta mirando hasta 14 páginas repartidas por el libro.
- La primera búsqueda por voz en un PDF enorme tarda (extrae el texto de cada página); después queda en memoria.
- DjVu.js es GPL v2, así que el plugin completo también.

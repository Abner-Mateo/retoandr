desarrollar una App en Android Studio (Java)
 Generador de Frases de Motivación
Descripción del objetivo: Desarrollar una aplicación móvil en Android Studio usando Java que muestre frases motivacionales al usuario cada vez que presione un botón. Las frases se obtendrán en tiempo real desde la API pública de Zen Quotes (https://zenquotes.io/api/random). El diseño debe ser simple, con una interfaz amigable que incluya un botón y un área de texto para mostrar la frase.
Objetivos técnicos:
- Consumir una API REST desde Android usando Retrofit.
- Parsear respuestas JSON para extraer frases.
- Mostrar la frase en pantalla con cada clic.
- (Opcional) Personalizar la frase con IA según el estado de ánimo del usuario.


Requisitos funcionales:
- Al iniciar la app, se muestra un botón que dice “¡Motívame!”.
- Al presionar el botón, se realiza una petición HTTP GET a la API de Zen Quotes.
- Se extrae la frase y el autor del JSON recibido.
- Se muestra la frase en un TextView de forma clara y estilizada.

Requisitos técnicos:
- Usar Retrofit para el consumo de la API.
- Usar Gson para el manejo de JSON.
- Permitir acceso a Internet en el AndroidManifest.xml.
- Crear una clase modelo (POJO) para mapear la respuesta JSON.
- Manejar errores de red y mostrar mensajes amigables.

utiliza las activitys que creas necesarias y wiew




MEJORAS IMPLEMENTADAS
Verificación de conexión a internet:
He añadido una función isNetworkAvailable() que comprueba si hay una conexión a internet activa antes de intentar hacer la petición a la API.
El botón ahora verifica primero la conectividad y solo intenta acceder a la API si hay conexión.


Si falla la conexión durante la petición a la API, ahora se mostrará una frase offline.
Si la respuesta de la API no es exitosa, también se mostrará una frase offline como respaldo.
Se añade un Toast informando que se está mostrando una frase offline por falta de conexión.

Con internet: obtendrá frases de la API como antes
Sin internet: mostrará frases preestablecidas, evitando errores y ofreciendo una experiencia de usuario fluida

Los usuarios pueden cambiar entre modo claro y oscuro según sus preferencias.
Las frases motivacionales aparecen con una animación suave y elegante.
La interfaz se adapta automáticamente a los cambios de tema.
Las preferencias de tema se mantienen entre sesiones.
Todo sigue funcionando sin conexión a internet gracias al sistema de frases offline.



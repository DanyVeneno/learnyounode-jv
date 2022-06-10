# Aprendiendo NodeJS

---


## CLIENT HTTP

Escribe un programa que reciba como argumento una URL y realice una pétición **HTTP GET** a la misma. Luego, Deberá imprimir por consola el contenido de cada evento **"data"** de lapetición, unopor linea.

---

## Pista


Para este ejercicio necesitas el modulo http incluido en Node.

Ladocumentación del modulo http la encuentras en file://Users/

El metodo **http.get()** es versión simplificada para peticiones GET y conviene que la use para la solución .Elprinmer parametro de **http.get()** es la URL y el segundo es un callback.
A diferencia de otros callbacks la firma es:

```NodeJS
function callback (response){/*...*/}

```

Siendo **response** un objeto Stream de Node.En Donde Node los Estreams emiten eventos, a los cuales puedes suscribir callbacks. Para este ejercicio sólo no interesan los eventos: **"data"**, **"error"** y **"end"**. Para escuchar un evento deveshacer:

```
response.on('data', function(data){/*...*/})

```

El evento **"data"** se dispara cuando un chunck, conjunto de datos, está disponible para procesarse.El tamaño de chunck depende de la implementación.

Nota: Por omición, los objetos **"data"**recibidosson buffers de Node que deben ser convertidos a Strings para luego ser eescritos en consola.Sin embargo, elobjeto response que obtienes de **http.get()** tiene un metodo setEncoding() que permite definir cómo se leen los bytes obtenidos. Ssilo llamas con parametro "utf-8" rexcibirás Strings en los eventos emitidos.

---


- Para ver estas instrucciones de nuevo,    ejecute: learnyournode print
- Para ejecutar su programa en un entorno de pruebas . ejecute: learnyounode run program.js
- Para verificar su programa ejecute learnyounode verify program.js 
- Para más información, ejecute: learyounode help



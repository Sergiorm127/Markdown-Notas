# React

Biblioteca de JavaScript para crear interfaces de usuario, desarrollo de app web de una página.

Es declarativo, no tenemos que decirle paso a paso que hacer.

## Formar de crear proyecto en React

* `npx create-react-app <nombre>` , `cd <nombre>`, `npm start` y se inicia la appweb. (crea una estructura de proyecto)

* O mediante Vite (También crea una estructura de proyecto, tiene como objetivo proporcionar una experiencia de desarrollo más rápida y ágil para proyectos web modernos). `npm create vite@latest`(elegimos la opción de swc que sirve para compilar más rápido), `cd <nombre-proyecto>`, `npm install` y `npm run dev`(inicializa el proyecto y nos da el localhost).

## Esturctura de archivos

* index.js : Componente principal que se carga de reenderizar nuestra app y componentes.

* Package.json : Información sobre proyecto(librerías y dependencias).

* .gitignores : Archivo donde ponemos que archivos no queremos subir a git .

* src : Directorio principal donde vamos a dejar archivos de nuestros componentes.

## Características React

* Props : Características que le pasamos por parámetro. Una prop especial es { children } ,con esta recoge todo lo que se haya escrito dentro del elemento creado.

* Hooks : Sirven para guardar estados de nuestros componentes (useState, useEffect).

## Hooks

* useState : Devuelve un array de dos posiciones, la primera es el valor del estado y la segunda la actualización. ( `const [count, setCount] = useState(0)`).

* useEffect : Nos permite ejecutar código arbitrario cada vez que se reenderiza el componente. (useEffect(código para ejecutar, lista de dependencias)),el código para ejecutar es una función y  la lista de dependencias es opcional, pero sino se le pasa nada se se ejecuta cada vez que reenderiza, es un array. Si ponemos un [] array vacío solo se ejecuta la primera vez que reenderiza. Ejemplo : `const [felicitacion, [winner]]` cada vez que haya un ganador se ejecutara la función llamada "felicitacion". Tambien se puede dar varios parámetros en el array. Se suele utilizar para guardar en la base de datos cada vez que pase algo, o para hacer una petición de datos una vez empieza la app o hacer un tracking. 
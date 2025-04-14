<!-- hide -->
# Traffic Light with React
<!-- endhide -->

A veces queremos crear componentes que mantengan un estado interno en el tiempo. Imaginemos un semáforo que cambia de color cada 3 segundos, para implementar eso tendríamos una variable `color` y le colocaríamos un color por defecto:

```js
let color = "blue";
```

Pero solo con tener esa variable no basta, necesitamos que cada vez que la variable color cambie también lo haga el código HTML del semáforo, para eso utilizamos el hook de react llamado `useState`:

```js
//        ↓ nombre de variable         ↓ valor por defecto
const [ color, setColor ] = useState("red");
//               ⬆ función para cambiar la variable "color"
```

De ahora en adelante, cada vez que utilicemos la función `setColor` para cambiar el valor de la variable `color`, el HTML del componente también se actualizará para reflejar el cambio.

> Puedes [leer más sobre hooks aquí](https://4geeks.com/es/lesson/react-hooks-explained-es).

<how-to-start>
  
## 🌱 Cómo comenzar este proyecto

No clones este repositorio porque vamos a usar una plantilla diferente.

Recomendamos abrir el `react boilerplate` usando un entorno de desarrollo como [Codespaces](https://4geeks.com/es/lesson/tutorial-de-github-codespaces) (recomendado) o [Gitpod](https://4geeks.com/es/lesson/como-utilizar-gitpod). Alternativamente, puedes clonarlo en tu computadora local usando el comando `git clone`.

Este es el repositorio que necesitas abrir o clonar:

```text
https://github.com/4GeeksAcademy/react-hello
```

**👉 Por favor sigue estos pasos sobre** [cómo comenzar un proyecto de programación](https://4geeks.com/es/lesson/como-comenzar-un-proyecto-de-codificacion).

> 💡 Importante: Recuerda guardar y subir tu código a GitHub creando un nuevo repositorio, actualizando el remoto (`git remote set-url origin <your new url>`) y subiendo el código a tu nuevo repositorio usando los comandos `add`, `commit` y `push` desde la terminal de git.

</how-to-start>

## 📝 Instrucciones

Simulemos un semáforo [como este](https://github.com/breatheco-de/exercise-traffic-light-react/blob/master/preview.gif).

La luz tiene que brillar cuando se hace clic.

- Todo el propósito del componente es mostrar un semáforo con luces roja, amarilla y verde.
- Cuando se hace clic (se selecciona) alguna luz, esta debe brillar, pero las otras luces deben dejar de brillar.
- El componente debe tener un estado que almacene el color actual que debe brillar, por eso debes usar el hook `useState` de la siguiente manera:
  
```js
const [ color, setColor ] = useState("red");
```

- Utiliza la función `setColor` para cambiar el color, y el componente se volverá a renderizar automáticamente (porque está vinculado con `useState`).
- Utiliza ReactDOM.render para renderizar el componente en el DOM de esta manera:

```js
ReactDOM.render(<TrafficLight />, document.querySelector('#app'));
```

## 🔥 Bonus

+ 2 Crea un botón que, al hacer clic en él, alterna el color seleccionado del semáforo entre rojo, verde y amarillo.
+ 10 Tener un botón que al hacer clic en él, añada un color extra "púrpura" al semáforo.

Este y otros proyectos son usados para [aprender a programar](https://4geeksacademy.com/es/aprender-a-programar/aprender-a-programar-desde-cero) por parte de los alumnos de 4Geeks Academy [Coding Bootcamp](https://4geeksacademy.com/us/coding-bootcamp) realizado por [Alejandro Sánchez](https://twitter.com/alesanchezr) y muchos otros contribuyentes. Conoce más sobre nuestros [Cursos de Programación](https://4geeksacademy.com/es/curso-de-programacion-desde-cero?lang=es) para convertirte en [Full Stack Developer](https://4geeksacademy.com/es/coding-bootcamps/desarrollador-full-stack/?lang=es), o nuestro [Data Science Bootcamp](https://4geeksacademy.com/es/coding-bootcamps/curso-datascience-machine-learning).

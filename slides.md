---
theme: default
class: text-center
highlighter: shiki
lineNumbers: true
drawings:
  persist: false
---

<div>
    <h1>Cypress</h1>
    <h4>Pruebas rápidas, fáciles y confiables para cualquier cosa que se ejecute en un navegador.</h4>
</div>

<div class="pt-5 opacity-80">
    <h3>Hoy con:</h3>
    <h4>Camilo Ruiz</h4>
    <h5>Desarrollador Front-end</h5>
</div>

<!--
Hola a todos gracias por venir a esta charla

...

hoy vamos a hablar de Cypress

...

Mi nombre es Camilo, soy desarrollador web con 6 años de experiencia mas que todo en el area de front-end

...

y mi objetivo hoy es ayudarlos a comenzar a trabajar con cypress, espero que al finalizar tengan una visión general de lo que es y de lo que puede hacer esta herramienta.

...

tenemos bastante que ver así que comencemos de una vez
-->

---
layout: center
class: text-center
---

# Qué es Cypress?

<!--
Antes de llegar a los detalles esenciales tomemos un momento para hablar de lo que es Cypress, algunos de ustedes probablemente ya tienen una idea, pero para aquellos que recién se están familiarizando, miremos rapidamente de que se trata
-->

---
layout: center
class: text-center
---

# Una herramienta para testear de manera confiable cualquier cosa que se ejecute en un navegador web.

<!--
Primero y ante todo, Cypress es una herramienta para testear de manera confiable cualquier cosa que se ejecute en un navegador web, especialmente es usada  para el testeo de aplicaciones web modernas como las que están escritas en react, vue, angular entre otros, pero es importante mencionar que Cypress es completamente agnóstico del stack tecnologico que estemos usando, es decir no importa cómo y en qué hayas escrito tu aplicación, en principio si se ejecuta en el navegador, Cypress es la herramienta ideal que va a ayudarnos con nuestro testing
-->

---
layout: center
---

# Para que se usa Cypress?

<div v-click>

- 🧑‍💻 **e2e tests**

</div>

<div v-click>

- 🐛 **Integration tests**

</div>

<div v-click>

- 🛠 **Unit tests**

</div>

<div v-click>

- 🛠 **Visual tests / UI testing**

</div>

<!--
Cypress lo podemos usar para

.... CLICK

End to end testing que en español seria algo como pruebas de principio a fin

....

Que es donde testeamos al mismo tiempo todos los diferentes sistemas y subsistemas que integran nuestra applicacion inclusive el front-end

.... CLICK

tambien nos permite escribir los tests de integración

.... CLICK

los test unitarios

.... CLICK

los tests visuales o los UI testCyp

Aunque su mayor cometido es realizar pruebas e2e, al ser un framework que incluye Mocha, Chai y Sinon se pueden realizar perfectamente pruebas unitarias.
-->

---
layout: center
class: text-center
---

# Pero que es testing?

<!--
Pero que es tesing? por que claro estamos hablando de testing y de testear, y ademas tenemos tambien muchos tipos de testing

....

por nombrar algunos:

Unit testing

Integration testing

Functional testing

End-to-end testing

Regression testing

Smoke testing

Acceptance testing

Performance testing

Exploratory testing

Visual testing

Asi que antes de seguir paremos un momento y preguntemonos que es testing o a que nos referimos con testear, pero de una forma mas general vale?

...

y lo digo mas por la gente del run, no por la gente que ya esten un poco mas avanzados en el tema, si no para los que estan aprendiendo un monton de cosas y siglas y terminos todos a la vez y de golpe

...

por que me paso, que cuando estaba haciendo el run, pues no todo lo que me mostraban o me intentaban explicar quedaba como en un lugar fijo en mi mente, si no que mas bien lo que yo tenia en ese momento se parecia mas a una masa sin pies ni cabeza ... y mas que la mayoria del tiempo escuchamos la referencia a los diferentes temas en palabras inglesas pues asi mas deficil para ententeder.

...

Entonces me gustaria que en un momento rapido nos fijemos a nuestro alrededor en todos los productos o cosas que usuamos en el dia a dia

...

por ejemplo una silla

...

Pues a esa silla alguien le tuvo que hacer un testing ... alguien la tuvo que testear alguien lo tubo que PROBAR estamos hablando de pruebas

...

o por ejemplo el boton de nuestro movil, alguien tuvo que PROBARLO para saber que realmente resiste una cantidad muy grande de obturaciones

...

o por ejemplo cuando cocinamos, usualmente PROBAMOS que tal va de sal la comida para corregir el sabor si es necesario

...

pues asi todos los productos pasaron por algun tipo de prueba y de la misma forma nuestros software necesita estas pruebas para asi nosotros saber de que es capaz y de que no, como cuando vemos en el manual de la silla que dice que la silla soporta hasta 70 kilos, asi mismo testeamos nuestra app para por ejemplo saber cuantos procesos soporta al mismo tiempo, con eso le podemos decir al cliente mira hasta 70kilos de peticiones soporta la app.

...

otro ejemplo es como los humanos de la edad de piedra fueron probando durante un largo tiempo todas las rocas de una en una para encontrar la que mas tenia resistencia para luego poder usarla como una herramienta para cortar, para casar o para lo que fuese, asi mismo podemos ver a nuestros test haciendo a nuestra aplication tan fuerte que al final no se rompe y con los diferentes test que escribimos se van probando los casos de usos que van surgiendo  y de esta forma haciendo de nuestra aplicacion una herramienta, efectiva Asi mismo como el ejercicio de pegarle a las rocas de alguna forma ayudaron a los humanos de la edad de piedra a tener herramientas utiles.

basicamente nuestra app es un diamente en bruto hasta que metemos los test y la pulimos

y para que hablo de esto?

Por que Cypress es una herramienta de testing

asi que voy a hablar de tres tipos de pruebas especificamente,  de las pruebas unitarias, de integracion y e2e y vamos a ver de manera rapida donde se ubica cada una de ellas en nuestro software

por lo general estos diferentes tipos de test se hacen instalando y configurando diferentes librerias y dependencia para cada caso

Pero Cypress es una herramienta que lo engloba todo en uno, la instalas y te permite escribir todo tipo de pruebas como las que ya hemos mencionado
-->

---
layout: center
class: text-center
---

# Unidades

<!--
Comenzamos con las unidades, y vamos a tomar de nuevo el ejemplo de las herramientas de la edad de piedra y en especifio una lanza con la que cazaban los animales
-->

---
layout: center
class: text-center
---

<div class="grid grid-cols-2 gap-4">
  <div>
    <img  v-click src="https://historiando.org/wp-content/uploads/2018/06/Edad-de-Piedra-Herramientas.jpg" class="w-100 mx-auto" />
    <img v-click src="https://hwcol.com/wp-content/uploads/2020/04/1586710935_La-cuerda-de-la-Edad-de-Piedra-fortalece-el-caso.jpeg" class="w-100 mx-auto" />
  </div>
  <div>
    <img  v-click src="https://tikihome.es/wp-content/uploads/2021/06/0425_tikihome_pantalla_palos_madera_blanca_02.jpg"
    style="width: 100%; object-fit: cover; height: 100%;"/>
  </div>
</div>

<!--
Entonces de que esta compuesta una lanza

-->

---
layout: center
class: text-center
---
# Integración

<img  src="https://i.pinimg.com/736x/f5/cb/d3/f5cbd38ec0321d59fbeed8e4c338c4eb.jpg" class="w-100 mx-auto" />

<!--
Aqui es donde entran los test de integracion que se encarga de probar que todas las unidades juegen bien entre ellas al momento de usar las juntas
-->

---
layout: center
class: text-center
---

# Subsistema

<img  src="cazador.png" class="w-50 mx-auto" />

<!--
Luego nuestra lanza  es usada por otra parte del sistema, probablemente un subsistema
-->

---
layout: center
class: text-center
---

<div class="sGrid">
  <div class="title" v-click="4">
    <img  src="titles.png" />
  </div>
  <div class="rigth" v-click="1">
    <img  src="rigth.png" />
  </div>
  <div class="left" v-click="2">
    <img  src="left.png" />
  </div>
  <div class="terceros" v-click="3">
    <img  src="terceros.png" />
  </div>
</div>

<style>

.sGrid {
  display: grid;
  grid-template-areas:
    ". sub1 title sub2 ."
    ". sub1 title sub2 ."
    ". sub1 third sub2 .";
  grid-template-rows: auto;
  grid-template-columns: 1fr 19% 46% 18% 1fr;

}
.rigth {
  grid-area: sub1;
}
.left {
  grid-area: sub2;
}
.title {
  grid-area: title;
}
.terceros {
  grid-area: third;
}

</style>

<!--
Entonces tenemos una parte de nuestro sistema o un subsistema pero no solo tiene que ser uno,

CLICK

podemos tener dos, 

CLICK

o tres, 

y ademas podemos estar requieriendo la ayuda de otros sistemas, que no hemos escrito nosotros 

CLICK

es decir cosas que desarrolamron terceros, como por ejemplo una dependencia o como la API de twitter

...

y todas estas partes o subsistemas conforma lo que es nuestra aplicacion que en este ejemplo se llama 

CLICK

MAMMOTH Hunting, que hace una cosa por por los usuario... que? pues casar un Mammoth


que es como cuando testeamos un sistema de compras

entonces el e2e es desde que la persona llega a nuestro website y ve nuestros producos hasta que le llega el correo de confirmacion de compra el producto
-->

---
layout: center
class: text-center
---

# Configuración e Instalación de Cypress

<div v-click class="pt-5 opacity-80">

```sh
$ npm install -D cypress
```
</div>

<!--
Bueno la instalación es muy simple

CLICK

todo lo que tenemos que hacer es npm install -D cypress

...

es solo esta línea, no hay herramientas o binarios adicionales ni nada más para
configurar o instalar Cypress

...

Esto es todo lo que tenemos que hacer para obtener una herramienta que va a manejar todo lo relacionado a pruebas o testing por nosotros

...

una vez que ejecutamos este comando obtendremos dos cosas, una es la aplicación visual para escritorio la cual probablemente es la que usaremos en nuestro día a día

Y también obtendremos la herramienta de linea de comandos o CLI la cual usaremos para arrancar Cypress sin necesidad de abrir la aplicación visual y también es la que usaremos para correrlo en entornos de integración continua.

Vamos a ir viendo mas de como estos dos programas funcionan a lo largo de la presentación
-->

---
layout: image-right
image: https://source.unsplash.com/collection/94734566/1920x1080
---

# Estructura del proyecto

* 📦 Carpeta principal del proyecto
  * 📁 ...
  * 📂 cypress
    * 📂 fixtures
    * 📂 integration
    * 📂 plugins
    * 📂 support

<!--
La estructura de un proyecto que usa Cypress luce similar a esta, tenemos la carpeta cypress que esta en el nivel superior dentro de la carpeta principal del proyecto y dentro tenemos la carpeta fixtures, la carpeta integration, la carpeta plugins y la carpeta support

...

debo recalcar que la carpeta integration es la mas importante, por que es esta carpeta la que usaremos para poner nuestros archivos de test

...

no debemos preocuparnos si no nos gusta el nombre de estas carpetas ya que luego podemos configurar Cypress para usar el nombre que queramos
-->

---
layout: center
---

# La API de Cypress

<div v-click>


```js
cy.<command>
```
</div>

<arrow v-click="2" x1="200" y1="420" x2="390" y2="310" color="#564" width="3" arrowSize="1" />

<arrow v-click="3" x1="400" y1="420" x2="415" y2="320" color="#564" width="3" arrowSize="1" />

<arrow v-click="4" x1="500" y1="420" x2="450" y2="320" color="#564" width="3" arrowSize="1" />

<!--
Avancemos y echemos un vistazo rapido a la API de Cypress

...

la API es una de las razones por las que da gusto usar Cypress y es porque la API es muy intuitiva y es casi como si narráramos como los usuarios interactúan con la aplicación, por ejemplo, el usuario visita la pagina de contactenos, el usuario rellena un fromulario, y el usuario hace click en el boton de enviar

...

sigamos adelante y veamos algunos ejemplos de cómo realmente usamos esta API.

CLICK

Podemos acceder a la API de Cypress a través de la propiedad global 'cy' que al ser global está disponible para que la usemos dentro de cualquier archivo dentro de la carpeta integration.

...

Entonces podemos escribir

CLICK

'cy'

 CLICK

punto

CLICK

y luego el commando que queramos usar

...

Todos los comandos están bien explicados en la documentation del sitio oficial de cypress, en la ultima parte de la presentación compartiré algunos enlaces dentro de los cuales esta el de la documentación, para que luego cada uno la mire con más tiempo, en esta presentación no podemos ver todos los comandos ya que son bastantes.
-->

---
layout: center
---

# Algunos commandos

<div v-click>

- **.click()**

</div>

<div v-click>

- **.dblclick()**

</div>

<div v-click>

- **.rightclick()**

</div>

<div v-click>

- **.type()**

</div>

<div v-click>

- **.clear()**

</div>

<div v-click>

- **.check()**

</div>

<div v-click>

- **.uncheck()**

</div>
<div v-click>

- **.select()**

</div>

---
layout: center
---

```js
cy.get('.botonAzul')
```

<!--
Echemos un vistazo por ejemplo al comando GET

...

Podemos usar este comando para obtener un elemento en la página

en este caso en especifico estamos obteniendo un botón que tiene la clase .botonAzul
-->

---
layout: center
---

```js {all|1|2|3}
cy.get('.botonAzul')
  .click()
  .should('have.class', 'active')
```

<!--
Una vez que obtengamos este botón, podemos realizar acciones con el y también hacer afirmaciones en su contra, por ejemplo

...CLICK

 aquí primero estamos obteniendo el botón

...CLICK

luego estamos haciendo click en el botón

...CLICK

y luego estamos haciendo una afirmación de que este botón debería  tener una clase 'active'  luego de haberse realizado el click

...

este es un ejemplo simple pero podemos hacer cosas aún más avanzadas
-->

---
layout: center
---

```js {all|1|2|3}
cy.request('/usuarios/1')
  .its('body')
  .should('deep.eql', {nombre:'Camilo', edad: 30})
```

<!--
Como por ejemplo hacer una solicitud a una base de datos por medio de una API

...CLICK

En este caso estamos requiriendo un endpoint llamado usuarios al cual le pasamos el ID numero 1

...CLICK

luego obtenemos el body de la respuesta

... CLICK

Y así luego podemos confirmar que el body contiene lo que estamos esperando.

....

en este caso el nombre y edad del usuario

-->

---
layout: center
class: text-center
---

# Abrir la applicación de escritorio

<div v-click class="pt-5 opacity-80">


```sh
$ npx cypress open
```
</div>

<!--
Ahora es tiempo de hablar de la aplicación de escritorio, comenzando por como la abrimos o como la ejecutamos

...CLICK

bueno como Cypress es un binario que esta en nuestra carpeta de node_modules podemos usar npx para ejecutar el comando 'cypress open' para así abrir la aplicación, teniendo en cuenta que si lo hacemos por primera vez, especialmente en un proyecto nuevo, este comando creara la carpeta cypress, que incluye todas las carpetas que vimos anteriormente, las cuales podemos utilizar para configurar y modificar el comportamiento de Cypress así como para añadir nuestros test...
-->

---
layout: image
image: >-
  https://c8.alamy.com/compes/cb78a3/el-engrasado-de-manos-de-un-mecanico-que-la-fijacion-de-un-eje-de-transmision-la-habana-la-habana-cuba-cb78a3.jpg
class: text-center
---

# Demo Time
### Vamos a ensuciarnos un poco las manos

<style>
h1,h3 {
  color: white !important;
  background-color: black !important;
  background-image: unset !important;
  padding: 20px !important;
  -webkit-background-clip: unset !important;
  -moz-background-clip: unset !important;
  -webkit-text-fill-color: unset !important;
  -moz-text-fill-color: unset !important;
}
</style>

<!--
Ahora que hemos escuchado un poco que es y que hace Cypress, es tiempo de adentrarnos y comenzar a utilizarlo, y también de ver como luce la aplicación de escritorio que habíamos mencionado antes
-->

---
layout: center
---

```js {1|2|4-7|9|11-13|15}
it('signup and login user', () => {
  cy.visit('http://localhost:8080/signup')

  cy.get('input[name="email"]').type('camilo@cypress.io')
  cy.get('input[name="password"]').type('1234')
  cy.get('input[name="confirm-password"]').type('1234')
  cy.get('#signup-button').click()

  cy.location('pathname').should('eq', '/login')

  cy.get('input[name="email"]').type('camilo@cypress.io')
  cy.get('input[name="password"]').type('1234')
  cy.get('#login-button').click()

  cy.location('pathname').should('eq', '/board')
})
```


---
layout: center
---

# Comando cy.task

```js {3-11}
// cypress/plugins/index.js

const { clearDatabase, seedDatabase } = require('../../server/db')

module.exports = (on, config) => {
  on('task', {
    'clear:db': () => {
      return clearDatabase()
    }
  })
}

```

---
layout: center
---

```js {6-20|1-4}
context('User setup', () => {
  beforeEach(() => {
    cy.task('clear:db')
  })

  it('signup and login user', () => {
    cy.visit('http://localhost:8080/signup')

    cy.get('input[name="email"]').type('camilo@cypress.io')
    cy.get('input[name="password"]').type('1234')
    cy.get('input[name="confirm-password"]').type('1234')
    cy.get('#signup-button').click()

    cy.location('pathname').should('eq', '/login')

    cy.get('input[name="email"]').type('camilo@cypress.io')
    cy.get('input[name="password"]').type('1234')
    cy.get('#login-button').click()

    cy.location('pathname').should('eq', '/board')
  })
})
```

<!--
-->

---
layout: center
---

# Hooks

<div v-click>

- **before()**

</div>

<div v-click>

- **beforeEach()**

</div>

<div v-click>

- **afterEach()**

</div>

<div v-click>

- **after()**

</div>


---
layout: center
---

# Comandos Customizados

---
layout: center
---

```js {all|16-18}
context('User setup', () => {
  beforeEach(() => {
    cy.task('clear:db')
  })

  it('signup and login user', () => {
    cy.visit('http://localhost:8080/signup')

    cy.get('input[name="email"]').type('camilo@cypress.io')
    cy.get('input[name="password"]').type('1234')
    cy.get('input[name="confirm-password"]').type('1234')
    cy.get('#signup-button').click()

    cy.location('pathname').should('eq', '/login')

    cy.get('input[name="email"]').type('camilo@cypress.io')
    cy.get('input[name="password"]').type('1234')
    cy.get('#login-button').click()

    cy.location('pathname').should('eq', '/board')
  })
})
```

---
layout: center
---

```js {3-11}
// cypress/support/commands.js

Cypress.Commands.add('loginWithUI', (email, password) => {
  cy.get('input[name="email"]').type(email)
  cy.get('input[name="password"]').type(password)
  cy.get('#login-button').click()
})

```

---
layout: center
---

```js {all|16-18}
context('User setup', () => {
  beforeEach(() => {
    cy.task('clear:db')
  })

  it('signup and login user', () => {
    cy.visit('http://localhost:8080/signup')

    cy.get('input[name="email"]').type('camilo@cypress.io')
    cy.get('input[name="password"]').type('1234')
    cy.get('input[name="confirm-password"]').type('1234')
    cy.get('#signup-button').click()

    cy.location('pathname').should('eq', '/login')

    cy.get('input[name="email"]').type('camilo@cypress.io')
    cy.get('input[name="password"]').type('1234')
    cy.get('#login-button').click()

    cy.location('pathname').should('eq', '/board')
  })
})
```

---
layout: center
---

```js {16}
context('User setup', () => {
  beforeEach(() => {
    cy.task('clear:db')
  })

  it('signup and login user', () => {
    cy.visit('http://localhost:8080/signup')

    cy.get('input[name="email"]').type('camilo@cypress.io')
    cy.get('input[name="password"]').type('1234')
    cy.get('input[name="confirm-password"]').type('1234')
    cy.get('#signup-button').click()

    cy.location('pathname').should('eq', '/login')

    cy.login('camilo@cypress.io', '1234')

    cy.location('pathname').should('eq', '/board')
  })
})
```


---
layout: center
---

# Comando cy.task

```js {3-11}
// cypress/plugins/index.js

const { clearDatabase, seedDatabase } = require('../../server/db')
const userSeed = require('../../server/seed/users')

module.exports = (on, config) => {
  on('task', {
    'clear:db': () => {
      return clearDatabase()
    }
  })

  on('task', {
    'seed:db': (data) => {
      return seedDatabase(data)
    }
  })
}

```

---
layout: center
---

# Stubbing network with fixtures cypress


```js {all}
// Fixture is stored in cypress/fixtures/tweets.json
cy.fixture('tweets').then((tweets) => {
  cy.route({
    url: '/tweets*',
    response: tweets,
    delay: 3000, // simulate slow response
    status: 404
  })
  .as('tweets')
})

cy.window().then(win => {
  cy.wait('@tweets')
    .its('response.body.tweets')
    .should('have.length', win.app.$store.state.tweets.length)
})
```

---
layout: center
---

# CI / Integración continua

<div v-click class="pt-5 opacity-80">

```sh
$ npx cypress run
```

</div>
---
layout: center
---

# Algunas Características de Cypress

<div v-click>

- 🧑‍💻 **Viaje en el tiempo**

</div>

<div v-click>

- 🐛 **Debuggability**

</div>

<div v-click>

- 🛠 **Espera automática**

</div>

<div v-click>

- 🚦 **Control de tráfico de red**

</div>

<div v-click>

- 📱 **Testeo responsive**

</div>

<div v-click>

- 🎥 **Capturas de pantalla y videos**

</div>

<div v-click>

- 🛠 **Testeo en multiples navegadores**

</div>

<!--
Ahora veamos algunas de las características más relevantes de Cypress

...CLICK

- Cypress toma capturas de pantalla mientras se ejecutan las pruebas. podemos pasar el cursor sobre los comandos en el registro de comandos para ver exactamente lo que sucedió en cada paso.

...CLICK

- Cypress nos ayuda también a dejar de adivinar por qué fallan nuestros test, debido a que se ejecuta dentro del navegador podemos debuggear directamente desde herramientas familiares como la Developer Tools.

...CLICK

- Cypress espera automáticamente los comandos y las afirmaciones antes de continuar. adios al async hell..

...CLICK

- Controle, cree stubs y pruebe casos extremos fácilmente sin involucrar a su servidor. Puede bloquear el tráfico de la red como desee.

...CLICK

- Con Cypress de manera fácil podemos configurar diferentes anchos de pantalla, lo cual no permite testear visualmente nuestra app en diferentes dispositivos

...CLICK

- Vea capturas de pantalla tomadas automáticamente en caso de falla o videos de todo su conjunto de pruebas cuando se ejecuta desde la CLI.

...CLICK

- Ejecute pruebas dentro de los navegadores de la familia Firefox y Chrome (incluidos Edge y Electron) localmente y de manera óptima
-->

---
layout: center
class: text-center
---

# Enlaces de interes

[Documentación](https://docs.cypress.io/guides/overview/why-cypress) · [GitHub](https://github.com/cypress-io/cypress) · [Ejemplos y Recetas](https://docs.cypress.io/examples/examples/tutorials#Test-a-React-Todo-App)

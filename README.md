# Base de datos de conjugaciones de verbos en español (MySQL)

Este repositorio contiene una base de datos en formato MySQL con conjugaciones de verbos en español, basada en el trabajo original de [asosab/esp_verbos](https://github.com/asosab/esp_verbos).

La base de datos incluye conjugaciones para múltiples modos, tiempos y personas gramaticales, estructuradas en una tabla llamada `conjugaciones`.

## Estructura de la tabla "conjugaciones"

| Campo        | Tipo           | Descripción                                   |
|--------------|----------------|-----------------------------------------------|
| id           | int            | Identificador único (auto-incremental)        |
| conjugacion  | varchar(64)    | Forma verbal conjugada                        |
| verbo        | varchar(64)    | Verbo en infinitivo                           |
| modo         | enum           | Modo verbal (indicativo, subjuntivo, etc.)    |
| tiempo       | varchar(32)    | Tiempo verbal (presente, pasado, etc.)        |
| persona      | varchar(32)    | Persona gramatical (yo, tú, él, etc.)         |

## Nota sobre auxiliares

Las formas auxiliares no están incluidas en esta base de datos. Se eliminaron para simplificar la estructura y evitar confusiones en las conjugaciones.

Por lo tanto, esta base contiene solo las formas conjugadas principales sin auxiliares explícitos para todos los verbos.

Por esa razón, agrego una referencia a ellos aquí:

| Auxiliar    | Modo               | Tiempo      | Ejemplo                          |
|-------------|--------------------|-------------|---------------------------------|
| habré       | perfecto           | futuro      | Yo habré terminado mañana       |
| habrás      | perfecto           | futuro      | Tú habrás llegado temprano       |
| habrá       | perfecto           | futuro      | Él habrá comido antes de salir   |
| habremos    | perfecto           | futuro      | Nosotros habremos terminado      |
| habréis     | perfecto           | futuro      | Vosotros habréis estudiado       |
| habrán      | perfecto           | futuro      | Ellos habrán llegado ya          |
| había       | perfecto           | imperfecto  | Yo había salido cuando llamaste  |
| habías      | perfecto           | imperfecto  | Tú habías visto la película      |
| habíamos    | perfecto           | imperfecto  | Nosotros habíamos terminado      |
| habíais     | perfecto           | imperfecto  | Vosotros habíais estudiado       |
| habían      | perfecto           | imperfecto  | Ellos habían comido              |
| habría      | perfecto           | condicional | Yo habría ido si pudiera         |
| habrías     | perfecto           | condicional | Tú habrías hecho lo correcto     |
| habríamos   | perfecto           | condicional | Nosotros habríamos comprado eso  |
| habríais    | perfecto           | condicional | Vosotros habríais ganado         |
| habrían     | perfecto           | condicional | Ellos habrían terminado         |
| he          | perfecto           | presente    | Yo he comido                     |
| has         | perfecto           | presente    | Tú has llegado                   |
| ha          | perfecto           | presente    | Él ha visto la película          |
| hemos       | perfecto           | presente    | Nosotros hemos hablado           |
| habéis      | perfecto           | presente    | Vosotros habéis escrito          |
| han         | perfecto           | presente    | Ellos han salido                 |
| hube        | perfecto           | pretérito   | Yo hube terminado                |
| hubiste     | perfecto           | pretérito   | Tú hubiste hablado               |
| hubo        | perfecto           | pretérito   | Él hubo llegado tarde            |
| hubimos     | perfecto           | pretérito   | Nosotros hubimos ganado          |
| hubisteis   | perfecto           | pretérito   | Vosotros hubisteis llegado       |
| hubieron    | perfecto           | pretérito   | Ellos hubieron terminado        |
| esté        | subjuntivo         | presente    | Espero que él esté bien          |
| estés       | subjuntivo         | presente    | Quiero que tú estés feliz        |
| esté        | subjuntivo         | presente    | Que ella esté preparada          |
| estemos     | subjuntivo         | presente    | Es importante que estemos juntos |
| estéis      | subjuntivo         | presente    | Espero que vosotros estéis aquí  |
| estén       | subjuntivo         | presente    | Ojalá que ellos estén listos     |
| estaré      | indicativo         | futuro      | Yo estaré en casa mañana         |
| estarás     | indicativo         | futuro      | Tú estarás contento              |
| estará      | indicativo         | futuro      | Él estará cansado                |
| estaremos   | indicativo         | futuro      | Nosotros estaremos listos        |
| estaréis    | indicativo         | futuro      | Vosotros estaréis felices        |
| estarán     | indicativo         | futuro      | Ellos estarán en la reunión      |
| estaba      | indicativo         | imperfecto  | Yo estaba trabajando             |
| estabas     | indicativo         | imperfecto  | Tú estabas leyendo               |
| estábamos   | indicativo         | imperfecto  | Nosotros estábamos en casa       |
| estabais    | indicativo         | imperfecto  | Vosotros estabais en la playa    |
| estaban     | indicativo         | imperfecto  | Ellos estaban jugando            |
| estuve      | indicativo         | pretérito   | Yo estuve en la fiesta           |
| estuviste   | indicativo         | pretérito   | Tú estuviste allí                |
| estuvo      | indicativo         | pretérito   | Él estuvo enfermo                |
| estuvimos   | indicativo         | pretérito   | Nosotros estuvimos juntos        |
| estuvisteis | indicativo         | pretérito   | Vosotros estuvisteis ausentes    |
| estuvieron  | indicativo         | pretérito   | Ellos estuvieron en la casa      |
| estaría     | condicional        | condicional | Yo estaría más feliz allí        |
| estarías    | condicional        | condicional | Tú estarías mejor descansando    |
| estaríamos  | condicional        | condicional | Nosotros estaríamos de acuerdo   |
| estaríais   | condicional        | condicional | Vosotros estaríais felices       |
| estarían    | condicional        | condicional | Ellos estarían esperando         |
| hubiere     | perfecto_subjuntivo| futuro      | Cuando él hubiere terminado      |
| hubieres    | perfecto_subjuntivo| futuro      | Cuando tú hubieres llegado       |
| hubiere     | perfecto_subjuntivo| futuro      | Cuando ella hubiere hecho eso    |
| hubiéremos  | perfecto_subjuntivo| futuro      | Cuando nosotros hubiéremos ganado|
| hubiereis   | perfecto_subjuntivo| futuro      | Cuando vosotros hubiereis visto  |
| hubieren    | perfecto_subjuntivo| futuro      | Cuando ellos hubieren salido     |
| hubiera     | perfecto_subjuntivo| pasado      | Si yo hubiera sabido             |
| hubieras    | perfecto_subjuntivo| pasado      | Si tú hubieras venido            |
| hubiera     | perfecto_subjuntivo| pasado      | Si ella hubiera hecho eso        |
| hubiéramos  | perfecto_subjuntivo| pasado      | Si nosotros hubiéramos llegado   |
| hubierais   | perfecto_subjuntivo| pasado      | Si vosotros hubierais estudiado  |
| hubieran    | perfecto_subjuntivo| pasado      | Si ellos hubieran hablado        |
| haya        | perfecto_subjuntivo| presente    | Espero que él haya llegado       |
| hayas       | perfecto_subjuntivo| presente    | Espero que tú hayas terminado    |
| haya        | perfecto_subjuntivo| presente    | Espero que ella haya comido      |
| hayamos     | perfecto_subjuntivo| presente    | Espero que nosotros hayamos visto|
| hayáis      | perfecto_subjuntivo| presente    | Espero que vosotros hayáis oído  |
| hayan       | perfecto_subjuntivo| presente    | Espero que ellos hayan venido    |


## Créditos

Este proyecto es una adaptación del trabajo de [@asosab](https://github.com/asosab), quien recopiló y generó las conjugaciones en su repositorio [esp_verbos](https://github.com/asosab/esp_verbos).

La licencia utilizada es la misma que la del proyecto original: **Creative Commons Attribution-ShareAlike 4.0 International (CC BY-SA 4.0)**.

---

## Licencia

[![CC BY-SA 4.0](https://licensebuttons.net/l/by-sa/4.0/88x31.png)](https://creativecommons.org/licenses/by-sa/4.0/)

Este proyecto se distribuye bajo la licencia **Creative Commons Attribution-ShareAlike 4.0 International (CC BY-SA 4.0)**, en concordancia con el proyecto original.

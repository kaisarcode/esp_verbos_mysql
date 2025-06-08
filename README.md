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

| Auxiliar    | Modo        | Tiempo      |
|-------------|-------------|-------------|
| habré       | perfecto    | futuro      |
| habrás      | perfecto    | futuro      |
| habrá       | perfecto    | futuro      |
| habremos    | perfecto    | futuro      |
| habréis     | perfecto    | futuro      |
| habrán      | perfecto    | futuro      |
| había       | perfecto    | imperfecto  |
| habías      | perfecto    | imperfecto  |
| habíamos    | perfecto    | imperfecto  |
| habíais     | perfecto    | imperfecto  |
| habían      | perfecto    | imperfecto  |
| habría      | perfecto    | condicional |
| habrías     | perfecto    | condicional |
| habríamos   | perfecto    | condicional |
| habríais    | perfecto    | condicional |
| habrían     | perfecto    | condicional |
| he          | perfecto    | presente    |
| has         | perfecto    | presente    |
| ha          | perfecto    | presente    |
| hemos       | perfecto    | presente    |
| habéis      | perfecto    | presente    |
| han         | perfecto    | presente    |
| hube        | perfecto    | pretérito   |
| hubiste     | perfecto    | pretérito   |
| hubo        | perfecto    | pretérito   |
| hubimos     | perfecto    | pretérito   |
| hubisteis   | perfecto    | pretérito   |
| hubieron    | perfecto    | pretérito   |
| esté        | subjuntivo  | presente    |
| estés       | subjuntivo  | presente    |
| esté        | subjuntivo  | presente    |
| estemos     | subjuntivo  | presente    |
| estéis      | subjuntivo  | presente    |
| estén       | subjuntivo  | presente    |
| estaré      | indicativo  | futuro      |
| estarás     | indicativo  | futuro      |
| estará      | indicativo  | futuro      |
| estaremos   | indicativo  | futuro      |
| estaréis    | indicativo  | futuro      |
| estarán     | indicativo  | futuro      |
| estaba      | indicativo  | imperfecto  |
| estabas     | indicativo  | imperfecto  |
| estábamos   | indicativo  | imperfecto  |
| estabais    | indicativo  | imperfecto  |
| estaban     | indicativo  | imperfecto  |
| estuve      | indicativo  | pretérito   |
| estuviste   | indicativo  | pretérito   |
| estuvo      | indicativo  | pretérito   |
| estuvimos   | indicativo  | pretérito   |
| estuvisteis | indicativo  | pretérito   |
| estuvieron  | indicativo  | pretérito   |
| estaría     | condicional | condicional |
| estarías    | condicional | condicional |
| estaríamos  | condicional | condicional |
| estaríais   | condicional | condicional |
| estarían    | condicional | condicional |

## Créditos

Este proyecto es una adaptación del trabajo de [@asosab](https://github.com/asosab), quien recopiló y generó las conjugaciones en su repositorio [esp_verbos](https://github.com/asosab/esp_verbos).

La licencia utilizada es la misma que la del proyecto original: **Creative Commons Attribution-ShareAlike 4.0 International (CC BY-SA 4.0)**.

---

## Licencia

[![CC BY-SA 4.0](https://licensebuttons.net/l/by-sa/4.0/88x31.png)](https://creativecommons.org/licenses/by-sa/4.0/)

Este proyecto se distribuye bajo la licencia **Creative Commons Attribution-ShareAlike 4.0 International (CC BY-SA 4.0)**, en concordancia con el proyecto original.

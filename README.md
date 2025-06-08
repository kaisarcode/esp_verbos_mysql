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

| Auxiliar      | Verbo  | Modo        | Tiempo        |
|---------------|--------|-------------|---------------|
| habré         | haber  | perfecto    | futuro        |
| habrás        | haber  | perfecto    | futuro        |
| habrá         | haber  | perfecto    | futuro        |
| habremos      | haber  | perfecto    | futuro        |
| habréis       | haber  | perfecto    | futuro        |
| habrán        | haber  | perfecto    | futuro        |
| había         | haber  | perfecto    | imperfecto    |
| habías        | haber  | perfecto    | imperfecto    |
| habíamos      | haber  | perfecto    | imperfecto    |
| habíais       | haber  | perfecto    | imperfecto    |
| habían        | haber  | perfecto    | imperfecto    |
| habría        | haber  | perfecto    | condicional   |
| habrías       | haber  | perfecto    | condicional   |
| habríamos     | haber  | perfecto    | condicional   |
| habríais      | haber  | perfecto    | condicional   |
| habrían       | haber  | perfecto    | condicional   |
| he            | haber  | perfecto    | presente      |
| has           | haber  | perfecto    | presente      |
| ha            | haber  | perfecto    | presente      |
| hemos         | haber  | perfecto    | presente      |
| habéis        | haber  | perfecto    | presente      |
| han           | haber  | perfecto    | presente      |
| hube          | haber  | perfecto    | pretérito     |
| hubiste       | haber  | perfecto    | pretérito     |
| hubo          | haber  | perfecto    | pretérito     |
| hubimos       | haber  | perfecto    | pretérito     |
| hubisteis     | haber  | perfecto    | pretérito     |
| hubieron      | haber  | perfecto    | pretérito     |
| esté          | estar  | subjuntivo  | presente      |
| estés         | estar  | subjuntivo  | presente      |
| esté          | estar  | subjuntivo  | presente      |
| estemos       | estar  | subjuntivo  | presente      |
| estéis        | estar  | subjuntivo  | presente      |
| estén         | estar  | subjuntivo  | presente      |
| estaré        | estar  | indicativo  | futuro        |
| estarás       | estar  | indicativo  | futuro        |
| estará        | estar  | indicativo  | futuro        |
| estaremos     | estar  | indicativo  | futuro        |
| estaréis      | estar  | indicativo  | futuro        |
| estarán       | estar  | indicativo  | futuro        |
| estaba        | estar  | indicativo  | imperfecto    |
| estabas       | estar  | indicativo  | imperfecto    |
| estábamos     | estar  | indicativo  | imperfecto    |
| estabais      | estar  | indicativo  | imperfecto    |
| estaban       | estar  | indicativo  | imperfecto    |
| estuve        | estar  | indicativo  | pretérito     |
| estuviste     | estar  | indicativo  | pretérito     |
| estuvo        | estar  | indicativo  | pretérito     |
| estuvimos     | estar  | indicativo  | pretérito     |
| estuvisteis   | estar  | indicativo  | pretérito     |
| estuvieron    | estar  | indicativo  | pretérito     |
| estaría       | estar  | condicional | condicional   |
| estarías      | estar  | condicional | condicional   |
| estaríamos    | estar  | condicional | condicional   |
| estaríais     | estar  | condicional | condicional   |
| estarían      | estar  | condicional | condicional   |

## Créditos

Este proyecto es una adaptación del trabajo de [@asosab](https://github.com/asosab), quien recopiló y generó las conjugaciones en su repositorio [esp_verbos](https://github.com/asosab/esp_verbos).

La licencia utilizada es la misma que la del proyecto original: **Creative Commons Attribution-ShareAlike 4.0 International (CC BY-SA 4.0)**.

---

## Licencia

[![CC BY-SA 4.0](https://licensebuttons.net/l/by-sa/4.0/88x31.png)](https://creativecommons.org/licenses/by-sa/4.0/)

Este proyecto se distribuye bajo la licencia **Creative Commons Attribution-ShareAlike 4.0 International (CC BY-SA 4.0)**, en concordancia con el proyecto original.

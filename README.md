# Base de datos de conjugaciones de verbos en español (MySQL)

Este repositorio contiene una base de datos en formato MySQL con conjugaciones de verbos en español, basada en el trabajo original de [asosab/esp_verbos](https://github.com/asosab/esp_verbos).

La base de datos incluye conjugaciones para múltiples modos, tiempos y personas gramaticales, estructuradas en una tabla llamada `conjugaciones`.

## Créditos

Este proyecto es una adaptación del trabajo de [@asosab](https://github.com/asosab), quien recopiló y generó las conjugaciones en su repositorio [esp_verbos](https://github.com/asosab/esp_verbos).

La licencia utilizada es la misma que la del proyecto original: **Creative Commons Attribution-ShareAlike 4.0 International (CC BY-SA 4.0)**.

## Estructura de la tabla `conjugaciones`

| Campo        | Tipo           | Descripción                                   |
|--------------|----------------|-----------------------------------------------|
| id           | int            | Identificador único (auto-incremental)        |
| conjugacion  | varchar(64)    | Forma verbal conjugada                        |
| verbo        | varchar(64)    | Verbo en infinitivo                           |
| modo         | enum           | Modo verbal (indicativo, subjuntivo, etc.)    |
| tiempo       | varchar(32)    | Tiempo verbal (presente, pasado, etc.)        |
| persona      | varchar(32)    | Persona gramatical (yo, tú, él, etc.)         |

---

Para más detalles, consulta el repositorio original [asosab/esp_verbos](https://github.com/asosab/esp_verbos).

## Licencia

Este proyecto se distribuye bajo la licencia **Creative Commons Attribution-ShareAlike 4.0 International (CC BY-SA 4.0)**, en concordancia con el proyecto original.

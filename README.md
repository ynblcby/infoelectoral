# infoelectoral

<!-- badges: start -->
[![Lifecycle: experimental](https://img.shields.io/badge/lifecycle-experimental-orange.svg)](https://lifecycle.r-lib.org/articles/stages.html#experimental)
[![R-CMD-check](https://github.com/hmeleiro/infoelectoral/workflows/R-CMD-check/badge.svg)](https://github.com/hmeleiro/infoelectoral/actions)
[![CRAN status](https://www.r-pkg.org/badges/version/infoelectoral)](https://CRAN.R-project.org/package=infoelectoral)
[![License: GPL-2](https://img.shields.io/badge/license-GPL--2-blue.svg)](https://cran.r-project.org/web/licenses/GPL-2)
<!-- badges: end -->

[Infoelectoral](https://hmeleiro.github.io/infoelectoral/) es una librería de R para descargar resultados electorales oficiales de España del [Ministerio del Interior](http://www.infoelectoral.mir.es/infoelectoral/min/). Permite descargar resultados de las elecciones generales y municipales de cualquier año a nivel de mesa electoral y de municipio.


# Cómo instalarlo?

```
devtools::install_github("hmeleiro/infoelectoral")
```

# Cómo usarlo

La librería tiene cinco funciones: 

1. ``` mesas()``` para descargar datos a nivel de mesa electoral e importarlos al entorno.
2. ``` municipios()``` para descargar datos a nivel de municipio e importarlos al entorno.
3. ```candidatos()``` para descargar los datos de las listas electorales e importarlos al entorno.


Las funciones aceptan cuatro argumentos:

1. ``` tipoeleccion = c("generales", "municipales")```. El tipo de elección que se quiere descargar.
2. ``` yr```. El año de la elección en formato YYYY. Puede ir como número o como texto.
3. ``` mes```. El mes de la elección en formato mm. Se debe introducir el número del mes pero en forma texto (p.e: para mayo hay que introducir "05").

## Ejemplo
Para descargar los resultados electorales a nivel de municipio de las elecciones generales de marzo de 1979 (e importarlos directamente al entorno) se debe introducir:

```
library(infoelectoral)
generales_1979 <- municipios(tipoeleccion = "generales", yr = 1979, mes = "03")

```

## Ejemplos de uso

Aquí algunos [ejemplos de uso](https://r-elecciones.netlify.com/posts/).

# TallerEvalRend

Este repositorio contiene un taller de evaluación de rendimiento de algoritmos de multiplicación de matrices en C, utilizando distintos modelos de paralelismo: 
POSIX Threads, OpenMP y procesos con `fork()`. El objetivo es comparar el desempeño de cada enfoque en términos de tiempo de ejecución y eficiencia.

## Contenido del repositorio

- `EnunciadoEval.pdf`: Documento con las instrucciones y objetivos del taller.
- `funciones.c` y `funciones.h`: Funciones auxiliares para la generación y multiplicación de matrices.
- `mmClasicaPosix.c`: Implementación de multiplicación de matrices utilizando hilos POSIX.
- `mmClasicaOpenMP.c`: Implementación utilizando directivas OpenMP.
- `mmClasicaFork.c`: Implementación utilizando procesos con `fork()`.
- `lanza.pl`: Script en Perl para automatizar la ejecución de pruebas.
- `Makefile`: Archivo para compilar los programas.
- `ResultadosClasicaPosix.zip`, `ResultadosClasicaOpenMP.zip`, `ResultadosClasicaFork.zip`: Archivos comprimidos con los resultados obtenidos en las pruebas de rendimiento
      para cada enfoque.

## Requisitos

- Compilador de C (por ejemplo, `gcc`) con soporte para OpenMP.
- Perl (para ejecutar el script `lanza.pl`).
- Sistema operativo compatible con POSIX (Linux o macOS).

## Compilación

Para compilar los programas, utiliza el siguiente comando:

```bash
make
```

Este comando generará los ejecutables:

- `mmClasicaPosix`
- `mmClasicaOpenMP`
- `mmClasicaFork`

## Ejecución

Puedes ejecutar cada programa de la siguiente manera:

```bash
./mmClasicaPosix
./mmClasicaOpenMP
./mmClasicaFork
```

Para automatizar las pruebas y recopilar resultados, puedes utilizar el script en Perl:

```bash
perl lanza.pl
```

Este script ejecutará las pruebas para cada implementación y almacenará los resultados correspondientes.

## Resultados

Los archivos comprimidos en formato ZIP contienen los resultados obtenidos en las pruebas de rendimiento para cada enfoque:

- `ResultadosClasicaPosix.zip`
- `ResultadosClasicaOpenMP.zip`
- `ResultadosClasicaFork.zip`

Cada archivo incluye datos sobre los tiempos de ejecución y otros parámetros relevantes para el análisis comparativo.

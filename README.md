# blog-tecnico
Blog técnico para documentación de proyectos.
# Cómo resolví un problema de rendimiento en una aplicación web

## Contexto

Durante el desarrollo de una aplicación web para la gestión de tareas, el equipo comenzó a detectar demoras significativas al cargar el panel principal. A medida que aumentaba la cantidad de registros, el tiempo de respuesta también crecía, afectando la experiencia del usuario.

El proyecto utilizaba Git para el control de versiones y GitHub como plataforma de colaboración.

---

## Problema

El principal inconveniente era que la página inicial realizaba múltiples consultas innecesarias a la base de datos, generando tiempos de carga superiores a los 5 segundos.

Luego de analizar el código, se identificaron tres causas principales:

* Consultas repetidas a la base de datos.
* Falta de paginación en los listados.
* Procesamiento de información que podía realizarse previamente.

---

## Acciones realizadas

Se siguió el siguiente proceso para solucionar el problema:

1. Se analizaron los tiempos de respuesta utilizando las herramientas de desarrollo del navegador.
2. Se identificaron las consultas más costosas.
3. Se optimizaron las consultas SQL eliminando redundancias.
4. Se implementó paginación para limitar la cantidad de registros cargados.
5. Se realizaron pruebas comparando el rendimiento antes y después de los cambios.

### Post-mortem

Una vez resuelto el problema, el equipo realizó un análisis para identificar oportunidades de mejora.

Aspectos positivos:

* Se detectó rápidamente la causa del problema.
* El trabajo quedó correctamente documentado.
* Se validaron los cambios mediante pruebas.

Aspectos a mejorar:

* Incorporar revisiones de rendimiento durante el desarrollo.
* Definir métricas antes de implementar nuevas funcionalidades.
* Automatizar pruebas de rendimiento para futuras versiones.

---

## Aprendizajes

Esta experiencia permitió comprender que:

* El rendimiento debe considerarse desde las primeras etapas del desarrollo.
* Los pequeños cambios pueden generar mejoras importantes.
* La documentación y el control de versiones facilitan el trabajo colaborativo.
* Realizar un post-mortem ayuda a evitar que el mismo problema vuelva a ocurrir.

---

## Evidencia de control de versiones

Repositorio:

https://github.com/tomascanone2/blog-tecnico

Commits relevantes:

* Commit inicial de la solución
* Commit de optimización de consultas
* Commit de implementación de paginación
* Commit con documentación del post-mortem

---

## Reflexión sobre el feedback radicalmente sincero

Durante el desarrollo procuré recibir comentarios directos sobre las decisiones técnicas tomadas. En lugar de interpretar las observaciones como críticas personales, las utilicé para mejorar la calidad de la solución. Gracias a este enfoque fue posible detectar oportunidades de optimización que inicialmente habían pasado desapercibidas y fortalecer tanto el código como la forma de trabajar en equipo.

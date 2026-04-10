# GUION EXPOSICION — ENFOKIDS

---

## DIAPOSITIVA 1 — PORTADA

*(La diapositiva tiene el título completo y tu nombre)*

Buenos días. Mi nombre es Carlos Torres y el proyecto que voy a presentar hoy se llama **EnfoKids** — una plataforma web para apoyar la terapia de niños con TDAH en Colombia.

---

## DIAPOSITIVA 2 — CONTENIDO

*(6 bloques numerados: Problema, Justificación, Objetivos, Diseño, Desarrollo, Conclusiones)*

La presentación la organicé en estos seis puntos que ven acá. Vamos a ir de la mano del problema que dio origen al proyecto, pasando por los objetivos y el desarrollo, hasta llegar a los resultados y conclusiones.

---

## DIAPOSITIVA 3 — CONCEPTUALIZACIÓN

*(La diapositiva tiene 5 términos: TDAH, Gamificación, SCRUM, GLPI, MVP)*

Antes de arrancar, acá en pantalla están los conceptos clave que van a aparecer durante toda la exposición, para que todo lo que diga tenga contexto.

El **TDAH**, como dice ahí, es la condición que afecta la concentración y el control de impulsos en niños. Es el problema de salud que motivó este proyecto.

La **gamificación** es usar elementos de videojuegos — puntos, niveles, recompensas — dentro de la terapia, para que el niño quiera participar en lugar de aburrirse.

**SCRUM** es la metodología con la que organicé el desarrollo, trabajando en sprints, que son ciclos cortos donde al final de cada uno tengo algo funcional que mostrar.

Y el **MVP** es esa primera versión funcional con lo mínimo necesario para probar que la solución sirve.

---

## DIAPOSITIVA 4 — PLANTEAMIENTO DEL PROBLEMA

*(La diapositiva describe el problema y termina con la pregunta de investigación)*

Como dice acá, el problema está en que los niños con TDAH necesitan ejercicios constantes, pero no hay nada que coordine a las tres personas involucradas: el terapeuta que planea, el cuidador que acompaña en casa y el niño que los realiza.

Eso genera exactamente lo que aparece en pantalla: desorden en la información, falta de seguimiento y poca motivación.

Y eso me llevó a la pregunta que ven al final de la diapositiva:

> *"¿Cómo puede una aplicación web con actividades interactivas y herramientas de seguimiento apoyar la terapia en niños con déficit de atención?"*

Esa es la pregunta que EnfoKids responde.

---

## DIAPOSITIVA 5 — JUSTIFICACIÓN

*(La diapositiva menciona tres enfoques: práctico, social y académico)*

La justificación, como la ven acá, se puede ver desde tres ángulos.

Desde lo **práctico**: facilita que las terapias continúen en casa porque el cuidador sabe exactamente qué tiene que hacer el niño.

Desde lo **social**: hace el proceso más motivante para el niño y fortalece la relación entre la familia y el terapeuta.

Y desde lo **académico**, que es lo que me corresponde como tecnólogo: aplica conocimientos de desarrollo de software a una necesidad real con impacto en personas.

---

## DIAPOSITIVA 6 — OBJETIVO GENERAL

*(La diapositiva tiene el objetivo redactado completo)*

El objetivo general está acá en pantalla. En pocas palabras: desarrollar una plataforma que conecte a los tres actores del proceso terapéutico en un solo lugar.

El terapeuta asigna ejercicios personalizados, el cuidador puede ver cómo va el proceso, y el niño accede a un entorno lúdico para hacer sus actividades. Todo integrado con seguimiento y reportes.

---

## DIAPOSITIVA 7 — OBJETIVOS ESPECÍFICOS

*(La diapositiva tiene 4 objetivos numerados en forma de pirámide)*

Para lograr ese objetivo general me planteé estos cuatro objetivos específicos que ven acá, y cada uno corresponde a una etapa del desarrollo.

El primero fue **analizar los requerimientos** — saber qué necesita cada usuario antes de escribir una sola línea de código.

El segundo, **diseñar la arquitectura y la interfaz** — priorizando que sea fácil de usar, especialmente para los niños.

El tercero, **crear los módulos interactivos**: asignación de ejercicios, actividades gamificadas y seguimiento.

Y el cuarto, **implementar los reportes de progreso** para que terapeutas y cuidadores tengan información clara para tomar decisiones.

---

## DIAPOSITIVA 8 — FASES DE LA METODOLOGÍA

*(La diapositiva tiene los 5 sprints a la izquierda y su descripción a la derecha)*

Acá ven cómo organicé el trabajo. Cada sprint del lado izquierdo tiene su descripción al lado derecho.

El **Sprint 0** fue de preparación: investigar, definir requerimientos y priorizar.

El **Sprint 1** fue construir el sistema de usuarios: registro, login y que cada rol vea solo lo suyo — administrador, terapeuta, cuidador y niño.

El **Sprint 2** fue el módulo de asignación: crear actividades, agruparlas en planes y asignárselas a cada niño.

El **Sprint 3** fue la gamificación: los juegos interactivos y el registro de progreso.

Y el **Sprint 4** fue empaquetar con Docker, desplegar en servidor y escribir los manuales.

---

## DIAPOSITIVA 9 — SPRINT 1 — ARQUITECTURA

*(La diapositiva tiene el diagrama de arquitectura cliente-servidor con los 4 roles)*

Acá se puede ver la arquitectura completa del sistema.

A la izquierda está el **cliente**: el navegador con React. A la derecha está el **servidor**: Spring Boot con Spring Security. Y abajo está la **base de datos** PostgreSQL.

Lo importante de este sprint, además de que todo se comunicara bien, fue implementar los cuatro roles que ven arriba a la derecha: administrador, terapeuta, cuidador y niño. Cada uno accede solo a lo que le corresponde gracias a la autenticación con JWT.

---

## DIAPOSITIVA 10 — SPRINT 2 — ASIGNACIÓN Y ACTIVIDADES

*(La diapositiva muestra la pantalla real de la plataforma con el formulario de planes, y a la derecha el flujo: Actividades → Planes → Asignaciones → Progreso)*

Acá ven la plataforma real funcionando. A la izquierda el panel del terapeuta con el formulario para crear un plan de actividades. A la derecha el flujo completo que ven en los iconos.

Primero se crean las **actividades** individuales. Luego se agrupan en un **plan**. Ese plan se **asigna** a un niño con fechas. Y desde ahí se puede hacer seguimiento del **progreso**.

Todo eso es lo que el terapeuta maneja desde su panel.

---

## DIAPOSITIVA 11 — SPRINT 3 — GAMIFICACIÓN

*(La diapositiva tiene a la izquierda el diagrama del flujo del niño, y a la derecha la pantalla real con las misiones)*

Acá se ven dos cosas. A la izquierda el flujo completo: el niño entra, selecciona una misión, juega, obtiene estrellas, suma puntos y ese progreso queda registrado automáticamente.

A la derecha pueden ver la pantalla real del niño — diseñada como videojuego con las tarjetas de misión, la barra HP y los botones de jugar.

Los tres juegos que desarrollé, que ven en el diagrama, son: **Memoria**, **Conexión** y **Orden Rápido**. Cada uno trabaja una habilidad cognitiva diferente — atención sostenida, memoria de trabajo y velocidad de procesamiento respectivamente.

---

## DIAPOSITIVA 12 — SPRINT 4 — VIDEO DESPLIEGUE

*(La diapositiva muestra una captura del video con la carpeta del proyecto)*

En este sprint empaqueté toda la aplicación con **Docker Compose**. Lo que ven en pantalla es el video que grabé mostrando cómo se ejecuta el proyecto completo con un solo comando desde esa carpeta.

La idea era que la plataforma fuera portable — que cualquier persona pueda levantarla en cualquier máquina sin configuraciones manuales.

---

## DIAPOSITIVA 13 — SPRINT 4 — PLATAFORMA EN VIVO

*(La diapositiva muestra la landing page de EnfoKids en el navegador)*

Y este es el resultado final. Acá ven la plataforma ya desplegada y accesible desde el navegador.

La frase principal lo resume todo: *"El progreso de cada niño, visible para todos."* Abajo ven las métricas: 3 roles integrados, 2 juegos terapéuticos y actividades ilimitadas.

Esto ya estaba funcionando en un servidor de producción, accesible desde internet.

---

## DIAPOSITIVA 14 — CONCLUSIONES

*(3 bloques con una conclusión cada uno)*

Las conclusiones las ven divididas en tres bloques.

El primero: **SCRUM** funcionó muy bien para este tipo de proyecto. Trabajar por sprints me permitió gestionar la complejidad sin perder el hilo.

El segundo: se logró construir la plataforma con los tres roles, los juegos y el seguimiento — cerrando exactamente la brecha de comunicación que describí al inicio.

Y el tercero, el más importante: la tecnología web con gamificación **sí es viable** para apoyar la terapia de niños con TDAH en Colombia, llenando un vacío real que existía.

---

## DIAPOSITIVA 15 — CIERRE

Eso es todo. Agradezco a la Universidad, a la Facultad y a mi directora la Ingeniera Yelitza Contreras por el acompañamiento durante este proceso.

Quedo disponible para las preguntas. Muchas gracias.

---

## TIPS PARA PRACTICAR

1. Pon la diapositiva en pantalla
2. Lee el guion de esa diapositiva una vez
3. Cierra el guion e intenta decirlo solo mirando la diapositiva
4. La diapositiva te va recordando qué sigue — no necesitas memorizar todo

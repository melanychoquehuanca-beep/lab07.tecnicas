# Tarea: Mi prompt avanzado

## Tarea elegida

Diseño e implementación de un módulo en Java Swing dentro de un sistema académico para registrar estudiantes y calcular el promedio ponderado de sus notas finales (escrito en rango de 0 a 20), clasificando automáticamente su estado en 'Aprobado' o 'Desaprobado' con validación de entradas.

## Version 1: prompt basico

Crea un programa en Java para calcular el promedio de un alumno.

## Version 2

Actúa como un desarrollador Senior en Java. Diseña un módulo académico para registrar notas de estudiantes.

Crea una interfaz gráfica usando Java Swing que reciba 3 notas de un estudiante (de 0 a 20) junto con sus porcentajes o pesos (que sumen 100%). Calcula el promedio ponderado y muestra si está Aprobado (nota mayor o igual a 11) o Desaprobado.

No uses librerías externas.

## Version 3: prompt final

Actúa como un arquitecto de software especializado en Java. Diseña un módulo académico completo para un sistema de gestión universitaria.

Objetivo:
Crear una interfaz gráfica interactiva con Java Swing que solicite al usuario los datos de un estudiante, 3 notas (rango de 0.0 a 20.0) y sus respectivas ponderaciones porcentuales (que deben sumar exactamente 100%). Muestra el promedio ponderado final y una etiqueta dinámica de 'Aprobado' (si promedio >= 10.5) o 'Desaprobado' (si promedio < 10.5).

Restricciones técnicas:

1. Utiliza únicamente librerías estándar del JDK (javax.swing y java.awt), sin frameworks externos.
2. Implementa manejo de excepciones (Try-Catch) para capturar NumberFormatException si el usuario ingresa texto o deja campos vacíos, mostrando un mensaje de advertencia visual mediante JOptionPane.
3. El cálculo de las notas debe estar encapsulado en un método estático reutilizable con la siguiente firma:
   public static double calcularPromedioPonderado(double[] notas, double[] pesos)

Formato de respuesta:

1. Explica brevemente la estructura del diseño y los métodos antes de presentar el código.
2. Presenta todo el código fuente listo para ejecutar dentro de un único archivo Java con la clase principal 'ModuloAcademico.java'.

## Tecnicas usadas en el prompt final

| Componente / Técnica                  | Texto de mi prompt final                                                                                                          |
| ------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------- |
| **Role Prompting**                    | `Actúa como un arquitecto de software especializado en Java.`                                                                     |
| **Contexto**                          | `Diseña un módulo académico completo para un sistema de gestión universitaria.`                                                   |
| **Prompt Estructurado / Instrucción** | `Crear una interfaz gráfica interactiva con Java Swing que solicite al usuario los datos de un estudiante, 3 notas...`            |
| **Restricción**                       | `1. Utiliza únicamente librerías estándar del JDK... 2. Implementa manejo de excepciones (Try-Catch)...`                          |
| **Few-Shot / Ejemplo**                | `public static double calcularPromedioPonderado(double[] notas, double[] pesos)`                                                  |
| **Formato de Salida**                 | `1. Explica brevemente la estructura... 2. Presenta todo el código fuente listo para ejecutar dentro de un único archivo Java...` |

## Evaluacion del resultado

| Criterio                                                                            | Cumple (Sí / No) |
| ----------------------------------------------------------------------------------- | ---------------- |
| ¿Está escrito en Java Swing utilizando únicamente librerías estándar del JDK?       | Sí               |
| ¿Realiza las validaciones de rango (0-20), campos vacíos y texto con `JOptionPane`? | Sí               |
| ¿Calcula el promedio ponderado y clasifica en 'Aprobado' o 'Desaprobado'?           | Sí               |
| ¿Sigue la firma del método de ejemplo y el formato de salida solicitado?            | Sí               |

## Por que elegi estas tecnicas

Combinar Role Prompting, Prompt Estructurado y Ejemplos de Firma de Método (Few-Shot) resulta esencial para el desarrollo de software. Al asignarle a la IA un rol de arquitecto de software, se condiciona la respuesta a seguir buenas prácticas de programación estructurada. Delimitar las restricciones de captura de excepciones (Try-Catch) evita que el programa se caiga por entradas inválidas del usuario, y especificar el formato exacto de salida garantiza un código modular y directamente ejecutable sin necesidad de hacer ajustes manuales.

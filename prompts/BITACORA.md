# Bitacora de tecnicas avanzadas

Laboratorio 07: Tecnicas Avanzadas de Prompting.
Herramienta de IA usada: (escribe aqui cual usaste)

## Ejercicio 2: Zero-shot, one-shot y few-shot

| Tipo      | Aciertos (de 5) | Formato de la respuesta                                             | Todas con el mismo formato (Si/No) |
| --------- | --------------- | ------------------------------------------------------------------- | ---------------------------------- |
| Zero-shot | 5               | Lista con explicaciones detalladas e viñetas adicionales.           | NO                                 |
| One-shot  | 5               | Lista numerada imitando el formato del ejemplo.                     | SI                                 |
| Few-shot  | 5               | Líneas directas en formato "Texto" -> Etiqueta sin texto adicional. | SI                                 |

## Ejercicio 3: Chain of Thought

| Pedido      | Respuesta de la IA                                                                  | Muestra los pasos (Si/No) | Correcta (Si/No) |
| ----------- | ----------------------------------------------------------------------------------- | ------------------------- | ---------------- |
| Directo     | 318.60                                                                              | NO                        | SI               |
| Paso a paso | Muestra cálculo de descuento, IGV, costo por 3 unidades y comprobación (S/ 318.60). | SI                        | SI               |

## Ejercicio 4: Role prompting

| Version        | Vocabulario (sencillo/tecnico) | Usa ejemplos o codigo                                                       | A quien le sirve mas                                       |
| -------------- | ------------------------------ | --------------------------------------------------------------------------- | ---------------------------------------------------------- |
| A. Sin rol     | Intermedio / Genérico          | Conceptos básicos sin fragmentos de código específicos.                     | Público general con conocimientos básicos de tecnología.   |
| B. Rol docente | Sencillo y analógico           | Ejemplos cotidianos (una caja con etiqueta para guardar cosas).             | Estudiantes principiantes o personas sin formación previa. |
| C. Rol senior  | Técnico avanzado               | Tipos de datos Java, asignación de memoria en Stack/Heap y alcance (scope). | Desarrolladores junior o compañeros de equipo técnico.     |

## Ejercicio 5: Descomposicion

| Paso   | Prompt / Tarea               | Resultado / Salida                                                                                        |
| ------ | ---------------------------- | --------------------------------------------------------------------------------------------------------- |
| Paso 1 | Identificación de requisitos | 5 requisitos principales del sistema (registro, consulta, actualización de stock, alertas y movimientos). |
| Paso 2 | Diseño de clases             | Modelado de clases (`Producto`, `Inventario`, `Proveedor`) con atributos y tipos de datos.                |
| Paso 3 | Código fuente                | Generación de la clase ejecutable `Producto.java` con constructor, getters y setters.                     |
| Paso 4 | Revisión / Mejoras           | Identificación de 3 mejoras: validación de valores negativos, `toString()` e inmutabilidad de ID.         |

| Criterio                  | Solicitud única (Sin descomponer) | Solicitud paso a paso (Descomposición)                 |
| ------------------------- | --------------------------------- | ------------------------------------------------------ |
| **Coherencia del código** | Genérico y superficial            | Estructurado, modular y alineado al diseño previo      |
| **Control de calidad**    | Respuestas imprecisas             | Permite auditar y corregir cada etapa incrementalmente |

## Ejercicio 6: Prompt estructurado y autocritica

| ID   | Escenario                          | Datos de entrada                | Resultado esperado                             | Estado       |
| ---- | ---------------------------------- | ------------------------------- | ---------------------------------------------- | ------------ |
| TC01 | Login exitoso                      | usuario@test.com / Pass123!     | Acceso concedido.                              | Original     |
| TC02 | Bloqueo por 3 intentos fallidos    | usuario@test.com / Wrong (x3)   | Cuenta bloqueada.                              | Original     |
| TC07 | Campos vacíos                      | "" / ""                         | Validación en cliente: "Campos requeridos".    | **Agregado** |
| TC08 | Formato de correo inválido (sin @) | usuariotest.com / Pass123!      | Error: "Formato de correo no válido".          | **Agregado** |
| TC09 | Contraseña con espacios en blanco  | usuario@test.com / " Pass123! " | Rechazo o recorte según política de seguridad. | **Agregado** |

| Qué revisar                                      | Cumple (Sí / No) |
| ------------------------------------------------ | ---------------- |
| ¿Tiene las 4 columnas pedidas?                   | Sí               |
| ¿Incluye el bloqueo después de 3 intentos?       | Sí               |
| ¿Incluye casos con campos vacíos?                | Sí               |
| ¿Indica qué casos agregó en la autocrítica?      | Sí               |
| ¿Hay algún caso repetido o que no tenga sentido? | No               |

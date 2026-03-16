Documentación de Validación XML mediante Esquemas XSD y Expresiones Regulares
Este proyecto presenta la implementación de un sistema de validación de datos para usuarios de una aplicación web, cumpliendo con los objetivos de aprendizaje del RA 4. El propósito principal es garantizar la integridad y el formato correcto de la información mediante restricciones definidas en un esquema XSD. 
Metodología e Implementación Técnica
Para la validación de los elementos, se han integrado restricciones basadas en facetas de patrón (xs:pattern), utilizando expresiones regulares (RegEx) testeadas en la herramienta Regex101.
Análisis de Restricciones Aplicadas:
Identificador de Usuario (nombreUsuario): Se ha definido un patrón que exige el inicio de la cadena con un carácter alfabético en minúscula, permitiendo una combinación posterior de caracteres alfanuméricos y guiones bajos conforme a los estándares de nomenclatura comunes.
Gestión de Correo Electrónico (email): Implementación de una expresión regular que valida la estructura sintáctica estándar (RFC 5322), asegurando la presencia de un identificador, el símbolo "@" y un dominio válido.
Telefonía (telefono): Restricción ajustada al plan de numeración nacional de España, validando secuencias de 9 dígitos que comienzan por los rangos oficiales (6, 7, 8 o 9) y permitiendo opcionalmente el prefijo internacional +34.
Codificación Postal (codigoPostal): El esquema limita la entrada a un patrón de exactamente 5 dígitos, restringiendo el primer valor al rango [0-5] para ajustarse a la división provincial de España.
Seguridad de Acceso (contrasena): Se ha optado por un estándar de alta seguridad que requiere una longitud mínima de 8 caracteres, incluyendo obligatoriamente mayúsculas, minúsculas, dígitos y caracteres especiales (símbolos) para prevenir vulnerabilidades.

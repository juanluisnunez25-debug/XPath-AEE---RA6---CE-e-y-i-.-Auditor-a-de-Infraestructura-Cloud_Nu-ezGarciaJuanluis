# Respuestas al Reto de Refactorización TechNova Cloud v2.0

### [cite_start]a) ¿Cuántas líneas de código habéis ahorrado al usar grupos? [cite: 43]
Al utilizar `xs:attributeGroup` y `xs:group`, hemos centralizado la definición de 3 atributos y 4 elementos de hardware. En este ejemplo con dos servidores, el ahorro es pequeño, pero en un entorno real con 50 servidores, ahorraríamos aproximadamente **250 líneas de código** al no tener que repetir las definiciones dentro de cada etiqueta `<servidor>`.

### [cite_start]b) ¿Qué error os da VS Code si intentáis poner dos servidores con el mismo ID? [cite: 44]
Si duplico el ID `srv-web-01`, VS Code subraya el error en rojo y muestra el siguiente mensaje:
`"Identity constraint 'UnicoID' failed: duplicate key value [srv-web-01] found for element 'catalogo_cloud'."`
[cite_start]Esto confirma que la restricción `<xs:unique>` funciona correctamente[cite: 37].

# Que es Oletools

Oletools es es un conjunto de herramientas programadas en python que sirven para analizar documentos de tipo OLE. Es una herramienta bastante similar a la ViperMonkey solo que esta es mas sencilla ya que hay funciones que no tiene como la de coger todo el payload en base64 y mostrarlo. La información que muestra es el código visual basic de la macro sin necesidad de ejecutarla.

Oletools esta compuesto por las herramientas: Oleid, olevba, MacroRaptor, msodde, pyxswf, oleobj, rtfobj, olebrowse, olemeta, oletimes, oledir y olemap.

## Como funciona olevba

Olevba es la herramienta principal de Oletools. Una vez ejecutado Olevba, esta te extrae el código fuente de la macro escrito en visual basic.

![Macro](/images/macro_payload.png)

Este ejemplo indica que al abrir el documento con Document_Open() se ejecutaría toda la cadena en base64

Lo siguiente que muestra es una tabla de indicadores de compromiso de lo que ejecuta la macro

![IOC1](/images/IOC_table.png)

En este ejemplo se puede ver que que hay funciones en base64, que es cierto ya que toda la macro está con el encoding base64. También hay una función Call al principio de la macro que parece que está llamando a la siguiente función. Luego hay otra función que se llama showwindow que puede esconder o mostrar ventanas.
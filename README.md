## Bases de datos:

Cuando nos conectemos a Odoo, nos pedirá crear una base de datos, en mi caso crearé dos, una con datos demo y otra real:

Con la demo activada:

![Captura de pantalla 2026-11-11 135635.png](fotos/Captura%20de%20pantalla%202026-11-11%20135635.png)

Base de datos sin demo:

![Captura de pantalla 2026-11-11 135832.png](fotos/Captura%20de%20pantalla%202026-11-11%20135832.png)

---

## Ejercicio 1 · Tipos de producto:

Para ello tendremos que ir a ventas y en la barra de búsqueda podremos ir filtrando por los distintos tipos de productos, viendo sus respectivos precios e IVAs asociados al tipo de producto, como por ejemplo los siguientes:

De tipo bien con un IVA del 21%, con seguimiento de stock:

![Captura de pantalla 2026-11-11 140744.png](fotos/Captura%20de%20pantalla%202026-11-11%20140744.png)

De tipo bien con un IVA del 21%, sin seguimiento de stock:

![Captura de pantalla 2026-11-11 141222.png](fotos/Captura%20de%20pantalla%202026-11-11%20141222.png)

De tipo servicio con un IVA del 21%:

![Captura de pantalla 2026-11-11 140843.png](fotos/Captura%20de%20pantalla%202026-11-11%20140843.png)

De tipo combinación el cual no tiene IVA:

![Captura de pantalla 2026-11-11 140857.png](fotos/Captura%20de%20pantalla%202026-11-11%20140857.png)

---

## Ejercicio 2 · Recorrido:

Lo primero será ir al apartado de contactos:

![Captura de pantalla 2026-11-11 141327.png](fotos/Captura%20de%20pantalla%202026-11-11%20141327.png)

Dentro agregaremos al nuevo cliente el cual va a ser la empresa CPR Daniel, al cual le asignaremos todos sus datos de empresa; a su vez, esta empresa tendrá asociado un contacto el cual es secretaría, ya que es un departamento específico de la compañía.

![Captura de pantalla 2026-11-11 141906.png](fotos/Captura%20de%20pantalla%202026-11-11%20141906.png)

Ahora también tendremos que crear los productos que necesita la empresa; para ello iremos a ventas y al apartado productos, y crearemos dos nuevos:

El primero es un servicio que se llama "hora de soporte" (quiero aclarar que en la captura me equivoqué y puse que es un bien y tiene el 21% de IVA de bienes y no el de servicios):

![Captura de pantalla 2026-11-11 142014.png](fotos/Captura%20de%20pantalla%202026-11-11%20142014.png)

El segundo es un bien el cual es un libro técnico con un 4% de IVA:

![Captura de pantalla 2026-11-11 142101.png](fotos/Captura%20de%20pantalla%202026-11-11%20142101.png)

Para poder hacer el presupuesto tendremos que ir a ventas > pedidos > presupuesto. Una vez dentro tendremos que ir asignándole los datos del cliente y agregar los productos.
*Importante:* en el apartado de "otra información" hay un apartado de almacenes en el cual pondremos el almacén de nuestra empresa. Es importante ponerlo, ya que sino nos dará un error.

![Captura de pantalla 2026-11-11 142230.png](fotos/Captura%20de%20pantalla%202026-11-11%20142230.png)

Una vez le demos a enviar se autogenerará un presupuesto para enviárselo a la empresa:

![Captura de pantalla 2026-11-11 142454.png](fotos/Captura%20de%20pantalla%202026-11-11%20142454.png)

Una vez lo enviemos, ya podremos confirmar el pedido:

![Captura de pantalla 2026-11-11 143611.png](fotos/Captura%20de%20pantalla%202026-11-11%20143611.png)

Y por último, ya confirmado, podremos pasar a crear la factura:

![Captura de pantalla 2026-11-11 143618.png](fotos/Captura%20de%20pantalla%202026-11-11%20143618.png)

Con esto la factura quedará registrada y podremos enviarla:

![Captura de pantalla 2026-11-11 143806.png](fotos/Captura%20de%20pantalla%202026-11-11%20143806.png)

Foto de la factura:

![Captura de pantalla 2026-11-11 143828.png](fotos/Captura%20de%20pantalla%202026-11-11%20143828.png)

Y una vez sea pagado por la empresa, podremos marcar el presupuesto como pagado:

![Captura de pantalla 2026-11-11 144120.png](fotos/Captura%20de%20pantalla%202026-11-11%20144120.png)

---

## Ejercicio 3 · Búsqueda guardada:

Para poder realizar la búsqueda de facturas publicadas, agrupadas por cliente y del favorito, tendremos que desplegar la flecha de la derecha de la barra de búsqueda, ya que ahí se encuentran los filtros de búsqueda. Los que usaremos en nuestro caso es el de registrado, socio, y marcaremos favorito y luego a guardar.

![Captura de pantalla 2026-11-11 145438.png](fotos/Captura%20de%20pantalla%202026-11-11%20145438.png)

Una vez hecho eso veremos que se encuentran divididas las facturas y agrupadas:

![Captura de pantalla 2026-11-11 145507.png](fotos/Captura%20de%20pantalla%202026-11-11%20145507.png)

---

## Ejercicio 4 · Modo desarrollador: capturas de las dos vías de activación y tabla con los nombres técnicos.


Para activar el modo de desarrollador hay dos formas:

La primera es tan fácil como en la URL escribir al final de todo `?debug=1`. Sabremos que está bien cuando veamos el símbolo de un bicho en la parte superior derecha; esto nos permite ver más información sobre los campos del formulario.

Podemos ver en la URL cómo está puesto el debug:

![Captura de pantalla 2026-11-11 150116.png](fotos/Captura%20de%20pantalla%202026-11-11%20150116.png)

La otra forma es desde ajustes, buscaremos abajo del todo un apartado que sea herramientas de desarrollador y le daremos al botón de "activar modo desarrollador".

![Captura de pantalla 2026-11-11 175227.png](fotos/Captura%20de%20pantalla%202026-11-11%20175227.png)

## Tabla con los nombres técnicos.

| Nombre | Nombre técnico | Modelo |
| :--- | :--- | :--- |
| Nif | vat | res.partner |
| Socio | partner_id | account.move |

## Incidencias

Como tal, problemas grandes a destacar no tuve, ya que si había algo que no encontraba lo buscaba o preguntaba a compañeros.

| Fecha | Problema | Solución |
| :--- | :--- | :--- |
| 11/11/2026 | Mi único problema fue que el precio interno de los productos fui incapaz de cambiarlo a euros, ya que sale en dólares. | Sin solución encontrada. |

## Declaración de uso de IA

Para lo único que he usado la IA es que no sabía cómo poner mi almacén en la propuesta de venta a la empresa, así que recurrí a preguntar a la IA cómo se hacía para agregarlo, y ya me explicó que es en el apartado que explico previamente en el ejercicio 2.
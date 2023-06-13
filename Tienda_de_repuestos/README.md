# Tienda de repuestos

### Credenciales de superusuario:
username: fawzi  
password: 123

### Credenciales de cliente (no superusuario ni acceso a administrador):
username: prueba  
password: casa4321

<br>

Una vez habiendo ingresado y recorrido la página de inicio, en la barra de navegación seleccionar **"Tienda"** para acceder a la tienda virtual. Tambien puede acceder desde el boton que se encuentra en el cuerpo de la web.

Allí puede observarse el catálogo completo de productos en el cual puede realizarse una búsqueda utilizando el **buscador** allí presente. Si bien las imagene estan dentro del proyecto, todavía el path de las mismas no esta referenciado correctamente, por lo que las mismas no se muestran.

Podemos acceder al **formulario de creación de usuario** en la sección superior derecha, sobre la navbar presionando en el boton **"Registrar"**. Al crear un nuevo usuario respetar las condiciones requeridas en los campos, dado que todavía no se encuentran implementados los mensajes de error.  
Una vez creado el usuario, usted será redirigido a la página principal de nuestro catálogo de productos con la sesión logueada. Una vez logueado, los botones presentes en la navbar cambian de *Iniciar sesión* y *Registrarse*, a un saludo a su username ("Hola {{username}}") y un boton para desloguarse llamado **Cerrar sesión**.

Los usuarios creados se almacenarán en la tabla *"auth_user"* que utiliza Django para manejar usuarios, dado que esta trae varias funcionalidades importantes realacionadas a manejo de sesiones. Los datos adicionales (DNI, telefono y dirección) se almacenarán en la tabla (modelo) *"App_Tienda_de_repuestos_client"* la cual posee dichas columnas, además de una columna llamada *"user_id"* la cual es una clave foranea que permite relacionar one-one dicha tabla con la tabla de usuarios de Django.

Para desloguearse simplemente presione *"Cerrar sesión*" y los botones volverán a ser *Iniciar sesión* y *Registrarse*. Solo basta con pulsar *Iniciar sesión* para acceder al **formulario de inicio de sesión** el cual se encargará de validar los datos ingresados con los que se encuentran en la tabla de usuarios e **insertar la fecha de ultimo logeo**.


En la navbar puede encontrar el botón de *Carrito* en el cual se almacenarán todos los productos que usted ha seleccionado *"Añadir al carrito"*. En él podrá visualizar los productos agregados y sumar o restar cantidades. Si el producto se encuentra con cantidad "1" y usted resta una unidad, el mismo desaparecerá del carrito. El carrito de compras recuerda los articulos y cantidad que fueron seleccionados dado que utiliza **Variables de contexto** o **Context_processor**, por lo que puede navegar por el sitio y luego volver, puediendo visualizar todos los items tal cual los tenía. 
El resto de funcionalidades del carrito de compras se encuentran en desarrollo.  
En el futuro se pretende que una vez se confirmen los articulos (y sus respectivas cantidades) en el carrito de compras se genere un pedido en la tabla *App_Tienda_de_repuestos_orders*, no obstante, esta funcionalidad todavía se encuentra en desarrollo.

Se creará una tabla especifica llamada *Contact* (*Pages_contact*) la cual almacenará las consultas que realizan los clientes en la pagina *Index* a través de su formulario correspondiente al pie de la página. Esta tabla se crea especificamente para poder cumplir con los requisitos de la preentrega (al menos 3 tablas con formularios que carguen información en éstas), dado que en futuro se tiene la intención de que cuando el cliente realice una consulta, la misma se envíe directamente por email a la dirección especificada.

<br>

# Requisitos de la "Tercera pre-entrega"

## Herencia HTML:

Puede observarse herencia de plantillas en la página del carrito de compras, la cual hereda desde la plantilla base.html ubicada en la aplicación de App_Tienda_de_repuestos

<br>

## Por lo menos 3 clases en models.py:
En el archivo models.py pueden encontrarse 4 clases (tablas) que conforman la base de datos de nuestro proyecto:
* **Product**: *App_Tienda_de_repuestos_product*
* **Client**: *App_Tienda_de_repuestos_client*
* **Orders**: *App_Tienda_de_repuestos_order*
* **Contact**: *Pages_contact*

<br>

## 3 formularios que escriben en (por lo menos 3) tablas: 

* **formulario de creación de usuario**: escribe en **Users.Django** y **App_Tienda_de_repuestos_client**.

* **formulario de inicio de sesión**: escribe en la tabla **Users.Django** (último inicio de sesión).

* **formulario de contacto**: escribe en la tabla **Contact** las consultas de los clientes.

<br>

## Buscador de productos:
**Buscador de productos** en la página principal de la tienda.

<br>

## Readme.md:
En el presente documento informativo pueden observarse algunas de las funcionalidades presentes en el proyecto, asi como sus indicaciones de uso y futuras implementaciones.

<br>
<br>

### El presente documento así como todos el proyecto se encontrará subido en mi repositorio de GitHub bajo el nombre de *"Tercera pre-entrega+El Gamal"*.

<br>

*Gracias por su atención.*

<br>

# *Copyright Fawzi El Gamal © 2023*





En caso de estar interesado en aplicar al test puede contactar por correo a [lsilva@deacero.com](mailto:lsilva@deacero.com)
.

Todas las respuestas pueden hacerse en un documento con la herramienta que mejor le convenga. El dashboard puede ser publicado en tableu public y agregar la liga o presentar el reporte en archivo PDF o HTML.

Una vez concluido el reto se debe comunicar al correo correspondiente con la liga al repositorio de github final para evaluar las respuestas.

Suerte a todos!!! 🤘 🤓 💻


<center> <h1></h1> </center>

<center> <h1>SQL SERVER - EXAMEN DE CONOCIMIENTO</h1> </center>

<center><h2>Examen Práctico</h2> </center>

Adjunto a este examen se encuentra un documento Excel llamado &quot;Examen Práctico&quot; en el cual cada hoja del documento hace referencia a una tabla SQL, tomando como base este documento, conteste lo siguiente

Que script se utilizaría para conocer el dato de:

  1. Insertar un registro en la tabla _Tbl\_Recuperacion_

  2. Eliminar de la tabla Dim\_Cliente los registros de los clientes que pertenezcan al AgrupadorCliente 543.

  3. Conocer el valor Total de ImpRecuperacion e ImpObjetivo por cliente correspondiente al año anterior (2020).

  4. Conocer el valor de %ImpRecuperacion utilizando la fórmula: ImpRecuperacion/(ImpObjetivo(Mes Anterior)-ImpBonificacion)



  5.  Utilizando la herramienta Tableau diseñe un dashboard que represente los datos de: 
  **ImpRecuperacion, ImpObjetivo e ImpBonificaciones** de cada cliente y por periodo mensual. 

> Sobre la página oficial de Tableau puede descargar la versión de prueba, la liga de descarga es: <center>https://www.tableau.com/support/releases/desktop/2021.1.1</center>

  6. Adjunto a este examen se encuentra un documento .txt llamado &quot;SP&quot;, este contiene un Stored Procedure que se utiliza para generar las estrellas, mencione que es lo que realiza el procedimiento y que resultado arroja.

  7. Cuenta con un archivo de tipo XML llamado Ventas.EsquemaFacturas

 - Usted necesita declarar una variable de tipo XML llamada XML1.
 - La solución deberá asegurar que XML1 ésta validada para utilizarse por Ventas.EsquemaFacturas
       
 8. Necesitas desplegar los registros de la tabla &quot;Ordenes&quot; para los Clientes de forma secuencial, considerando el formato XML como a continuación se visualiza:

<row OrdenID = “1” FechaOrden = “2016-01-01 23:59” Total = “2800.00” Nombre = “Cliente A” País = ‘México” />
<row OrdenID = “2” FechaOrden = “2016-02-01 20:00” Total = “3200.00” Nombre = “Cliente B” País = ‘México” />

¿Cuál de las siguientes T-SQL debería usar?

**a.** SELECT OrdenID, FechaOrden, Total, Nombre, Pais FROM Ordenes INNER JOIN Clientes ON Ordenes.ClienteID = Clientes.ClienteID WHERE Clientes.ClienteID = 1

FOR XML RAW

**b.** SELECT OrdenID, FechaOrden, Total, Nombre, Pais FROM Ordenes INNER JOIN Clientes ON Ordenes.ClienteID = Clientes.ClienteID WHERE Clientes.ClienteID = 1

FOR XML RAW, ELEMENTS

**c.** SELECT OrdenID, FechaOrden, Total, Nombre, Pais FROM Ordenes INNER JOIN Clientes ON Ordenes.ClienteID = Clientes.ClienteID WHERE Clientes.ClienteID = 1

FOR XML AUTO

**d.** SELECT OrdenID, FechaOrden, Total, Nombre, Pais FROM Ordenes INNER JOIN Clientes ON Ordenes.ClienteID = Clientes.ClienteID WHERE Clientes.ClienteID = 1

FOR XML RAW, AUTO

  9. Necesitas crear una tabla con el siguiente nombre &quot;DetalleOrdenes&quot;. Esta deberá reunir los siguientes requerimientos:

**a.** Escribir a disco el resultado
**b.** Contener una columna llamada TotalPorItem que almacene por cada producto el Precio de lista por la cantidad de la tabla Productos.

¿Cuál de los siguientes T-SQL deberá utilizar?

    CREATE TABLE DetalleOrdenes (PrecioLista money not null, Cantidad int not null,
    
    TotalPorItem as (PrecioLista \* Cantidad) PERSISTED TO DISK)
    
    CREATE TABLE DetalleOrdenes (PrecioLista money not null, Cantidad int not null,
    
    TotalPorItem as (PrecioLista \* Cantidad) PERSISTED)
    
    CREATE TABLE DetalleOrdenes (PrecioLista money not null, Cantidad int not null,
    
    TotalPorItem as (PrecioLista \* Cantidad) TO DISK)

  10. Una aplicación comienza a presentar lentitud, usted descubre que una gran cantidad de memoria es consumida por un simple query dinámico.

Necesitas reducir el procedimiento cache de los querys sin la necesidad de crear ningún índice adicional.

¿Cuál opción deberá elegir para mejorar esto?

**a.** Add a HASH hint to the query
**b.** Add a LOOP hint to the query
**c.** Add a FORCESEEK hint to the query
**d.** Add an INCLUDE clause to the index
**e.** Add a FORCESCAN hint to the Attach query
**f.** Add a COLUMNSTORE index to cover the query
**g.** Enable the optimize for ad hoc workloads option
**h.** Cover the unique clustered index with a COLUMNSTORE index
**i.** Include a SET FORCEPLAN ON statement before you run the query
**j.** Include a SET STATISTICS PROFILE ON statement before you run the query
**k.** Include a SET STATISTICS SHOWPLAN\_XML ON statement before you run the query
**l.** Include a SET TRANSACTION ISOLATION LEVEL REPEATABLE READ statement before you run the query

  11. Usted tiene las siguientes definiciones en dos tablas:

| | |
| --- | --- |
| **CREATE TABLE CLIENTES** (ClientID INT NOT NULL PRIMARY KEY,Nombrecliente VARCHAR(100) NOT NULL, Direccion VARCHAR(100) NOT NULL) | **CREATE TABLE ORDENES** (OrdenID INT NOT NULL PRIMARY KEY, ClienteID INT NOT NULL, DescripcionOrden VARCHAR(200)) |

Usted necesita asegurar que la columna ClienteID en la tabla &quot;Ordenes&quot; contiene solo valores que existen en la columna ClienteID de la Tabla Clientes.

¿Cuál de las T-SQL deberá utilizar?

**a.** ALTER TABLE CLIENTES ADD CONSTRAINT FX\_Clientes\_ClienteID FOREIGN KEY (ClienteID) REFERENCES Ordenes (ClienteID)

**b.** ALTER TABLE ORDENES ADD CONSTRAINT FX\_Ordenes\_ClienteID FOREIGN KEY (ClienteID) REFERENCES Clientes (ClienteID)

**c.** ALTER TABLE ORDENES ADD CONSTRAINT CK\_Ordenes\_ClienteID CHECK (ClienteID IN SELECT ClienteID FROM Clientes))

**d.** ALTER TABLE ORDENES ADD CONSTRAINT FK Ordenes ClienteID PRIMARY KEY (ClienteID)

  12. Usted crea una tabla que tiene las columnas ProductoID, DescripcionCodigo y Totales, registra una marca a mitad de año para los productos en esa tabla.

La tabla tiene totales obtenidos por 50 productos para varias marcas.

Usted Necesita recuperar productos que obtuvieron los totales más altos para cada marca junto con el detalle de los totales.

¿Cuál de los T-SQL deberá utilizar?

  **a.** SELECT ProductID AS Code, RANK() OVER(Order BY avg(Marcas) DESC) AS Value

FROM ProductosMarcados GROUP BY ProductID

  **b.** SELECT ProductID, Nombre, Marca DENSE\_RANK() OVER(Order BY Marcas DESC) AS Rank

FROM ProductosMarcados

  **c.** SELECT ProductID as Code, DENSE\_RANK() OVER(Order BY avg(Marcas) DESC) AS Value

FROM ProductosMarcados GROUP BY ProductID

  **d.** SELECT ProductID as Code, NTILE(2) OVER(Order BY avg(Marcas) DESC) AS Value

FROM ProductosMarcados

GROUP BY ProductID

  **e.** SELECT ProductID as Code, Marcas as Value

FROM (SELECT ProductoID, Marcas AS Marcas,RANK() OVER(PARTITION BY DescripcionCodigo ORDER BY Marcas ASC) AS Rank FROM ProductosMarcados) tmp

WHERE Rank = 1

**f.** SELECT ProductID as Code, Marcas as Value

FROM (SELECT ProductoID, Marcas AS Marcas,RANK() OVER(PARTITION BY DescripcionCodigo ORDER BY Marcas DESC) AS Rank

FROM ProductosMarcados) tmp

WHERE Rank = 1

**g.** SELECT ProductID as Code, Marcas as Value

FROM (SELECT ProductoID, Marcas AS Marcas,RANK() OVER(PARTITION BY ProductoID ORDER BY Marcas ASC) AS Rank FROM ProductosMarcados) tmp

WHERE Rank = 1

  13. Usted comprueba que durante periodos se detectan picos altos en consumo de CPU, ciertas operaciones están tomando más tiempo que el esperado. Al parecer el problema son bloqueos.

Usted necesita reunir más datos para determinar cuáles procesos están bloqueando y poder identificar la causa-raíz. ¿Qué debemos hacer?

  **a.** Comenzar un trace utilizando SQL Server Profile para cachar el evento Deadlock

  **b.** Utilizar SP\_CONFIGURE y poner un parámetro para el proceso bloqueado y Comenzar un Trace con el SQL Server Profile para cachar el proceso bloqueado.

  **c.** Programar un JOB en el agente y ejecutarlo cada 60 segundos e insertar los resultados de la ejecución de la vista dinámica sys.dm\_os\_wait\_stats dentro de una tabla.

  **d.** Utilizar el sistema de monitoreo para cachar el evento: Lock Waits/sec

  14. Detecta que el índice &quot;IDX\_TransaccionProductos\_CodidoTransaccion&quot; es pobre debido a una alta fragmentación.

Usted necesita desfragmentar el índice y asegurar que los querys en uso son capaces de indexar durante el proceso de fragmentación. ¿Cuál opción deberá utilizar?

**a.** ALTER INDEX ALL ON TransaccionProductos REBUILD

**b.** ALTER INDEX IDX\_TransaccionProductos\_CodidoTransaccion ON TransaccionProductos\_CodidoTransaccion REORGANIZE

**c.** ALTER INDEX IDX\_TransaccionProductos\_CodidoTransaccion ON TransaccionProductos\_CodidoTransaccion REBUILD

**d.** CREATE INDEX IDX\_TransaccionProductos\_CodidoTransaccion ON IDX\_TransaccionProductos\_CodidoTransaccion WITH DROP EXISTING

  15. Hay alta contención de Lecturas/Escrituras en varias tablas utilizadas por su transacción.

Usted necesita minimizar el espacio en la base de datos TEMPDB.

¿Cuál nivel de ISOLATION deberá utilizar?

**a.** SERIALIZABLE
**b.** SNAPSHOT
**c.** READ COMMINTTED SNAPSHOT
**d.** REPEATABLE READ




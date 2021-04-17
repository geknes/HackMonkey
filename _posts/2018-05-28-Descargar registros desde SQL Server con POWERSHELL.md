---
layout: post
active: blog
title: Descargar registros desde SQL Server con POWERSHELL
date: 2018-05-28
categories: [programación ,powershellaventura, aventura]
---

{:class="parrafo-imagen"}
![image-title-here](https://images.unsplash.com/photo-1590615368995-77191aa9e571?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=784&q=80){:class="img-responsive"}


{:class="img-referencia"}
Foto de [Ehimetalor Akhere](https://unsplash.com/@theeastlondonphotographer) en [Unsplash](https://unsplash.com)
<!-- Referencia de la foto -->

{:id="_parrafo"}
Bienvenido a mi primer artículo donde te enseñaré a descargar una tabla de registros desde SQL server a CSV con Powershell.


## Aquí el código en Powershell

```Powershell

#Cadena de conexión
$BaseDeDatos = "DB_Ejemplo"
$Servidor = "Servidor_Ejemplo"

#Archivo a exportar
$AttachmentPath1 ='D:\archivo.csv'


# Escribe tu sentencia SQL para extraer tu tabla
$SqlQuery1 = "Select * From Tu_Tabla"

$SqlConnection = New-Object System.Data.SqlClient.SqlConnection
$SqlConnection.ConnectionString = "Server = $Servidor; Database = $BaseDeDatos; Integrated Security = True"
$SqlCmd = New-Object System.Data.SqlClient.SqlCommand
$SqlCmd.CommandText = $SqlQuery1
$SqlCmd.Connection = $SqlConnection
$SqlAdapter = New-Object System.Data.SqlClient.SqlDataAdapter
$SqlAdapter.SelectCommand = $SqlCmd
$DataSet = New-Object System.Data.DataSet
$nRecs = $SqlAdapter.Fill($DataSet)
$nRecs | Out-Null
#Populate Hash Table
$objTable = $DataSet.Tables[0]
#Export Hash Table to CSV File
$objTable | Export-CSV $AttachmentPath1 -NoTypeInformation
```

Espero les sirva :)

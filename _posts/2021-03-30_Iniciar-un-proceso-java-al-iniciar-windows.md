---
layout: post
active: blog
title: Hola mundo - Powershell
categories: [programación ,powershell]
---

{:class="parrafo-imagen"}
![image-title-here](https://images.unsplash.com/photo-1499951360447-b19be8fe80f5?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=750&q=80){:class="img-responsive"}


{:class="img-referencia"}
Foto de [Autor](https://) en [Lugar de donde salió](https://)
<!-- Referencia de la foto -->

{:id="_parrafo"}
Hay muchas maneras de obtener un mismo resultado cuando trabajamos con Powershell. 

Veamos un ejemplo sencillo con el cual todo buen programador empieza en este mundo de codigos.

Humanity’s struggle to locate the easy button permeates all aspects of our existence. In the context of the financial markets, everyone wants to find that expert, newsletter, or secret trading program that if followed will lead to instant, risk-free and above-average sick GAINZ. Intrinsically, we all know that said button is a fleeting chimera one chases at one’s peril — and yet, I continually get asked “What coins should I buy”, “Is now a good time to buy”, “Does technical analysis work”, and on and on. I don’t offer such opinions even to my closest friends lest they erroneously believe I’m the oracle of the Kampong.

*Aquí el código en powershell*

```powershell
> Write-Host "Hola Mundo!"
"Hola Mundo!"
```
Usamos Write-Host para imprimir el texto "Hola mundo!"

Veamos un ejemplo más de como se puede hacer lo mismo utilizando Write-Output 

*Aquí el código en powershell*

```powershell
> Write-Output "Hola Mundo!"
"Hola Mundo!"
```

Vale la pena señalar que aunque Write-Output y Write-Host muestran un texto en la pantalla, hay una sutil diferencia. Write-Host escribe solo en la salida estándar (es decir, la pantalla de la consola), mientras que Write-Output escribe tanto en la salida estándar como en la secuencia de salida [éxito] permitiendo utilizar este valor nuevamente. Esto permite que la salida de un comando se dirija como entrada a otro, incluida la asignación a una variable.

*Veamos*

```powershell
> $mensaje = Write-Output "Hola Mundo!"
> $mensaje
"Hola Mundo!"
```

*Y por último tambien podríamos tipear directamente para mostrar el texto en la pantalla*

```powershell
> "Hola Mundo!"
"Hola Mundo!"
```







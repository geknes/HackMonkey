---
layout: post
active: blog
title: Insertar o Adjuntar un archivo de Excel en Word con Python
date: 2018-07-10
categories: python
---

{:class="parrafo-imagen"}
![image-title-here](https://images.unsplash.com/photo-1561409625-df3c51c39c2f?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=1375&q=80){:class="img-responsive"}


{:class="img-referencia"}
Foto de [Bahman Adlou](https://unsplash.com/@drbabooli) en [Unsplash](https://unsplash.com/photos/hGV2TfOh0ns)


{:id="_parrafo"}
Estaba buscando una manera de poder adjuntar un archivo dentro de un documento de word con python y encontré una librería que trabaja con archvos .docx pero que no me fue de mucha ayuda.

Al final logré adjuntar el archivo Excel en Word con la ayuda de la librería win32com. No encontré mucha documentación pero que en la siguiente [página](https://msdn.microsoft.com/en-us/vba/word-vba/articles/object-model-word-vba-reference) pude encontrar metodos que son compatibles a la hora de usar la librería win32com con python.

## Aquí el código en Python

<script src="https://gist.github.com/geknes/3d6b5817c3cd4764ba6ffbbe7fa6e9f1.js"></script>

Espero les sirva :)
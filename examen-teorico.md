# Preguntas teóricas

1. **¿Qué es _Python_?**

**_Python_** es un lenguaje de programación interpretado, multiplafatorma y débilmente tipado.

2. **¿Por qué _Python_ es mejor que _Java_?**

La pregunta está mal formulada, ya que se asume que _Python_ es mejor que _Java_, lo cual no es cierto, ambos lenguajes tiene sus pros y contras. Decidir cual es mejor es cuestión de gustos del programador y de lo que se quiere realizar.  Por ejemplo, en cuanto a potencia se refiere, _Java_ se prefiere  a usar  _Python_ , ya que la potencia de su máquina virtual hace que en este aspecto sea preferida por las empresas. 

3. **¿Cuántos tipos de datos existen en el lenguaje _Python_?**

Python ofrece una gran variedad de tipos de datos. Los principales,  se pueden clasificar como sigue:

| Tipo de Datos|  _Python_ |
|--|--|
|Tipo cadena | `str` |
|Tipos numéricos|`int`,  `float`,  `complex`|
|Tipos de secuencias| `list`,  `tuple`,  `range`|
|Tipo de diccionario| `dict`|
|Tipos de conjuntos| `set`,  `frozenset`|
|Tipo booleano| `bool`|
|Tipos de datos binarios |`bytes`,  `bytearray`,  `memoryview`|
|None|`None`|

4. **¿Cuál es la diferencia entre "tupla" y “lista"?**

Las **tuplas** no son mutables y las **listas** sí lo son, esto quiere decir, que una vez creada una tupla  no se pueden cambiar sus valores. Esto provoca que las tuplas ocupen menos memoria que las listas. 

5. **¿Qué es PEP8?**

**PEP8** (Python Enhancement Proposals) es el manual de estilo que aborda los temas de cómo nombrar clases, funciones, variables, etc en _Python_. 

6. **¿Qué es "pickling" y "unpickling"?**

**Pickling**: es un proceso en el que un objeto  se convierte en un flujo de bytes.  

Ejemplo:
~~~
import pickle
def pickle_data():  
    data = {  
                'name': 'Eduardo',  
                'profession': 'Something',  
                'country': 'Mexico'  
        }  
    filename = 'PersonalInfo'  
    outfile = open(filename, 'wb')  
    pickle.dump(data,outfile)  
    outfile.close()
pickle_data()
~~~
El argumento de la función open `'wb'` se refiere a la escritura en modo binario. Al ejecutar la función `pickle_data()`se crea el archivo  `PersonalInfo`.

**Unpickling**: Es el proceso inverso de **Pickling**, donde un flujo de bytes se convierte en un objeto.

Por ejemplo:
~~~
import pickle
def unpickling_data():  
    file = open('PersonalInfo','rb')  
    new_data = pickle.load(file)  
    file.close()  
    return new_data  
~~~
Al ejecutar `print(unpickling_data())` se obtiene:
~~~
{
	'name': 'Eduardo', 
	'profession': 'Something',  
	'country': 'Mexico'  
}
~~~

7. **¿Qué es "lambda"?**

En  _Python_,  una función **lambda** se refiere a una  pequeña función anónima, esto es,  carece de nombre y está definida por una única  expresión.

Su sintaxis es la siguiente:
~~~
lambda _arguments_ : _expression_
~~~
Por ejemplo:
~~~
>>> suma_dos = lambda x,y : x + y
>>> suma_dos(1,2)
3
~~~
8. **¿Cómo se administra la memoria dentro del lenguaje Python?**

El administrador de memoria de _Python_ administra fragmentos de memoria llamados "Blocks". Una colección de "blocks" del mismo tamaño forma el “Pool”. Si los objetos se destruyen, el administrador de memoria llena este espacio con un nuevo objeto del mismo tamaño.

 - Los métodos y las variables se crean en la _Stack Memory_. 
   
  - Los objetos y las variables de instancia se crean en la _Heap
   Memory_.
   
![Python Memory Management. Have you ever wonder why memory… | by Seema Thapa  | DataDrivenInvestor](https://miro.medium.com/max/804/1*xnHGBRJ1eIG83sJVrJ81Hw.png)

Los objetos de Python tienen tres cosas: _tipo_, _valor_ y _recuento de referencias_.

La recolección de basura se implementa en Python de dos formas: _recuento de referencias_ y _generacional_. 

Cuando el recuento de referencias de un objeto llega a 0, el algoritmo de recolección de basura del recuento de referencias limpia el objeto inmediatamente. 

Si tiene un ciclo, el recuento de referencias no llega a cero, espera a que se ejecute el algoritmo de recolección de basura generacional y limpie el objeto. 

1. **¿Qué es "pass"?**

`pass` como su nombre lo indica es una operación nula, o sea que no pasa nada cuando se ejecuta. 

Se utiliza cuando se requiere por sintaxis una declaración pero no se quiere ejecutar ningún comando o código. También se utiliza en lugares donde  el código irá finalmente, pero no ha sido escrita todavía.

Por ejemplo:
~~~
for letra in "Python":
    if letra == "h":
        pass
    print("Letra actual :" + letra)
~~~
Se recorre la cadena `"Python"`, caracter por caracter,  pero al pasar por el caracter `'h'` no se hace nada en el condicional `if`.
~~~
Letra actual :P
Letra actual :y
Letra actual :t
Letra actual :h
Letra actual :o
Letra actual :n
~~~

10. **¿Puedes copiar un objeto en el lenguaje Python?**

Sí, hay varios mecanismos para copiar un objeto. Por ejemplo podemos utilizar el modulo `copy`.
~~~
>>> from  copy  import  copy  
>>> lista1  =  [1,2,3]  
>>> lista2  =  copy(lista1)
>>> id(lista1)
140000857767744
>>> id(lista2)
140000857767552
>>> lista = lista1
>>> id(lista)
140000857767744
~~~

La función `id()` recibe como argumento un objeto y retorna otro objeto que sirve como identificador único para el primero.

11.  **¿Cómo borrar un archivo dentro de Python?**

Para eliminar un archivo se emplea el modulo `os` y la función `remove()`.
~~~
from os import remove  
remove("archivo.txt")
~~~
12. **¿Qué es un "diccionario"?**

Un **diccionario** es una estructura de datos y un tipo de dato en Python, que permite guardar un conjunto no ordenado de pares **clave**-**valor**, donde no pueden existir dos elementos con una misma clave. Por ejemplo:
~~~
articulos = dict() 
articulos = { 
	'Mesa' : 300, 
	'Reloj' : 1200, 
	'Televisión': 8000 
	}
~~~
13. **¿Es Python un lenguaje de programación interpretado?**

Sí

14. **¿Cuál de ellos es un error?**

Sin respuesta.

15. **¿Cómo Python se considera un lenguaje orientado a objetos?**

Los seres humanos pensamos en términos de substantivos (objetos) y verbos (acciones de los objetos). _Python_ es un lenguaje orientado a objetos ya que en ella se encuentran los conceptos de la Programación Orientada a Objetos, como son:

 - Clases. 
 - Objetos. 
 - Abstracción. 
 - Encapsulamiento. 
 - Herencia. (_Python_ permite la herencia multiple)
 - Polimorfismo. 
 - Asociaciones entre objetos.

 16.  **¿Qué es “slicing"?**

En _Python_, el “slicing"  de listas es una práctica común. Considere una lista de Python. Se  desea acceder a un rango de elementos en esta lista. Una forma de hacer esto es usar el operador de corte simple, es decir, dos puntos `:`

Con este operador, se puede especificar dónde comenzar el corte, dónde terminar y especificar el paso. La división de listas devuelve una nueva lista de la lista existente. La sintaxis es la siguiente:

~~~
List[ inicio : fin : paso]
~~~
Por ejemplo:
~~~
>>> lista = [2,5,8,1,-1,5,11,14]
>>> lista[1:6:2]
[5, 1, 5]
~~~
 
 17. **Según la guía de estilos PEP8 ¿como deben escribirse las constantes?**

Las **constantes**  deben estar escritas con todas las letras en mayúscula y con guiones bajos separando palabras.  Por ejemplo,  `NUMERO_PI = 3.1416`

18. **¿Qué es virtualenv y como lo inicias con un interpretador de Python especifico?**

**virtualenv** es una herramienta utilizada para crear un entorno Python aislado. Este entorno tiene sus propios directorios de instalación que no comparten bibliotecas con otros entornos virtualenv o las bibliotecas instaladas globalmente en el servidor.

Una vez instalado **virtualenv**, para crear un entorno virtual con  Python3, simplemente ejecutamos el comando  `virtualenv`  de la siguiente manera:
```
$ virtualenv env --python=python3
```
Este crea un directorio llamado `env`, para activar este entorno virtual, se ejecuta el script  `activate`  instalado en el directorio  `bin/`:
```
$ cd env
$ source bin/activate
(env)$
```

[Examen Práctico](examen-practico.ipynb)

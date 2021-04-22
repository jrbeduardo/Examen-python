# Preguntas teóricas

1. **¿Qué es Python?**

**Python** es un lenguaje de programación interpretado, multiplafatorma y débilmente tipado.

2. **¿Por qué Python es mejor que Java?**

La pregunta esta mal formulada, ya que se asume que _Python_ es mejor _Java_, lo cual no es cierto, ambos lenguajes tiene sus pros y contras. Decidir cual es mejor es cuestion de gustos del programador y de lo que se quiere realizar.  Por ejemplo, en cuanto a potencia se refiere, _Java_ se prefiere  a usar  _Python_ , ya que la potencia de su máquina virtual hace que en este aspecto sea preferida por las empresas. 

3. **¿Cuántos tipos de datos existen en el lenguaje Python?**

Python ofrece una gran variedad de tipos de datos. Los principales,  se pueden clasificar como sigue:

| Tipo de Datos|  python |
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

Las **tuplas** no son mutables, es decir, una vez creada  no se pueden cambiar sus valores. Esto provoca que las tuplas ocupen menos memoria que las listas. 

5. **¿Qué es PEP8?**

**PEP8** (Python Enhancement Proposals) es el manual de estilo que aborda los temas de cómo nombrar clases, funciones, variables, etc en Python. 

6. **¿Qué es "pickling" y "unpickling"?**

**Pickling**: es un proceso en el que un objeto  se convierte en un flujo de bytes.  

Ejemplo:
~~~
import pickle
def pickle_data():  
    data = {  
                'name': 'Prashant',  
                'profession': 'Software Engineer',  
                'country': 'India'  
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
{'name': 'Prashant', 'profession': 'Software Engineer', 'country': 'India'}
~~~

7. **¿Qué es "lambda"?**

En  Python,  una función **lambda** se refiere a una  pequeña función anónima, esto es,  carece de nombre y está definida por una única  expresión.

Su sintaxis es la siguiente:
~~~
lambda _arguments_ : _expression_
~~~
Por ejemplo:
~~~
suma_dos = lambda x,y : x + y
~~~
9. **¿Cómo se administra la memoria dentro del lenguaje Python?**

El administrador de memoria de Python administra fragmentos de memoria llamados "Blocks". Una colección de "blocks" del mismo tamaño forma el “Pool”. Si los objetos se destruyen, el administrador de memoria llena este espacio con un nuevo objeto del mismo tamaño.

 - Los métodos y las variables se crean en la _Stack memory_. 
   
  - Los objetos y las variables de instancia se crean en la _Heap
   memory_.

![12 Difference Between Stack And Heap In C++ (With Table) - Viva Differences](https://vivadifferences.com/wp-content/uploads/2019/09/Stack-And-Heap-1.png)
Los objetos de Python tienen tres cosas: _tipo_, _valor_ y _recuento de referencias_.

La recolección de basura se implementa en Python de dos formas: _recuento de referencias_ y _generacional_. 

Cuando el recuento de referencias de un objeto llega a 0, el algoritmo de recolección de basura del recuento de referencias limpia el objeto inmediatamente. 

Si tiene un ciclo, el recuento de referencias no llega a cero, espera a que se ejecute el algoritmo de recolección de basura generacional y limpie el objeto. 

10. **¿Qué es "pass"?**

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
13. **¿Qué es un "diccionario"?**

Un **diccionario** es una estructura de datos y un tipo de dato en Python, que permite guardar un conjunto no ordenado de pares **clave**-**valor**, donde no pueden existir dos elementos con una misma clave. Por ejemplo:
~~~
articulos = dict() 
articulos = { 
	'Mesa' : 300, 
	'Reloj' : 1200, 
	'Televisión': 8000 
	}
~~~
14. **¿Es Python un lenguaje de programación interpretado?**

Sí

15. **¿Cuál de ellos es un error?**

16. **¿Cómo Python se considera un lenguaje orientado a objetos?**


17. **¿Qué es “slicing"?**

18. **Según la guía de estilos PEP8 ¿como deben escribirse las constantes?**

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

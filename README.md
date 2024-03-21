# ¿Qué son los interfaces comparable y comparator? 

## Aplicando lo visto durante el trimestre.

## Introducción

Muchas operaciones entre objetos nos obligan a compararlos: buscar, y también ordenar. 

Podríamos haberle dedicado una unidad didáctica entera a los métodos de ordenaciones pero a estas alturas del curso, podemos aparcar a los tipos primitivos y hacer uso de algunas clases ya implementan su orden (natural, lexicográfico), para nuestras clases tenemos que especificar el orden con el que las vamos a tratar.

---

## Comparable

Comparable es una **interfaz** propuesta por la API de Java, y su definición es sencilla:

        public interface Compararable<T> {
            public int compareTo(T o);
        }

---

Recibe un objeto del mismo tipo que la clase que lo implementa. El valor de retorno del método compareTo será:

0 si ambos objetos son iguales,
un valor negativo si el objeto es menor,
y uno positivo si es mayor.
Nos sirve para indicar el orden principal de una clase.

---

## Comparator

Comparator también es un interfaz propuesto por Java, y su definición también es sencilla:

        public interface Comparator<T> {
            public int compare(T o1, T o2);
        }

---

Recibe dos argumentos, y su valor de retorno es análogo al de comparable.

Comparator nos servirá para indicar un orden diferente al orden natural definido con Comparable (no es necesario haber definido un orden con Comparable para poder utilizar Comparator, aunque sí es recomendable).

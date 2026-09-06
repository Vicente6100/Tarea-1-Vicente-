# Tarea-1-Vicente-
Tarea 1 Vicente 
Sistema de gestión de lista de espera para restaurante


Descripción
Este sistema permite a los usuarios gestionar la atención de clientes en un restaurante. Los usuarios pueden registrar nuevos clientes, asignar prioridades, ver la lista de espera, y más. Esta herramienta está diseñada para mejorar la eficiencia en la atención de un restaurante, asegurando que aquellos con mayor prioridad y antelación sean atendidos primero.


Cómo compilar y ejecutar

Este sistema ha sido desarrollado en lenguaje C y puede ejecutarse fácilmente utilizando Visual Studio Code junto con una extensión para C/C++, como C/C++ Extension Pack de Microsoft.
Para comenzar a trabajar con el sistema en tu equipo local, sigue estos pasos:

Pasos para compilar y ejecutar:
1. Descarga el archivo `.zip` en una carpeta de tu elección.
2. Abre el proyecto en Replit 
    - Entrar a https://replit.com/~.
    - Iniciar Sesión
    - Selecciona `+ > Import an existing proyect > Zip file` y elige la carpeta donde se encuentra el proyecto.
    - Carga el archivo y selecciona `View app ´
3. Compila el código
    - Abre el archivo principal (`tarea1.c`).
    - Selecciona `+ > Shell ´ para abrir la terminal  integrada
    - En la terminal, compila el programa con el siguiente comando (ajusta el nombre si el archivo principal tiene otro nombre):

			gcc tdas/*.c tarea1.c -Wno-unused-result -o tarea1

    - Luego ejecuta la aplicación con:

			./tarea1

Funcionalidades :


Funcionando correctamente:
Registrar grupos de clientes con sus datos básicos y una prioridad inicial.
Asignar o modificar la prioridad de los clientes.
Ver la lista de espera de los clientes, ordenada por prioridad y hora de registro.
Atender al siguiente grupo, respetando el orden de prioridad (o por Hora si la prioridad es la misma).
Buscar clientes en la lista de espera.

Problemas conocidos:
No valida si en la hora se ingresa un valor no numérico
No toma en cuenta nombres / ID duplicados
Solo toma en cuenta los nombres escritos exactamente a como se registraron

A mejorar :

Eficiencia al momento de registrar los datos 


Ejemplo de uso

Paso 1: Registrar un Nuevo Grupo

Se comienza registrando un nuevo grupo que acaba de llegar al Restaurante.

```
Opción seleccionada: 1) Registrar cliente
Ingrese el ID/Nombre del cliente: José Rojas
Ingrese la cantidad de personas: 11
Ingrese Hora de llegada (FORMATO XXXX) : 1700
```

El sistema registra a José Rojas con una prioridad inicial "Estándar" y guarda la hora actual de registro. La prioridad inicial puede ser ajustada más tarde.

Paso 2: Asignar Prioridad a un Cliente

Tras una observación detallada se le reasigna la prioridad al grupo .

```
Opción seleccionada: 2) Asignar prioridad a cliente
Ingrese el nombre del cliente: José Rojas
Seleccione el nuevo nivel de prioridad (1 para VIP, 2 para Grupo Grande, 3 para Estándar): 2
```

El sistema actualiza la prioridad de José Rojas a "Grupo Grande", asegurando que su grupo será uno de los próximos atendidos.

Paso 3: Ver la Lista de Espera

El usuario revisa la lista de espera para ver todos los clientes, sus prioridades y la Hora de llegada.

```
Opción seleccionada: 3) Mostrar lista de espera
```

La lista muestra a José Rojas en la parte superior, indicando su prioridad alta y que su grupo es el siguiente en línea para recibir atención.

Paso 4: Asignar una mesa al siguiente grupo

Basándose en su prioridad (o en su defecto, la hora de llegada) el grupo de José Rojas es atendido y se elimina de la lista de espera.

```
Opción seleccionada: 4)Asignar mesa al siguiente grupo
```
Otras opciones son :
5) Buscar reserva por ID/Nombre
Se ingresa el ID/Nombre buscado y se muestra el ID/Nombre, la cantidad de personas, la prioridad y la Hora de llegada

6) Salir
Termina la ejecución del programa



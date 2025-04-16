# ACT3_ED_SFF

1. Análisis del problema y requisitos: Identifica los actores y funcionalidades principales del sistema.
Objetivo del sistema:
Desarrollar un sistema que permita gestionar torneos deportivos con funcionalidades clave como crear torneos, inscribir equipos, generar emparejamientos, registrar resultados y mostrar clasificaciones.
Actores identificados:
- Administrador: Interactúa con funciones de gestión completas. Es decir, el responsable de añadir equipos y jugadores.
- Usuario: Consulta información de equipos y clubes. Simplemente visualiza.

Requisitos funcionales:
- Crear jugadores.  (include: Comprobar la no existencia de jugador)
- Crear equipos. (include: Comprobar la no existencia de equipo)
- Crear torneos. (include: Comprobar la no existencia de torneo)
- Consultar torneos. (include: Comprobar existencia de torneo)
- Inscribir equipos en torneos existentes. (include: Comprobar existencia de torneo y del equipo y si el equipo está inscrito)
- Comprobar si un equipo ya está inscrito. (include: Comprobar existencia de torneo y del equipo)
- Generar emparejamientos entre equipos disponibles. (include: Comprobar si equipo existe y está libre)
- Registrar resultados de partidas. (include: Comprobar existencia de torneo)
- Calcular la clasificación del torneo. (include: Comprobar existencia de torneo)
- Mostrar información detallada de jugador. (extend: Mostrar información equipo)
   
2. Elaboración del diagrama de casos de uso: Dibuja el diagrama UML mostrando actores y relaciones (<<include>>, <<extend>>).
![image](https://github.com/user-attachments/assets/85c536e8-8bce-4da6-afa9-dc6c1d1e0a1c)



   
3. Identificación de clases y relaciones: Define las clases principales y su categoría (Entidad, Control, Interfaz). Establece atributos, métodos y asociaciones entre clases.
Clases de entidad: existen cuatro, jugador, que es la entidad más pequeña y, que uniendo varios crean equipos. Al igual que partidas, que forman parte de un torneo. 
- Jugador: nombre, posición, dorsal
- Equipo: nombre, jugadores, club | Métodos: agregarJugador(), obtenerEstadísticas()
- Partida: equipo1, equipo2, golesEq1, golesEq2 | Métodos: obtenerResultado()
- Torneo: nombre, equipos[], partidas[] | Métodos: agregarEquipo(), obtenerClasificación()

Clase de control: métodos con la lógica necesaria para que funcione la aplicación, relacionando las entidades anteriores. 
- ControlTorneo: Métodos para lógica de negocio como crearTorneo(), inscribirEquipo(), registrarResultado(), generarEmparejamientos()

Clases de interfaz: las pantallas que se necesitan para la gestión visual de la aplicación.
- IU_Torneo: Pantalla de gestión de torneos
- IU_Equipo: Vista de detalle de equipos
- IU_Clasificación: Muestra rankings
  
4. Creación del diagrama de clases UML: Representa la estructura del sistema con clases, atributos, métodos y relaciones.
El diagrama representa la estructura del sistema:
- Asociación entre Torneo y Equipo (1 a muchos)
- Asociación entre Torneo y Partida (1 a muchos)
- Asociación entre Equipo y Jugador (1 a muchos)

- Clase ControlTorneo centraliza la lógica de negocio

![image](https://github.com/user-attachments/assets/be3d09a9-5245-49db-b440-15bbece9a589)









  

  

# Prueba - Desarrollo de interfaces interactivas con vue.
![App pokemon](src/assets/app.png)

Este proyecto es una aplicación de Vue.js que permite a los usuarios adivinar los nombres de diferentes Pokemon. Utiliza la API para obtener datos sobre varios Pokemon y muestra tarjetas coloreadas de estos en una cuadrícula.

### Estructura del proyecto:   
* App.vue: Componente principal de la aplicación.  
* PokeCard.vue: Componente hijo utilizado para mostrar cada tarjeta de Pokémon.

### Funcionalidades:  
* Mostrar una lista de Pokémon obtenidos aleatoriamente de la API de Pokémon.  
* Permitir a los usuarios adivinar el nombre de cada Pokémon.  
* Marcar un Pokémon como adivinado correctamente si el usuario ingresa el nombre correcto.  
* Contar y mostrar el número total de Pokémon adivinados correctamente.  


### Requerimientos: 

1. Usar las directivas para enlazar variables del estado con el template.
2. Importar y ocupar componentes hijos que reciban datos a través de props.
3. Renderizar dinámicamente componentes hijos usando el v-for. 
4. Usar los eventos para agregar interacciones en la aplicación y enlazarlos con métodos
locales.
5. Comunicar componentes hijos con su padre para la ejecución de un método. 
6. Usar la renderización condicional de elementos para mostrar u ocultar contenido.
7. Asignar condicionalmente estilos o clases por medio del style y class binding.
8. Utilizar Axios para el consumo de la API.
9. Hacer uso del ciclo de vida para ejecutar código al cargar la aplicación. 
10. Utilizar computed properties para el procesamiento de datos del estado. 
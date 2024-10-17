# OBJETOS Y ARREGLOS

LABORATORIO 04: INTRODUCCIÓN A JAVASCRIPT

## 🚀 Desarrallo 

Pagina web de referencia: MULTICINES (https://www.multicines.com.ec/)

### Ejercicios

//1. ARRAYS

![peliculas_multicines](https://github.com/user-attachments/assets/73bb8ab9-6b34-4806-889e-f9639939723b)
    
    const peliculas = ["VENOM 3", "SONRIE 2", "UN PANDA EN AFRICA", "MISFIT", "HORIZONTE", "EL CANDIDATO HONESTO", 
                    "EL GRAN AVISO", "JOKER 2", "ROBOT SALVAJE", "BEETLEJUICE", "LA SUSTANCIA"];

    const clientes = [
        {
            nombre: "Jonathan",
            reserva: 2,
            lugar: "Multicines Scala",
            pelicula: "VENOM 3"
        },
        {
            nombre: "James",
            reserva: 3,
            lugar: "Multicines Paseo San Francisco",
            pelicula: "JOKER 2"
        }
    ]

    //forEach : se recorre el arrya de pelicukas
    peliculas.forEach((pelicula, indice) => {
        console.log(`${indice + 1} - ${pelicula}`);
    })


//2. MAP 

BOLETOS VIP

![servicio_vip_multicines](https://github.com/user-attachments/assets/09c5c9be-33c8-4dcb-b741-de5bdc76a821)

SERVICIO DE COMIDA

![servicio_comida_multicines](https://github.com/user-attachments/assets/055949ef-680e-467d-b4eb-5a4941084c57)
  
    const servicios = [
        {
            nombre: "Boletos VIP",
            precio: 7.10,
            imagen: "img/servicio2.png",
        },
        {
            nombre: "Combo 1",
            precio: 9.75,
            imagen: "img/servicio2.png",
            detalles: ["Canguil Mediano", "Bebida","Hot dog"]
        }
    ]

    const nuevosServicios = servicios.map(s => (
        {
            nombre: s.nombre,
            precio: s.precio
        }
    ))

    console.log(nuevosServicios)

//3. Desestructuracion

    //Forma 1
    const [pelicula1, pelicula2, pelicula3, pelicula4] = peliculas;
    console.log(pelicula1); 
    //Forma 2
    const [,,,,,pelicula9] = peliculas;
    console.log(pelicula9);


//4. Condicional Ternario

    const categoriasPeliculas = ["Aventura", "Comedia", "Terror", "Ciencia Ficción", "Animación"];

    categoriasPeliculas.length <= 5 ? console.log("Registrar nueva categoría") : console.log("No se puede registrar más categorías");


![categoria_multicines](https://github.com/user-attachments/assets/c6be5523-f532-416a-9340-f0ae4709c5d7)


//5. Métodos

    //push: agrega un nuevo elemento al final de un arreglo
    categoriasPeliculas.push("Acción") 
    //unshift : agrega al inicio del arreglo
    categoriasPeliculas.unshift("Romance") 
    //pop: elimina el ultimo elemento del arreglo  -- funciona en conjunto con el shift()
    categoriasPeliculas.pop()
    //shift(): elimina el primer elemento del arreglo
    categoriasPeliculas.shift()

    console.log(categoriasPeliculas)

//6. Find

    let categoriaEncontrada = categoriasPeliculas.find((c) => {return c === "Terror"});

    categoriaEncontrada ? console.log("Mostrar subcategorías") : console.log("Categoría no encontrada");

//7. Filter

    let categoriasFilter = categoriasPeliculas.filter((c) => (c.startsWith('C')));
    console.log(categoriasFilter)

//8. REST

    const [movie1,movie2,movie3,movie4,movie5,...movies] = peliculas
    console.log(movies)

//9. SPREAD: Une los arreglos en uno solo


    let allServices = []

    allServices = [...peliculas,...categoriasPeliculas]
    console.log(allServices)

## Author

👤 **Author**

- GitHub: [@JonathanRamirez23](https://github.com/JonathanRamirez23)

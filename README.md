Esta función puede pasar de muchas lineas a 4

```js
/** 
         * la funcion jugar recibe un parametro, siempre que nos refiramos a la palabra "usuario" me esta redirigiendo al texto piedra/papel/tijera.
         * jugadorAI también vale (piedra, papel o tijera)
         * cada vez que lea un "usuario" es como decir: piedra, papel o tijera
         * */
        function jugar(usuario) {
            const jugadorAI = elegirJugadorAI(); // devuelve piedra, papel o tijera

            let resultado = "";

            if (jugadorAI == usuario) { resultado = 'Empate';} 
            else if (usuario == 'piedra') { // cuando yo tiro piedra, la ia tiene 2 opciones, o tirar papel y yo pierdo, o tirar tijeras y yo gano.

                // if (jugadorAI == 'papel') {
                //     console.log('Perdiste');
                //     resultado = 'Perdiste';
                // } else {
                //     console.log('Ganaste');
                //     resultado = 'Ganaste';
                // }

                // hemos convertido el if en una operación ternaria
                // resultado = () ? "verdadero": "falso";
                resultado = (jugadorAI=='papel') ? "Perdiste": "Ganaste";
            } else if (usuario == 'papel') {
                resultado = (jugadorAI=='tijera') ? "Perdiste": "Ganaste";
            } else if (usuario == 'tijera') {
                resultado = (jugadorAI=='piedra') ? "Perdiste": "Ganaste";
            }

            console.log(resultado);
```
# sesión 06 - 19/05

# Clase introductoria y Pre-Examen

## Sonido en p5.js 
loadSound()

*  Primer paso es suber sonidos al menu desplegable de p5.js
*  Recordar subirlo a carpetas para mantener todo ordenado
*  usar todo en minuscula y sin espacios

let sonido; 

function preload(){
sonido=loadSound('nombreCancion.mp3')
}

function setup(){
createCanvs(400,400);
frameRate(20);
sonido.play
}

Métodos de control de sonido 
nombreVar.play(sonido una vez)
".loop()
"
"
"

Metodos de Estado o de consulta 
nombreVariable.isPlaying (devuelve a true si el sonido esta sonando en ese momento y false si no.)
.isPaused() Devuelve true si el sonido fue congelado con pause()
.isLooping() Devuelve true si el sonido esta configurado para repetirse en loop()
.currentTime 

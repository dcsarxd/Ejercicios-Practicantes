<h1 align="center">Uso de la Terminal con Cowsay</h1>

<p align="center"> Este contenido es mas centrado a que comprendan el uso de la terminal, el concepto basico de que si ustedes escriben algo en la terminal, esto conlleva a una reaccion del equipo devolviendo una respuesta relacionada o directa a lo que ustedes solicitaron. 
    <br> 
</p>

# 📋 Contenido

- [Actualizacion de Instalación de Cowsay](#install)
- [¿Que es Cowsay?](#cowsay)
- [Utilizando Cowsay](#doing_shieeeet)
- [Usando Cowsay con Fortune](#fortune)
- [Usando Cowsay con Fortune y Lolcat](#lolcat)
- [Prueba Final](#final_test)
- [Instalación de RVM](#rvm_install)
- [Limpieza de Imagen](#clean_img)

## 🛠️: Actualizacion de Instalación de Cowsay <a name = "install"></a>
Como les comentaba, "APT" es el manejador de paquetes en el sistema operativo ubuntu, asi mismo apt lo es en otros sistemas operativos parecidos.

*Siempre como buena practica, acostumbren actualizar sus equipos antes de realizar una instalación de algun paquete. No es obligatorio, pero si que es una buena practica.* 😁

   ```   
   sudo apt update
   ```
*Una vez actualizados los repositorios de apt, procedemos con la instalación.*
   ```   
   sudo apt install cowsay
   ```
## 🤨: ¿Que es Cowsay? <a name = "cowsay"></a>
Cowsay es...

<p align="center">
  <a href="" rel="noopener">
 <img width=800px height=200px src="https://itsfoss.com/content/images/2023/06/normal-cowsay.svg" alt="cowsay_holis"></a>
</p>

*Asi es, es una vaquita que habla.*

Lo bueno de cowsay es que se puede usar para "trabajo serio" si se combina con otros comandos. Un ejemplo de ello es su uso para mostrar el "mensaje del día" en un servidor Linux compartido con varios usuarios.

## 🛸 : Utilizando Cowsay <a name = "doing_shieeeet"></a>
Como se los comentaba y como lo sugiere el nombre, se trata de una vaca parlante en ASCII que genera el texto que se le proporciona como entrada. De manera predeterminada, cowsay ofrece varias opciones para modifical el aspecto y la apariencia de la vaca ASCII. 
   ```
cowsay "Hola!!"
   ```
*El comando anterior les imprimirá una vaquita parecida a la de la imagen anterior.*

### 🪄 Utiliza Caracteres Especiales como Ojos
Puedes usar la opción *"-e"* y luego indicar los dos caracteres que quieres que aparezcan como ojos. 

   ```
cowsay -e hh "Hola!!"
   ```
<p align="center">
  <a href="" rel="noopener">
 <img width=800px height=200px src="https://itsfoss.com/content/images/2023/06/cowsay-special-eyes.svg" alt="cowsay_holis2"></a>
</p>

O tambien pueden hacer una Vaca Codiciosa 🤑.
   ```
cowsay -g "Hola!!"
   ```
<p align="center">
  <a href="" rel="noopener">
 <img width=800px height=200px src="https://itsfoss.com/content/images/2023/06/greedy-cowsay.svg" alt="cowsay_holis3"></a>
</p>

### 🐣 Utilizaremos otro personaje en lugar de la vaca
Cowsay tambien proporciona muchas otras imagenes ASCII, que pueden tulizar a traves de la opcion *"-f"*. 

Y para listar las opciones que tenemos podriamos hacerlo con: 
   ```
cowsay -l
   ```
Al ejecutar el comando anterior les devolverá algo similar a esto: 
   ```
Cow files in /usr/share/cowsay/cows:
apt bud-frogs bunny calvin cheese cock cower daemon default dragon
dragon-and-cow duck elephant elephant-in-snake eyes flaming-sheep fox
ghostbusters gnu hellokitty kangaroo kiss koala kosh luke-koala
mech-and-cow milk moofasa moose pony pony-smaller ren sheep skeleton
snowman stegosaurus stimpy suse three-eyes turkey turtle tux unipony
unipony-smaller vader vader-koala www
   ```
¿No se ve muy bonito asi verdad? ¡Que tal si lo ordenamos!

   ```
 Comando: cowsay -l | tail -n +2 | tr ' ' '\n' | sort

apt
bud-frogs
bunny
calvin
cheese
cock
cower
daemon
default
dragon
dragon-and-cow
duck
elephant
elephant-in-snake
eyes
flaming-sheep
fox
ghostbusters
gnu
hellokitty
kangaroo
kiss
koala
kosh
luke-koala
mech-and-cow
milk
moofasa
moose
pony
pony-smaller
ren
sheep
skeleton
snowman
stegosaurus
stimpy
suse
three-eyes
turkey
turtle
tux
unipony
unipony-smaller
vader
vader-koala
www
   ```

Ahora si ¿no? asi ordenadito ya se ve mejor. Con esto ya podemos usar cualquier animalito que nos guste o llame la atencion, en mi caso un DRAGON.

   ```
cowsay -f dragon "HOLAAAAAAAAAAAA"
   ```

<p align="center">
  <a href="" rel="noopener">
 <img width=800px height=400px src="https://itsfoss.com/content/images/2023/06/cowsay-different-inbuilt-files.svg" alt="cowsay_holis4"></a>
</p>

Asi mismo podemos utilizar otras opciones.
<table>
<thead>
<tr>
<th><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Opción</font></font></th>
<th><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Usar</font></font></th>
</tr>
</thead>
<tbody>
<tr>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">-b</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Invoca el modo Borg</font></font></td>
</tr>
<tr>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">-d</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Hace que la vaca parezca muerta.</font></font></td>
</tr>
<tr>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">-pag</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Provoca un estado de paranoia en la vaca.</font></font></td>
</tr>
<tr>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">-s</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Hace que la vaca parezca completamente drogada</font></font></td>
</tr>
<tr>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">-t</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Una vaca cansada</font></font></td>
</tr>
<tr>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">-y</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Da a la vaca un aspecto juvenil.</font></font></td>
</tr>
</tbody>
</table>

## ✨ : Usando Cowsay con Fortune <a name = "fortune"></a>

Con la ayuda de lo que se conoce como "la redireccion de tuberias/respuestas (pipelines)" pueden utilizar cowsay junto con otros comandos populares y divertidos en linxu, como *"fortune"* o *"lolcat"*

   ```
sudo apt install fortune

sudo apt install lolcat

O, si les da problema la instalacion de lolcat, pueden intentar con lo siguiente: 

sudo snap install lolcat


**Cuando hagan estas instalaciones reinicien la termina, es decir, cierren y vuelvan a abrir una nueva. 
   ```

*"Fortune"* es un pequeño programa que imprime citas de personajes famosos en una terminal. Se puede ejecutar independiente, por ejemplo. 

   ```
fortune
   ```
Ahora, si quieres que lo diga la vaquita, utiliza: 
   ```
fortune | cowsay
   ```
Les invito a que lo prueben con otros animalitos y demás... 
 ```
fortune | cowsay -f tux   
   ```
## ✨ : Usando Cowsay con Fortune y Lolcat <a name = "lolcat"></a>

Ahora si quieren hacerlo mas interesante, pueden hacer uso de la herramienta lolcat, igualmente haciendo uso de los pipelines.
 ```
fortune | cowsay -f tux  | lolcat
   ```

<p align="center">
  <a href="" rel="noopener">
 <img width=800px height=400px src="https://itsfoss.com/content/images/2023/06/-cowsay-fortune-lolcat-tux.svg" alt="cowsay_holis4"></a>
</p>


## 🧐 : Prueba Final <a name = "final_test"></a>
Ahora que ya conocen todo el uso que se le puede hacer a una herramienta de terminal, dicha herramienta ya la han utilizado en conjunto con otras herramientas incluso.

Ya podriamos hacer algo productivo para lo aprendido.

#### Quiero que configuren un mensaje con cowsay, fortune y lolcat para que se muestre cada vez que ustedes creen una pestaña nueva.

¿Pero... Como hacemos eso? Tranquilas, aca mismo se los indico.

Primero, vamos a instalar el administrador de archivos llamdo "*vim*".

 ```
sudo apt install vim
   ```
Una vez que lo tengan instalado, vamos a crear un archivo con vim, esto lo hacemos con el siguiente comando: 

 ```
vim start-terminal.sh
   ```
El comando anterior les va a abrir una terminal en blanco, en donde ustedes ya podran escribir, pero para eso tienen que activar el modo "*interactivo*". Esto lo hacen unicamente presionando *la letra i*. 

Una vez lo hayan hecho, ya podrán escribir en el archivo, por lo cual van a pegar lo siguiente y configurandolo a sus gustos. 

 ```
#!/bin/bash 
fortune | cowsay -f hellokitty | lolcat
   ```
Una vez hayan escrito los comandos en el archivo, escriban ":wq" y luego presionan enter. Esto guardará su archivo las sacará de la terminal interactiva.

Pueden consultar su archivo con el siguiente comando: 
 ```
cat start-terminal.sh
   ```

Una vez hecho esto, quiero que comprendan de que lo que caban de hacer, es *"un archivo ejecutable en ubuntu"*, tengan mucho en cuenta eso. 

Pueden ejecutar dicho archivo de esta manera: 

 ```
./start-terminal.sh
   ```

#### ¡¡PERFECTO!! 🤯🤯

Ahora debemos de conocer en donde es que hemos creado nuestro archivo.
Para esto podemos ejecutar el siguiente comando:
 ```
pwd

**Este comando les va a devolver algo parecido a esto: /home/miusuario
   ```
Nuestro sript de bash o ejecutable de ubuntu funciona y sabemos en donde está, ahora debemos de indicar de que se ejecute cada vez que abramos una ventana nueva.
Para esto, existe un archivo especial y especifico para las configuraciones de BASH o la terminal como tal. Este es el famoso "*.bashrc*".

Por lo tanto, vamos a abrir dicho archivo con "*vim*"


 ```
vim .bashrc
** Quiero que tomen en cuenta de que el archivo .bashrc unicamente lo encontrarán en la raiz de sus usuarios. Si tienen dudas sobre esto, me preguntan. 
   ```

Cuando abran este archivo, verán muchas cosas que no van a comprender, no se preocupen, es normal. Lo que deben de hacer es ir bajar hasta la parte final del documento, pueden moverse con las flechas del teclado.

Una vez se encuentren en la ultima linea, presionen nuevamente la terminal interactiva con *"i"*

Y escriben lo siguiente:

 ```
source /home/miusuario/start-terminal.sh
   ```

Una vez escrito esto, pueden guardar y salir de la terminal igualmente con "*:wq*"

Ahora pueden validar su trabajo abriendo una nueva ventana de la terminal. 

### ¡¡Felicidades Chicas!! 🥳🥳


## LES AUTRES COMPOSANTS 

### 1- Le moteur 
![Légende de l'image](./images/moteur.png)

Un moteur est un dispositif qui transforme une forme d'energie en energie mecanique. 
#### Branchement : 
On ne le branche pas directement sur la carte Arduino, on passe par un driver (comme le l293D par exemple). 
#### Role :
Faire tourner des roues, ventilateurs, etc.


### 2- Une pile 
![Légende de l'image](./images/pile.png)

C'est une source d'energie electrique.
#### Branchement :
`+` -> circuit 

`-` -> GND

#### Role : 
Alimenter tout un circuit.

### 3- Buzzer piezoelectrique
![Légende de l'image](./images/buzzer.png)

Un buzzer est un composant qui fait du son. 
#### Branchement :
`+` -> pin Arduino

`-` -> GND
#### Role : 
Emettre un bip/son/alarme.

### 4- Une LED  
![Légende de l'image](./images/pile.png)

C'est un composant qui emet de la lumiere quand le courant passe
#### Branchement :
anode `+` -> circuit 

 cathode `-` -> GND via un resistance 

#### Role : 
indique quelque chose visuellement 


### 5- Une resistance  
![Légende de l'image](./images/pile.png)

Limite le passage du courant electrique 
#### Branchement :
il se met en serie avec un compaosant dont le courant est trop elevee (une led par exemple )

#### Role : 
Empeche de griller un composant 

---
### 6- Le L293D 
![Légende de l'image](./images/pile.png)

Le L293D est un driver moteur contenant 2 ponts en H 
Un pont en H permet de controler un moteur (soit tourner dans un sens ou dans l autre) 
Le L293D a deux ponts en H. Il peut donc controler deux moteurs.
#### Branchement :

🔹 Alimentation

Vcc1 (pin 16) → 5V (logique, Arduino)

Vcc2 (pin 8) → alimentation moteur (ex: 6V, 9V…)c est à cette broche qu'on augmente la puissance 

GND (pins 4,5,12,13) → masse commune

🔹 Moteur 1

OUT1 (pin 3) → borne 1 du moteur

OUT2 (pin 6) → borne 2 du moteur

🔹 Commande moteur

IN1 (pin 2) → contrôle sens

IN2 (pin 7) → contrôle sens

EN1 (pin 1) → activation (mettre à 1 ou PWM)

#### Role : 
Il permet d'alimenter un moteur d'alimenter un moteur avec plus de puissance que ce que peut fournir un microcontroleur( arduino par exemple)

#### Bilan des entrees : 
Arduino envoie des ordres en 0 ou 1 aux entrees et il execute . Pour un moteur on a deuc entrees indirect l'un dans chaque direction 

---

### 7- Un capteur de distance à ultraons (le HC-SR04) 
![Légende de l'image](./images/pile.png)

C'est un capteur de distance à ultrasons . Il envoie une onde sonore (ultrason) dans l'environnement . L'onde touche un objet et revient vers le capteur .Le capteur mesure ainsi le temps aller-retour . La formule utilisee est: $$d = \frac{v \times t}{2}$$
#### Branchement :
Le HC-SR04 a 4 pins :

VCC → alimentation (5V)

GND → masse

TRIG → envoyer le signal

ECHO → recevoir le signal

Exemple  =

vcc->5V     GND->GND    TRIG->9      ECHO->10 

#### Role : 
Mesurer la distance entre lui et un objet Il est bon à savoir que sa distance maximale est de 4m et la minimale  est de 2cm




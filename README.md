# m3-uf1-examen (2 part)
M3 UF1 Examen 2

En aquest examen haureu de respondre les següents preguntes, substituint allà on posi //TODO per la vostra resposta.

Només hi ha 1 pregunta, que servirà per a pujar nota un màxim de 3 punts.

Haureu d'utilitzar el jshell per a testejar tot el codi relacionat amb cada pregunta, i al final de l'exercici 
haureu d'incloure en aquest repositori els fitxers _history_ i _snippets_ (seguint el patró de noms establert a l'exercici 0) 
corresponents a aquest exercici, **directament al directori arrel del repositori**.

#### No es pot consultar cap material, excepte el referenciat en aquest enunciat.

### Criteris de qualificació:
* Si no s'incorporen els fitxers _history_ i _snippets_ amb els seus continguts que demostrin que l'alumne ha treballat en les respostes a cadascuna de les preguntes, la qualificació serà de 0.
* L'exercici val 3 punts.
* S'avaluarà la correctesa en la resposta, així com la seva **claredat** (que no presenti ambigüitats).
* **Per a obtenir la màxima nota de 3, és imprescindible que la solució sigui correcta, que funciona i, també, que el codi estigui comentat amb comentaris (que comencen amb //) explicant què fa el codi**
* El codi ha d'estar **ben formatat**. En cas contrari, no s'avaluarà la resposta (obtenint un 0).
* Tot i que l'enunciat està redactat en català, l'alumne pot respondre, a banda de en català, en anglès o en espanyol. Faltes d'ortografia en el redactat penalitzarà la nota.

### Preguntes

#### Pregunta 1 - Ordenació d'arrays

Escriu una funció, la signatura de la qual pot ser

```
int[] sortArrayEvenOdd(int[] a);
```

o també pot ser

```
void sortArrayEvenOdd(int[] a);
```

depenent de l'algorisme que escolliu per a resoldre aquest problema.


Què cal fer? Implementar aquesta funció, usant l'algorisme que es vulgui, per a ordenar **de major a menor** tots els números enters que hi hagi a l'array a que es passa com a paràmetre, però amb la següent peculiaritat: primer han d'estar ordenats els números parells, i a continuació, els números senars. 

Exemple:

si a = {4,3,-1,6,7,14,-11,3,8}

llavors el resultat a obtenir serà {14,8,6,4,7,3,3,-1,-11}

Escriu aquesta funció a continuació:


int [] sortArrayEvenOdd(int[]a){ \\inicialitza la funció

sort(a); \\cridem a la funció sort per a que ordeni l'array que li donem.

for(int i=0;i<a.length;i++){\\creem la variable index per a que passi per a cada valor.

if(a[i]%2 !=0){ \\aqui fem que el modul no sigui igual a 0 per a trobar els numeros impars.

int j=i;

while(a[j]%2 !=0 && j<a.length-1){\\aqui posem la condició per a fer el nou array i separar els pars dels impars.

j++;

}

if(j>=a.length-1){\\aqui posem que sigui menor per a posar el limit als numeros pars.

if(a[j]%2 !=0){

return a;\\retornem l'array que ja fara el bucle per separar els numeros pars i impars.

}

}

int temporal = a[i];

a[i]=a[j];

a[j]= temporal;

}\\fem una iteracio per que vagi posant els valors en el lloc que li correspon.

}

return a;\\aqui retornem l'array ja ordenat completament i separats en numeros pars i impars.

}

Pots consultar els apunts de Moodle que vulguis així com d'altres pràctiques d'aquesta UF1.

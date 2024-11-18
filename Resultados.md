# Resultados
### 1. Identificación de la lacasa de _M. profundimaris_
Con la secuencia de la proteína de _M. profundimaris_ se hallaron los siguientes dominios:
![image](https://github.com/user-attachments/assets/e44fdf94-f479-48ae-95be-aa8324fb3b24)

### 2. Alineamiento de la lacasa de _M. profundimaris_ y similares
A partir de el alineamiento, se encontraron estas distancias filogenéticas entre secuencias:
![image](https://github.com/user-attachments/assets/1e8fc9fe-959c-49d5-a304-0f9d42c66982)

### 3. Selección del organismo con una proteína similar
El modelado de _M. profundimaris_ fue (sitio catalítico encerrado en rojo):

![image](https://github.com/user-attachments/assets/ac5c7617-3fdf-46d2-93a3-67e151370347)

El modelado de _M. colpomeniae_ fue (sitio catalítico encerrado en rojo):

![image](https://github.com/user-attachments/assets/9c42eab9-9b69-4aea-a644-0830c0c1eb10)

El modelado de _M. xestospongiae_ fue (sitio catalítico encerrado en rojo):

![image](https://github.com/user-attachments/assets/ad4d7166-fc19-44d0-a096-675bb1d56f02)

El modelado de _O. bacterium_ fue (sitio catalítico encerrado en rojo):

![image](https://github.com/user-attachments/assets/838ea515-d4a2-48bd-ae75-713efa512103)

Se eligió la proteína _M. xestospongiae_ debido a su sitio catalítico tan conservado y similar al de _M. profundimaris_.

### 4. Obtención de la secuencia de ADN
Utilizando la secuencia de aminoácidos de _Marinobacter xestospongiae_, se encontró una coincidencia en la secuencia del genoma completo de _Marinobacter sp_.

![image](https://github.com/user-attachments/assets/5b367458-00f0-4393-b17c-e77f24cd86b2)

Específicamente, en las posiciones de inicio y parada (3589529, 3590887).Se utilizó la secuencia identificada en GeneBank con el ID: CP071785.1:3589529-3590887.

![image](https://github.com/user-attachments/assets/5a6ccaa9-36e8-4a8a-9762-55f7f0a04e6a)

### 5. Clonación
- Para el diseño manual de primers, fue necesario trabajar con una secuencia de nucleótidos más amplia que la seleccionada como secuencia de interés. Específicamente, se utilizó el ID: CP071785.1:3589519-3590887. Como se puede apreciar, el cambio consistió en considerar 10 nucleótidos aguas arriba de la secuencia, con el fin de tener más libertad al momento de diseñar los primers, los cuales fueron:

  Forward: ACCATCCGTTATGCCA, %GC = 50%, T<sub>m</sub> = 51.83 °C

  Reverse complement: ACTGACTTCGATGTAACC, %GC = 44%, T<sub>m</sub> = 51.22 °C

  ![image](https://github.com/user-attachments/assets/61fbbdfd-79f1-4598-bff7-2c26b6c5599b)

  
- Basándose en el trabajo realizado por Chang et al. (2022), en el que se clona una proteína lacasa en _E. coli_, se optó por el plásmido pET-22b, cuyo mapa de restricción está bien reportado y, además, codifica para la resistencia a la ampicilina
- Para el vector plasmídico, se obtuvo el siguiente mapa de restricción:
  
  ![image](https://github.com/user-attachments/assets/0c21cd60-daf1-4af8-895c-275f83f5f3a9)
  
  Para el inserto, se obtuvo el siguiente mapa de restricción:
  ![image](https://github.com/user-attachments/assets/7aa43027-88c7-4770-9d0c-93f713b888f4)

- Contrastando ambos mapas de restricción, se aprecia que el vector contiene las regiones de restricción de las enzimas _HindIII_ y _BamHI_, mientras que el inserto carece de estas secuencias, razón por la cual son seleccionadas para el proceso de digestión.
- Teniendo las enzimas seleccionadas, es necesario modificar los primers con las respectivas secuencias de restricción para que los amplicones generen extremos cohesivos al ser digeridos con las enzimas.

  _HindIII_ → AAGGTT

  _BamHI_ → GGATCC

  Se obtienen entonces los primers

  Forward: AAGCTTACCATCCGTTATGCCA, %GC = 45.4%, T<sub>m</sub> = 51.83 °C
  
  Reverse complement: GGATCCACTGACTTCGATGTAACC, %GC = 50%, T<sub>m</sub> = 51.22 °C

  El porcentaje GC se comprueba de forma manual, obteniendo un valor aceptable. Por otro lado, la T<sub>m</sub> permanece igual, al no involucrar las regiones de reconocimineto añadidas. 


### _Project 10: net_pratice - Tenth project for the formation of software engineers at school 42 São Paulo._

🏠 [home](https://github.com/Vinicius-Santoro/42-formation-lvl2-10.net_pratice)<br>
⬅ [level 08](https://github.com/Vinicius-Santoro/42-formation-lvl2-10.net_pratice/blob/main/readmes/level08.md) | [level 10](https://github.com/Vinicius-Santoro/42-formation-lvl2-10.net_pratice/blob/main/readmes/level10.md) ➡
<h1></h1>

### _This is `level 09`_

![level09_unsolved](https://user-images.githubusercontent.com/83036509/200429808-8d84ca01-743b-4bfe-b50e-1719984bb104.png)

<h1></h1>

### _Goal 1:  meson need to communicate with ion._
- O que podemos fazer inicialmente, é deixar todas as máscaras iguais da `interface R11`. 
- Utilizei o IP `200.100.10` para as `interfaces A1`, `B1` e `R11`.
- Configurei o `gateway` co cliente `A` e `B` com o IP da `interface R11`.
- Para sabermos o intervalo de cada subrede, precisamos calcular o salto, que é (256 - (octeto misto)). Ou seja, 256 - 128 = 128.
- Há duas redes possíveis para o IP `200.100.10.*`.

<div align="center">
    
| Rede     |      Host     | Broadcast |
|:----------:|:-------------:|:------:|
| 200.100.10.0 | 200.100.10.1 - 200.100.10.126| 200.100.10.127
| 200.100.10.128 | 200.100.10.129 - 200.100.10.254| 200.100.10.255
  
</div>

### _Goal 2:  cation need to communicate with gluon._
- O que podemos fazer inicialmente, é deixar a máscara da `interface D1` igual a da `interface R23`.
- O IP da `interface R23` é fixo, de acordo com o `gateway` de `client D`. Sendo ele: `75.85.129.177`.
- Para sabermos o intervalo de cada subrede, precisamos calcular o salto, que é (256 - (octeto misto)). Ou seja, 256 - 192 = 192.
- Há quatro redes possíveis para o IP `75.85.129.*/26`.

<div align="center">
    
| Rede       |      Host     |  Broadcast |
|:----------:|:-------------:|:----------:|
| 75.85.0.0| 75.85.0.1 - 75.85.63.254| 75.85.63.255
| 75.85.64.0| 75.85.64.1 - 75.85.127.254| 75.85.127.255
| 75.85.128.0| 75.85.128.1 - 75.85.191.254| 75.85.191.255
| 75.85.192.0| 75.85.192.1 - 75.85.255.254| 75.85.255.255
  
</div>

- Deixei o IP da `interface C1` e `interface R22` com a rede `11.0.0`.
- Para sabermos o intervalo de cada subrede, precisamos calcular o salto, que é (256 - (octeto misto)). Ou seja, 256 - 0 = 0.
- Há uma rede possível para o IP `11.0.0.*/24`.

<div align="center">
    
| Rede       |      Host     |  Broadcast |
|:----------:|:-------------:|:----------:|
| 	11.0.0.0| 11.0.0.1 - 11.0.0.254|	11.0.0.255
  
</div>

- Antes de continuar os objetivos, coloquei as `interfaces R13 e R2` no IP de rede `117.229.18`. E também, alterei o apontamento do `router R2` para `117.229.18.254`.

### _Goal 3: meson need to communicate with Internet._

- No `gateway` da `internet`, apenas coloquei o IP de rede `200.100.10.0/25`.

### _Goal 4: meson need to communicate with gluon._

- No `gateway` do `router R1`, coloquei o IP de rede `75.85.129.0/18` e apontamento para `117.229.18.253`.

### _Goal 5: ion need to communicate with cation._

- No `gateway` do `router R1`, coloquei o IP de rede `11.0.0.0/24` e apontamento para `117.229.18.253`.

### _Goal 6: cation need to communicate with Internet._

- No `gateway` da `internet`, apenas coloquei o IP de rede `11.0.0.0/24`.

![level09_solved](https://user-images.githubusercontent.com/83036509/200429429-f8c3b8e7-4b35-4f48-a940-d07523527173.png)


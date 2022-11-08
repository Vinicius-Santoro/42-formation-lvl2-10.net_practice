### _Project 10: net_pratice - Tenth project for the formation of software engineers at school 42 São Paulo._

🏠 [home](https://github.com/Vinicius-Santoro/42-formation-lvl2-10.net_pratice)<br>
⬅ [level 09](https://github.com/Vinicius-Santoro/42-formation-lvl2-10.net_pratice/blob/main/readmes/level09.md) 
<h1></h1>

### _This is `level 10`_

### _Task_

<h1></h1>

### _Goal 1: Host one need to communicate with Host two._
- O que podemos fazer inicialmente, é deixar todas as máscaras iguais da `interface R11`. 
- Como a `interface R11` possui IP de rede fixo `161.216.219.1`, podemos calcular o intervalo das redes.
- Para sabermos o intervalo de cada subrede, precisamos calcular o salto, que é (256 - (octeto misto)). Ou seja, 256 - 128 = 128.
- Há duas redes possíveis para o IP `161.216.219.*/25`.

<div align="center">
    
| Rede     |      Host     | Broadcast |
|:----------:|:-------------:|:------:|
| 161.216.219.0 | 161.216.219.1 - 161.216.219.126| 161.216.219.127
| 161.216.219.128 | 161.216.219.129 - 161.216.219.254| 161.216.219.255
  
</div>

### _Goal 2: Host three need to communicate with Host four._
- O que podemos fazer é deixar a máscara `255.255.255.192` nas `interfaces H41 e R23`.
- Deixamos a máscara `255.255.255.252` nas `interfaces H31 e R22`.
- Utilizamos a máscara `255.255.255.252` nas `interfaces H31 e R22` para não dar conflitos por redes em uso. Para calcularmos o salto aqui, devemos somar os saltos das `interfaces R11, R23`, sendo eles, respectivamente, `128 + 64 = 192`. Isso significa que podemos utilizar os hosts a partir de `192`, com saltos da máscara `255.255.255.252`, ou seja, de 4 em 4.
- Para sabermos o intervalo dessa cada subrede, precisamos calcular o salto, que é (256 - (octeto misto)). Ou seja, 256 - 252 = 4. (Lembrando que só podemos utilizar os hosts a partir de `192`, com saltos da máscara `255.255.255.252`).
- Há quatro redes possíveis para o IP `75.85.129.*/26`.

<div align="center">
    
| Rede       |      Host     |  Broadcast |
|:----------:|:-------------:|:----------:|
| 161.216.219.192| 161.216.219.193 - 161.216.219.194| 161.216.219.195
| 161.216.219.196| 161.216.219.197 - 161.216.219.198| 161.216.219.199
| 161.216.219.200| 161.216.219.201 - 161.216.219.202| 161.216.219.203
| 161.216.219.204| 161.216.219.205 - 161.216.219.206| 161.216.219.207
| 161.216.219.208| 161.216.219.209 - 161.216.219.210| 161.216.219.211
| 161.216.219.212| 161.216.219.213 - 161.216.219.214| 161.216.219.215
| 161.216.219.216| 161.216.219.217 - 161.216.219.218| 161.216.219.219
| 161.216.219.220| 161.216.219.221 - 161.216.219.222| 161.216.219.223
| 161.216.219.224| 161.216.219.225 - 161.216.219.226| 161.216.219.227
| 161.216.219.228| 161.216.219.229 - 161.216.219.230| 161.216.219.231
| 161.216.219.232| 161.216.219.233 - 161.216.219.234| 161.216.219.235
| 161.216.219.236| 161.216.219.237 - 161.216.219.238| 161.216.219.239
| 161.216.219.240| 161.216.219.241 - 161.216.219.242| 161.216.219.243
| 161.216.219.244| 161.216.219.245 - 161.216.219.246| 161.216.219.247
| 161.216.219.248| 161.216.219.249 - 161.216.219.250| 161.216.219.251
| 161.216.219.252| 161.216.219.253 - 161.216.219.254| 161.216.219.255
  
</div>

- Deixei o IP da `interface C1` e `interface R22` com a rede `11.0.0`.
- Para sabermos o intervalo de cada subrede, precisamos calcular o salto, que é (256 - (octeto misto)). Ou seja, 256 - 0 = 0.
- Há uma rede possível para o IP `11.0.0.*/24`.

<div align="center">
    
| Rede       |      Host     |  Broadcast |
|:----------:|:-------------:|:----------:|
| 	11.0.0.0| 11.0.0.1 - 11.0.0.254|	11.0.0.255
  
</div>

- Antes de continuar os objetivos, coloquei as `interfaces R13 e R2` no IP de rede `117.229.18`. E também, alterei o apontamento do `router R2` para `117.229.18.254` e o apontamento do `router R1` para .`117.229.18.253`.

### _Goal 3: meson need to communicate with Internet._

- No `gateway` da `internet`, apenas coloquei o IP de rede `200.100.10.0/25`.

### _Goal 4: meson need to communicate with gluon._

- No `gateway` do `router R1`, coloquei o IP de rede `75.85.129.0/18` e apontamento para `117.229.18.253`.

### _Goal 5: ion need to communicate with cation._

- No `gateway` do `router R1`, coloquei o IP de rede `11.0.0.0/24` e apontamento para `117.229.18.253`.

### _Goal 6: cation need to communicate with Internet._

- No `gateway` da `internet`, apenas coloquei o IP de rede `11.0.0.0/24`.

![level09_solved](https://user-images.githubusercontent.com/83036509/200429429-f8c3b8e7-4b35-4f48-a940-d07523527173.png)



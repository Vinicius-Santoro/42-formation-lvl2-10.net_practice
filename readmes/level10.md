### _Project 10: net_pratice - Tenth project for the formation of software engineers at school 42 São Paulo._

🏠 [home](https://github.com/Vinicius-Santoro/42-formation-lvl2-10.net_pratice)<br>
⬅ [level 09](https://github.com/Vinicius-Santoro/42-formation-lvl2-10.net_pratice/blob/main/readmes/level09.md) 
<h1></h1>

### _This is `level 10`_

![level10_unsolved](https://user-images.githubusercontent.com/83036509/200459985-895256a1-42ea-4cef-9627-a0e180d0daf2.png)

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

### _Goal 3: Host one need to communicate with Internet._

- Alteramos a máscara da `interface R13` para `255.255.255.252`. Isso já resultará na comunicação com o outro roteador.
- No `gateway` da `internet`, apenas coloquei o IP de rede `161.216.219.0/24`.
- A máscara no `gateway` da `internet` pode ser no intervalo de `0 até 24`. Porque o `/25` é a menor máscara usada, restringindo nosso intervalo.

### _Goal 4: Host one need to communicate with Host four._

- No `gateway` do `router R1`, coloquei o IP de rede `161.216.219.0/24`, referente ao `gateway` da `internet`. Eles devem ser iguais, respeitando o intervalo de `0 até 24.

### _Goal 5: Host two need to communicate with Host three._

- Os dois hosts já estão comunicados por conta do IP de rede `router R1`.

### _Goal 6: Host three need to communicate with Internet._

- O host já estão comunicado na internet por conta do IP de rede `router R1`.

### _Goal 7: Host four need to communicate with Internet._

- O host já estão comunicado na internet por conta do IP de rede `router R1`.

![level10_solved](https://user-images.githubusercontent.com/83036509/200460017-e8a9231e-d7eb-483f-8bb0-078c9f14314f.png)


### _Project 10: net_pratice - Tenth project for the formation of software engineers at school 42 São Paulo._

🏠 [home](https://github.com/Vinicius-Santoro/42-formation-lvl2-10.net_pratice)<br>
⬅ [level 07](https://github.com/Vinicius-Santoro/42-formation-lvl2-10.net_pratice/blob/main/readmes/level07.md) | [level 09](https://github.com/Vinicius-Santoro/42-formation-lvl2-10.net_pratice/blob/main/readmes/level09.md) ➡
<h1></h1>

### _This is `level 08`_

![level08_unsolved](https://user-images.githubusercontent.com/83036509/200423727-d467da6d-83dc-467d-ab1a-c02f54429574.png)

<h1></h1>

### _Goal 1:  office.non-real.com need to communicate with home.non-real.com._
- O que podemos fazer inicialmente, é deixar todas as máscaras iguais da `interface D1`. 
- Como o `router R2` mostra que a `interface R13` possui IP `146.27.96.62`, podemos calcular o intervalo de cada subrede.
- Para sabermos o intervalo de cada subrede, precisamos calcular o salto, que é (256 - (octeto misto)). Ou seja, 256 - 240 = 16.
- Há dezesseis redes possíveis para o IP `146.27.96.1.*`.

<div align="center">
    
| Rede     |      Host     | Broadcast |
|:----------:|:-------------:|:------:|
| 146.27.96.0 |   146.27.96.1 - 146.27.96.14| 146.27.96.15
| 146.27.96.16| 146.27.96.17 - 146.27.96.30| 146.27.96.31
| 146.27.96.32| 146.27.96.33 - 146.27.96.46| 146.27.96.47
| 146.27.96.48| 146.27.96.49 - 146.27.96.62| 146.27.96.63
| 146.27.96.64| 146.27.96.65 - 146.27.96.78| 146.27.96.79
| 146.27.96.80| 146.27.96.81 - 146.27.96.94| 146.27.96.95
| 146.27.96.96| 146.27.96.97 - 146.27.96.110| 146.27.96.111
| 146.27.96.112| 146.27.96.113 - 146.27.96.126| 146.27.96.127
| 146.27.96.128| 146.27.96.129 - 146.27.96.142| 146.27.96.143
| 146.27.96.144| 146.27.96.145 - 146.27.96.158| 146.27.96.159
| 146.27.96.160| 146.27.96.161 - 146.27.96.174| 146.27.96.175
| 146.27.96.176| 146.27.96.177 - 146.27.96.190| 146.27.96.191
| 146.27.96.192| 146.27.96.193 - 146.27.96.206| 146.27.96.207
| 146.27.96.208| 146.27.96.209 - 146.27.96.222| 146.27.96.223
| 146.27.96.224| 146.27.96.225 - 146.27.96.238| 146.27.96.239
| 146.27.96.240| 146.27.96.241 - 146.27.96.254| 146.27.96.255

</div>

- No caso, coloquei a `interface D1` e `interface R23` no intervalo `146.27.96.1 - 146.27.96.14`. E coloquei a `interface C1` e `interface R22` no intervalo `146.27.96.17 - 146.27.96.30`.
- Configurei os `gateways` de acordo com os IP's inseridos da task anterior. Lembrando, o `default (0.0.0.0/0)` tem a funcionalidade de 'a partir deste dispositivo'.

### _Goal 2 and 3:  office.non-real.com and home.non-real.com need to communicate with internet._
- Sabendo que a `interface R13` possui IP `146.27.96.62`, podemos concluir que a `interface R21` precisa estar no intervalo de ` 146.27.96.49 - 146.27.96.62`.
- No `router R1`, configuro a próximo ponto sendo o IP  da `interface R21`.
- Na `internet`, configuro a próximo ponto sendo o IP  da `interface R12`.

![level08_solved](https://user-images.githubusercontent.com/83036509/200423453-0f2c4f51-325d-4f6d-bef8-dd4e519189ac.png)

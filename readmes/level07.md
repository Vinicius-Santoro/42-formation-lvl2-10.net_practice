### _Project 10: net_pratice - Tenth project for the formation of software engineers at school 42 São Paulo._

🏠 [home](https://github.com/Vinicius-Santoro/42-formation-lvl2-10.net_pratice)<br>
⬅ [level 06](https://github.com/Vinicius-Santoro/42-formation-lvl2-10.net_pratice/blob/main/readmes/level06.md) | [level 07](https://github.com/Vinicius-Santoro/42-formation-lvl2-10.net_pratice/blob/main/readmes/level08.md) ➡
<h1></h1>

### _This is `level 07`_

![level07_unsolved](https://user-images.githubusercontent.com/83036509/200404670-bc52afe3-c0f7-45b7-af11-5b0b0fbc5624.png)

<h1></h1>

### _Goal 1: dev.non-real.net need to communicate with accounting.non-real.net._
- O que podemos fazer inicialmente, é deixar todas as máscaras iguais, usando por exemplo, a máscara `255.255.255.192`, que nos dará 4 intervalos para uso.
- Para sabermos o intervalo de cada subrede, precisamos calcular o salto, que é (256 - (octeto misto)). Ou seja, 256 - 192 = 64.
- Há quatro redes possíveis para o IP `91.198.14.1.*`.

<center>
<table>
    <thead>
        <tr align="center">
            <td align="center"><strong>Rede</strong></td>
            <td align="center"><strong>Host</strong></td>
            <td align="center"><strong>Broadcast</strong></td>
        </tr>
        <tr>
            <td align="center">91.198.14.0</td>
            <td align="center">91.198.14.1 - 91.198.14.62</td>
            <td align="center">	91.198.14.63</td>
        </tr>
         <tr>
            <td align="center">91.198.14.64</td>
            <td align="center">91.198.14.65 - 91.198.14.126</td>
            <td align="center">91.198.14.127</td>
        </tr>
        <tr>
            <td align="center">91.198.14.128</td>
            <td align="center">91.198.14.129 - 91.198.14.190</td>
            <td align="center">	91.198.14.191</td>
        </tr>
        <tr>
            <td align="center">91.198.14.192</td>
            <td align="center">91.198.14.193 - 91.198.14.254</td>
            <td align="center">91.198.14.255</td>
        </tr>
    </thead>
</table>
</center>

- No `gateway` do `cliente A`, configuraremos o IP com o próximo ponto do cliente, neste caso, o IP da `interface R11: 91.198.14.1`. O default tem a funcionalidade de 'a partir deste dispositivo'.
- Na `interface A1`, podemos colocar qualquer IP no intervalor de `91.198.14.1 - 91.198.14.62`, excluindo o IP `91.198.14.1`, pois ele já está sendo usado.
- No `gateway` do `router R1`, configuraremos o IP com o próximo ponto do cliente, neste caso, o IP da `interface R21`.
- Na `interface AR21`, podemos colocar qualquer IP no intervalor de `91.198.14.193 - 91.198.14.254`, excluindo o IP `91.198.14.254`, pois ele já está sendo usado.
- No `gateway` do `router R2`, configuraremos o IP com o próximo ponto do cliente, neste caso, o IP da `interface R12: 91.198.14.254`.
- Na `interface R22` e `interface C1`, podemos utilizar IP's dos intervalos disponíveis da tabela de hosts. No caso, utilizei o intervalo `91.198.14.65 - 91.198.14.126`.

![level07_solved](https://user-images.githubusercontent.com/83036509/200404408-c05510ed-f94e-45ef-8746-5ffc7dbfd731.png)
 

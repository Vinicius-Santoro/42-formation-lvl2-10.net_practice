### _Project 10: net_pratice - Tenth project for the formation of software engineers at school 42 São Paulo._

🏠 [home](https://github.com/Vinicius-Santoro/42-formation-lvl2-10.net_pratice)<br>
⬅ [level 01](https://github.com/Vinicius-Santoro/42-formation-lvl2-10.net_pratice/blob/main/readmes/level01.md) | [level 03](https://github.com/Vinicius-Santoro/42-formation-lvl2-10.net_pratice/blob/main/readmes/level03.md) ➡
<h1></h1>

### _This is `level 02`:_



### _Goal 1: Computer B need to communicate with Computer A._
-  O cliente A e o cliente B DEVEM ter a mesma máscara de Classe C.
- A interface B1 possui o IP 192.168.124.`222`, com isso podemos gerar a tabela de
todas as redes, hosts e broadcasts possíveis.
- Para sabermos o intervalo de cada subrede, precisamos calcular o salto, que é (256 - (octeto misto)). Ou seja, 256 - 224 = 32.

<table>
    <thead>
        <tr>
            <td align="center"><strong>Rede</strong></td>
            <td align="center"><strong>Host</strong></td>
            <td align="center"><strong>Broadcast</strong></td>
        </tr>
        <tr>
            <td align="center">192.168.124.<strong>0</strong></td>
        </tr>
         <tr>
            <td align="center">192.168.124.<strong>32</strong></td>
        </tr>
         <tr>
            <td align="center">192.168.124.<strong>64</strong></td>
        </tr>
        <tr>
            <td align="center">192.168.124.<strong>96</strong></td>
        </tr>
        <tr>
            <td align="center">192.168.124.<strong>128</strong></td>
        </tr>
        <tr>
            <td align="center">192.168.124.<strong>160</strong></td>
        </tr>
        <tr>
            <td align="center">192.168.124.<strong>192</strong></td>
        </tr>
        <tr>
            <td align="center">192.168.124.<strong>224</strong></td>
        </tr>
         <tr>
            <td align="center">192.168.124.<strong>224</strong></td>
        </tr>
    </thead>
</table>

<h1></h1>

### _Goal 2: My Mac need to communicate with my little sister's computer._
-  O cliente A e o cliente B possuem a mesma máscara de Classe B.
- A interface C1 possui o IP 211.191.`126.75`, com isso podemos gerar a tabela de
todas as redes, hosts e broadcasts possíveis.
- Para sabermos o intervalo de cada subrede, precisamos calcular o salto, que é (256 - (octeto misto)). Como não há octeto misto, essa rede possui um único intervalo, sendo de 0.1, até 255.254.
<table>
    <thead>
        <tr>
            <td align="center"><strong>Rede</strong></td>
            <td align="center"><strong>Host</strong></td>
            <td align="center"><strong>Broadcast</strong></td>
        </tr>
        <tr>
            <td align="center">211.191.<strong>0.0</strong></td>
            <td align="center">211.191.<strong>0.1</strong> até 211.191.<strong>255.254</strong></td>
            <td align="center">211.191.<strong>255.255</strong></td>
        </tr>
    </thead>
</table>

![level01_solved](https://user-images.githubusercontent.com/83036509/200187248-16a74205-b3de-48ef-817b-c772b1eb6e00.png)



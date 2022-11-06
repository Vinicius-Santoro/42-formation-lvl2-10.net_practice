### _Project 10: net_pratice - Tenth project for the formation of software engineers at school 42 São Paulo._

🏠 [home](https://github.com/Vinicius-Santoro/42-formation-lvl2-10.net_pratice) | 
[level 2](https://github.com/Vinicius-Santoro/42-formation-lvl2-10.net_pratice/blob/main/readmes/level02.md) ➡

<h1></h1>

### _This is `level 01`_

![level01_unsolved](https://user-images.githubusercontent.com/83036509/200187198-96728260-f044-452a-a4de-aad9741a4bc7.png)


### _Goal 1: My PC need to communicate with my little brother's computer._
-  O cliente A e o cliente B possuem a mesma máscara de Classe C.
- A interface B1 possui o IP 104.96.23.`12`, com isso podemos gerar a tabela de
todas as redes, hosts e broadcasts possíveis.
- Para sabermos o intervalo de cada subrede, precisamos calcular o salto, que é (256 - (octeto misto)). Como não há octeto misto, essa rede possui um único intervalo, sendo de 1, até 254.

<table>
    <thead>
        <tr>
            <td align="center">Rede</td>
            <td align="center">Host</td>
            <td align="center">Broadcast</td>
        </tr>
        <tr>
            <td align="center">104.96.23.0</td>
            <td align="center">104.96.23.1 até 104.96.23.254</td>
            <td align="center">104.96.23.255</td>
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
            <td align="center">Rede</td>
            <td align="center">Host</td>
            <td align="center">Broadcast</td>
        </tr>
        <tr>
            <td align="center">211.191.0.0</td>
            <td align="center">211.191.0.1 até 211.191.255.254</td>
            <td align="center">211.191.255.255</td>
        </tr>
    </thead>
</table>

![level01_solved](https://user-images.githubusercontent.com/83036509/200187248-16a74205-b3de-48ef-817b-c772b1eb6e00.png)

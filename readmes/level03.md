### _Project 10: net_pratice - Tenth project for the formation of software engineers at school 42 São Paulo._

🏠 [home](https://github.com/Vinicius-Santoro/42-formation-lvl2-10.net_pratice)<br>
⬅ [level 02](https://github.com/Vinicius-Santoro/42-formation-lvl2-10.net_pratice/blob/main/readmes/level02.md) | [level 04](https://github.com/Vinicius-Santoro/42-formation-lvl2-10.net_pratice/blob/main/readmes/level04.md) ➡
<h1></h1>

### _This is `level 03`:_

![level03_unsolved](https://user-images.githubusercontent.com/83036509/200192523-aabd0b76-8e0b-4e0a-a267-5015831e1a53.png)

<h1></h1>

- O que podemos fazer inicialmente, é deixar todos os clientes com a mesma máscara. Ou seja, todos os clientes terão a máscara de classe C `255.255.255.128`.
- A `inteface A1` possui o endereço de rede `104.198.107`, com isso podemos gerar a tabela de todas as redes, hosts e broadcasts possíveis.
- Para sabermos o intervalo de cada subrede, precisamos calcular o salto, que é (256 - (octeto misto)). Ou seja, 256 - 128 = 128.
- Há duas redes possíveis para o IP `104.198.107`.

<table>
    <thead>
        <tr>
            <td align="center">Rede</td>
            <td align="center">Host</td>
            <td align="center">Broadcast</td>
        </tr>
        <tr>
            <td align="center">104.198.107.0</td>
            <td align="center">104.198.107.1 - 104.198.107.126</td>
            <td align="center">104.198.107.127</td>
        </tr>
         <tr>
            <td align="center">104.198.107.128</td>
            <td align="center">104.198.107.129 - 104.198.107.254</td>
            <td align="center">104.198.107.255</td>
        </tr>
    </thead>
</table>

- Como o `cliente A` possui IP fixo, temos que utilizar o intervalo `104.198.107.1 - 104.198.107.126`.

![level03_solved](https://user-images.githubusercontent.com/83036509/200192865-84393901-7a6a-4bb2-b338-fdb1f9888b5c.png)



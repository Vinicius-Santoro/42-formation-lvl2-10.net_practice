### _Project 10: net_pratice - Tenth project for the formation of software engineers at school 42 São Paulo._

🏠 [home](https://github.com/Vinicius-Santoro/42-formation-lvl2-10.net_pratice)<br>
⬅ [level 03](https://github.com/Vinicius-Santoro/42-formation-lvl2-10.net_pratice/blob/main/readmes/level03.md) | [level 05](https://github.com/Vinicius-Santoro/42-formation-lvl2-10.net_pratice/blob/main/readmes/level05.md) ➡
<h1></h1>

### _This is `level 04`:_

![level04_unsolved](https://user-images.githubusercontent.com/83036509/200193506-b9b7d213-ece3-4cf8-a28a-f56e417f2c3b.png)

<h1></h1>

- O que podemos fazer inicialmente, é deixar todos os clientes com a mesma máscara. Ou seja, todos os clientes terão a máscara de classe C `255.255.255.128`.
- A `inteface A1` possui o endereço de rede `113.210.111`, com isso podemos gerar a tabela de todas as redes, hosts e broadcasts possíveis.
- Para sabermos o intervalo de cada subrede, precisamos calcular o salto, que é (256 - (octeto misto)). Ou seja, 256 - 128 = 128.
- Há duas redes possíveis para o IP `113.210.111`.

<table>
    <thead>
        <tr>
            <td align="center">Rede</td>
            <td align="center">Host</td>
            <td align="center">Broadcast</td>
        </tr>
        <tr>
            <td align="center">113.210.111.0</td>
            <td align="center">113.210.111.1 - 113.210.111.126</td>
            <td align="center">113.210.111.127</td>
        </tr>
         <tr>
            <td align="center">113.210.111.128</td>
            <td align="center">113.210.111.129 - 113.210.111.254</td>
            <td align="center">	113.210.111.255</td>
        </tr>
    </thead>
</table>

- Como o `cliente A` possui IP fixo, temos que utilizar o intervalo `113.210.111.129 - 113.210.111.254`. Porém, como a `interface R3` possui máscara `255.255.255.192`, o intervalo que temos de hosts disponíves agora é de `113.210.111.129 - 113.210.111.192`

![level04_solved](https://user-images.githubusercontent.com/83036509/200193522-ad4f4451-258d-4916-9637-07a85f1131e9.png)


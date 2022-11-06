### _Project 10: net_pratice - Tenth project for the formation of software engineers at school 42 São Paulo._

🏠 [home](https://github.com/Vinicius-Santoro/42-formation-lvl2-10.net_pratice)<br>
⬅ [level 05](https://github.com/Vinicius-Santoro/42-formation-lvl2-10.net_pratice/blob/main/readmes/level05.md) | [level 07](https://github.com/Vinicius-Santoro/42-formation-lvl2-10.net_pratice/blob/main/readmes/level07.md) ➡
<h1></h1>

### _This is `level 06`:_

![level06_unsolved](https://user-images.githubusercontent.com/83036509/200199432-0576ccdb-0068-4076-ac1a-b01f4afb6825.png)

<h1></h1>

### _Goal 1: Interface A1 need to communicate with interface Somewhere on the Net._
- O que podemos fazer inicialmente, é colocar a `interface A1` com a mesma máscara da `interface R1`.
- A `inteface A1` possui o endereço de rede `120.177.255`, com isso podemos gerar a tabela de todas as redes, hosts e broadcasts possíveis.
- Para sabermos o intervalo de cada subrede, precisamos calcular o salto, que é (256 - (octeto misto)). Ou seja, 256 - 128 = 128.
- Há duas redes possíveis para o IP `120.177.255.*`.

<table>
    <thead>
        <tr>
            <td align="center">Rede</td>
            <td align="center">Host</td>
            <td align="center">Broadcast</td>
        </tr>
        <tr>
            <td align="center">120.177.255.0</td>
            <td align="center">120.177.255.1 - 120.177.255.126</td>
            <td align="center">120.177.255.127</td>
        </tr>
         <tr>
            <td align="center">120.177.255.128</td>
            <td align="center">120.177.255.129 - 120.177.255.254</td>
            <td align="center">120.177.255.255</td>
        </tr>
    </thead>
</table>

- No `gateway` do `cliente A`, configuraremos o IP com o próximo ponto do cliente, neste caso, o IP da `interface R1`. O default tem a funcionalidade de 'a partir deste dispositivo'.
- Como o `Interface A1` possui IP fixo, temos que utilizar o intervalo `120.177.255.129 - 120.177.255.254` na `interface R1`.
 No `gateway` do `internet`, configuraremos com o IP da rede da `interface R1`, ou seja, `120.177.255.0/16`, especificando a máscara `/16`.
 
 ![level06_solved](https://user-images.githubusercontent.com/83036509/200199381-adc8e0af-3cc3-4bf7-a03f-500e16f75c09.png)

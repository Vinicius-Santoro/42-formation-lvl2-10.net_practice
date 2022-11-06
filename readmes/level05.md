### _Project 10: net_pratice - Tenth project for the formation of software engineers at school 42 São Paulo._

🏠 [home](https://github.com/Vinicius-Santoro/42-formation-lvl2-10.net_pratice)<br>
⬅ [level 04](https://github.com/Vinicius-Santoro/42-formation-lvl2-10.net_pratice/blob/main/readmes/level04.md) | [level 06](https://github.com/Vinicius-Santoro/42-formation-lvl2-10.net_pratice/blob/main/readmes/level06.md) ➡
<h1></h1>

### _This is `level 05`:_

![level05_unsolved](https://user-images.githubusercontent.com/83036509/200198437-ef1f8fc5-930c-4034-9f9f-6715b8a66b0a.png)

<h1></h1>

### _Goal 1: Machine A need to communicate with The Mighty Router._
- O que podemos fazer inicialmente, é colocar a `interface A1` com a mesma máscara da `interface R1`.
- A `inteface R1` possui o endereço de rede `39.70.193`, com isso podemos gerar a tabela de todas as redes, hosts e broadcasts possíveis.
- Para sabermos o intervalo de cada subrede, precisamos calcular o salto, que é (256 - (octeto misto)). Ou seja, 256 - 128 = 128.
- Há duas redes possíveis para o IP `39.70.193.255`.

<table>
    <thead>
        <tr>
            <td align="center">Rede</td>
            <td align="center">Host</td>
            <td align="center">Broadcast</td>
        </tr>
        <tr>
            <td align="center">39.70.193.0</td>
            <td align="center">39.70.193.1 - 39.70.193.126</td>
            <td align="center">39.70.193.127</td>
        </tr>
         <tr>
            <td align="center">39.70.193.128</td>
            <td align="center">39.70.193.129 - 39.70.193.254</td>
            <td align="center">39.70.193.255</td>
        </tr>
    </thead>
</table>

- Configuramos o `gateway` com o próximo ponto do cliente, neste caso, o IP da `interface R1`.
- O default tem a funcionalidade de 'a partir deste dispositivo'.

### _Goal 2: Machine B need to communicate with The Mighty Router._
- Colocamos a `interface B1` com a mesma máscara da `interface R2`.
- A `inteface R2` possui o endereço de rede `148.210`, com isso podemos gerar a tabela de todas as redes, hosts e broadcasts possíveis.
- Para sabermos o intervalo de cada subrede, precisamos calcular o salto, que é (256 - (octeto misto)). Ou seja, 256 - 192 = 64.
- Há quatro redes possíveis para o IP `39.70.193.255`.

<table>
    <thead>
        <tr>
            <td align="center">Rede</td>
            <td align="center">Host</td>
            <td align="center">Broadcast</td>
        </tr>
        <tr>
            <td align="center">148.210.0.0</td>
            <td align="center">148.210.0.1 - 148.210.63.254</td>
            <td align="center">	148.210.63.255</td>
        </tr>
         <tr>
            <td align="center">148.210.64.0</td>
            <td align="center">148.210.64.1 - 148.210.127.254</td>
            <td align="center">148.210.127.255</td>
        </tr>
        <tr>
            <td align="center">148.210.128.0</td>
            <td align="center">148.210.128.1 - 148.210.191.254</td>
            <td align="center">148.210.191.255</td>
        </tr>
         <tr>
            <td align="center">148.210.192.0</td>
            <td align="center">148.210.192.1 - 148.210.255.254</td>
            <td align="center">148.210.255.255</td>
        </tr>
    </thead>
</table>

- Configuramos o `gateway` com o próximo ponto do cliente, neste caso, o IP da `interface R2`.
- O default tem a funcionalidade de 'a partir deste dispositivo'.

![level05_solved](https://user-images.githubusercontent.com/83036509/200198397-99ecbba8-e6a6-4fbc-9872-f68c6bce4552.png)



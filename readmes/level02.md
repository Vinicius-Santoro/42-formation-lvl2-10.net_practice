### _Project 10: net_pratice - Tenth project for the formation of software engineers at school 42 São Paulo._

🏠 [home](https://github.com/Vinicius-Santoro/42-formation-lvl2-10.net_pratice)<br>
⬅ [level 01](https://github.com/Vinicius-Santoro/42-formation-lvl2-10.net_pratice/blob/main/readmes/level01.md) | [level 03](https://github.com/Vinicius-Santoro/42-formation-lvl2-10.net_pratice/blob/main/readmes/level03.md) ➡
<h1></h1>

### _This is `level 02`:_

![level02_unsolved](https://user-images.githubusercontent.com/83036509/200188665-5eb0f947-5521-4d5b-89ad-d2cc3b3b00a3.png)


### _Goal 1: Computer B need to communicate with Computer A._
-  O cliente A e o cliente B DEVEM ter a mesma máscara de Classe C.
- A interface B1 possui o IP 192.168.124.`222`, com isso podemos gerar a tabela de
todas as redes, hosts e broadcasts possíveis.
- Para sabermos o intervalo de cada subrede, precisamos calcular o salto, que é (256 - (octeto misto)). Ou seja, 256 - 224 = 32.

<table>
    <thead>
        <tr>
            <td align="center">Rede</td>
            <td align="center">Host</td>
            <td align="center">Broadcast</td>
        </tr>
        <tr>
            <td align="center">192.168.124.0</td>
            <td align="center">192.168.124.1 até 192.168.124.30</td>
            <td align="center">192.168.124.31</td>
        </tr>
         <tr>
            <td align="center">192.168.124.32</td>
            <td align="center">192.168.124.33 até 192.168.124.62</td>
            <td align="center">192.168.124.63</td>
        </tr>
         <tr>
            <td align="center">192.168.124.64</td>
            <td align="center">192.168.124.65 até 192.168.124.94</td>
            <td align="center">192.168.124.95</td>
        </tr>
        <tr>
            <td align="center">192.168.124.96</td>
            <td align="center">192.168.124.97 até 192.168.124.126</td>
            <td align="center">192.168.124.127</td>
        </tr>
        <tr>
            <td align="center">192.168.124.128</td>
            <td align="center">192.168.124.129 até 192.168.124.158</td>
            <td align="center">192.168.124.159</td>
        </tr>
        <tr>
            <td align="center">192.168.124.160</td>
            <td align="center">192.168.124.161 até 192.168.124.190</td>
            <td align="center">192.168.124.191</td>
        </tr>
        <tr>
            <td align="center">192.168.124.160</td>
            <td align="center">192.168.124.129 até 192.168.124.158</td>
            <td align="center">192.168.124.159</td>
        </tr>
         <tr>
            <td align="center">192.168.124.192</td>
            <td align="center">192.168.124.193 até 192.168.124.222</td>
            <td align="center">192.168.124.223</td>
        </tr>
         <tr>
            <td align="center">192.168.124.224</td>
            <td align="center">192.168.124.225 até 192.168.124.254</td>
            <td align="center">192.168.124.255</td>
        </tr>
    </thead>
</table>

<h1></h1>

### _Goal 2: My Mac need to communicate with my little sister's computer._
-  O cliente C e o cliente D possuem a mesma máscara de Classe C. O `/30`é a notação da máscara `255.255.255.252`.
- Como nenhuma interface possui IP fixo, podemos criar de acordo com a tabela de
todas as redes, hosts e broadcasts possíveis. Vamo usar o IP 192.168.10.1 para o exemplo.
- Para sabermos o intervalo de cada subrede, precisamos calcular o salto, que é (256 - (octeto misto)). Ou seja, 256 - 252 = 4.
- Teremos 64 redes disponíveis para o IP: 192.168.10.* 
<table>
    <thead>
        <tr>
            <td align="center">Rede</td>
            <td align="center">Host</td>
            <td align="center">Broadcast</td>
        </tr>
         <tr>
            <td align="center">192.168.10.0</td>
            <td align="center">	192.168.10.1 - 192.168.10.2</td>
            <td align="center">192.168.10.3</td>
        </tr>
         <tr>
            <td align="center">192.168.10.4</td>
            <td align="center">192.168.10.5 - 192.168.10.6</td>
            <td align="center">192.168.10.7</td>
        </tr>
         <tr>
            <td align="center">...</td>
            <td align="center">... - ...</td>
            <td align="center">...</td>
        </tr>
         <tr>
            <td align="center">192.168.10.248</td>
            <td align="center">192.168.10.249 - 192.168.10.250</td>
            <td align="center">192.168.10.251</td>
        </tr>
         <tr>
            <td align="center">192.168.10.252</td>
            <td align="center">192.168.10.253 - 192.168.10.254</td>
            <td align="center">192.168.10.255</td>
        </tr>
    </thead>
</table>

![level02_solved](https://user-images.githubusercontent.com/83036509/200188824-e35810fb-710a-465c-92bc-c07609bbf625.png)

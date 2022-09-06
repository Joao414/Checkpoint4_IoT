# Como Funciona

O nó Inject, na primeira ligação, envia uma tag RFID em formato JSON que é publicado em um tópico MQTT chamado "TagRFID", na segunda ligação, a tag é enviada para um nó debug e, na terceira ligação, é inserido um nó Function que também recebe a tag e retorna uma mensagem que, por sua vez, é enviada para o último nó desse fluxo, um Telegram Sender(esse nó está conectado à um bot no telegram que receberá a tag RFID, conforme segunda imagem abaixo).

![image](https://user-images.githubusercontent.com/79977429/188530769-44f4bfe6-4d1d-47f2-8c39-392bedea4d7d.png)
![image](https://user-images.githubusercontent.com/79977429/188531379-bae2ed19-af56-4aa0-898e-e8e1c2e8a302.png)



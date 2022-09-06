# Como Funciona

O nó Inject, na primeira ligação, envia uma tag RFID em formato JSON que é publicado em um tópico MQTT chamado "TagRFID". Na segunda ligação, a tag é enviada para um nó debug e, na terceira ligação, é inserido um nó "Function" que também recebe a tag e retorna uma mensagem que, por sua vez, é enviada para o último nó desse fluxo, um "Telegram Sender"(esse nó está conectado à um bot no telegram que receberá a tag RFID, conforme segunda imagem abaixo).

![image](https://user-images.githubusercontent.com/79977429/188530769-44f4bfe6-4d1d-47f2-8c39-392bedea4d7d.png)
![image](https://user-images.githubusercontent.com/79977429/188531379-bae2ed19-af56-4aa0-898e-e8e1c2e8a302.png)

O fluxo localizado abaixo inicia com um nó "mqttt in" que irá pegar a tag que foi publicada no tópico "TagRFID" e enviará para um nó JSON que, por sua vez, receberá a tag, transformando-a em formato json. Em seguida, a tag é enviada para um nó "Change" que irá selecionar a tag e envia-la para o último nó 
"text input" que exibirá a mesma em um dashboard(conforme segunda imagem).

![image](https://user-images.githubusercontent.com/79977429/188535132-01501684-4a52-4822-b432-19ee8ec91276.png)
![image](https://user-images.githubusercontent.com/79977429/188536446-a284e26f-74d5-4ac0-98d8-d204b1c73243.png)


Fluxo completo:

![image](https://user-images.githubusercontent.com/79977429/188536673-8feac693-65f4-4f1c-9df8-45a6f0400e8c.png)

![chat-benefits](https://user-images.githubusercontent.com/40874530/101500214-ecea2e00-394c-11eb-9f7f-00f598378812.png)
### Features

- Leitura do mural de mensagens;
- Post de mensagens pelo colaborador;
- Organização dos colaboradores por ID;
- Performace do codigo em python 3;
- Aplicação dockerizada e escalavel;
- Metodos http POST e GET definidos na requisição.
------------

###Requisitos

- Ter instalado:  Docker,  Git, Postman.
- S.O linux.

------------

###Modo de uso

> 1 Clone o projeto:

[Link github](https://github.com/gblbjj/api-flask>)

> 2 Build  e deploy do container:
- Navegue até o projeto clonado.
- Encontre o arquivo bash service.sh
- Execute sudo chmod +x service.sh
- Agora execute sh service.sh
- Se você executar o comando netstat no terminal netstat -nlpt a seguinte saida será apresentada(:::5000), isso quer dizer que nosso container esta rodando e aplicação tambem.

> 3 Consultar mural de mensagens
- Abra o postman e solicite uma nova guia com a requisição para GET.
- Consultaremos a seguinte URL http://127.0.0.1:5000/colaborador/ (Não se preocupe as configuração na aplicação e container vão direcionar todo trafego para porta 5000).

> 4 Postando mensagens 
- Com o postman aberto ainda solicitamos uma nova guia para requisição POST.
- Usaremos a mesma URL http://127.0.0.1:5000/colaborador/ .
- Clique  em Body, depois em raw e logo em seguite no type altere type de text para json.
- Use o seguinte modelo  json:

| Modelo | Description                    |
| ------------- | ------------------------------ |
| `"id"`      | O ID do colaborador será atribuido altomaticamente.       |
| `"mensagem"`   | A mensagem se ser postada pelo colaborador    |
| `"nome"`   | Nome do colaborador a ser registrado junto com seu feedback   |



|Exemplo pratico|
| -------- |
> {
        "id":"" ,
        "mensagem": "Me acustumando ao novo normal",
        "nome": "joão"
    }

- Após realizar o post você recebera a mensagem()
- Consultaremos a seguinte URL http://127.0.0.1:5000/colaborador/ novamente paravermos id, nome e comentarios postados. 

**Desenvolvido por:**
> Gabriel Oliveira
[LinkedIn](https://www.linkedin.com/in/gabriel-oliveira-553168163/)

###END
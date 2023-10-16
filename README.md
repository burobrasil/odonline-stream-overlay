# Galeria de Stream Overlays de ODOnline

No [Old Dragon Online](https://olddragon.com.br/online), qualquer jogador pode criar sua ficha de personagem para Old Dragon Segunda Edição (OD2). E através da API aberta e gratuita, dados da ficha podem ser facilmente lidos e integrados por outras ferramentas.

Para quem faz stream de suas aventuras de OD2 usando o OBS, é possível fazer uso destas informações dinâmicas de maneira fácil e bem personalizável.

## Configuração

1. Baixe o arquivo "minimalista.html" deste repositório.
2. Duplique este arquivo, para ter um por personagem.
3. Atualize cada arquivo, procurando a linha `const id = "59a2adaf-96e6-4569-827b-a172982cf13c";` e trocando o ID para o desejado. Você descobre o ID do seu personagem simplesmente abrindo sua ficha no OD Online e extraindo da URL. Se sua URL é `https://olddragon.com.br/personagens/aaac1efd-51a1-4140-9cb3-7f139f5bbd2a`, então a linha deverá ser atualizada com `const id = "aaac1efd-51a1-4140-9cb3-7f139f5bbd2a";`. Salve (grave) o arquivo quando terminar. Você pode abrir este arquivo em um navegador (como o Chrome) para garantir que funciona.
4. Abra o OBS, vá em "Fontes" (Sources), depois em "Navegador" (Browser). Aponte para o arquivo local do personagem que deseja. Configure a altura e largura para algo que deseja, algo como 100 de largura e 50 de altura.
5. Posicione na tela em qual lugar você quer que a vida apareça.

Uma vez que garantir que funciona, você pode realizar alterações no arquivo HTML mexendo na cor, no tamanho, na fonte, e até mesmo adicionando outros campos além da vida. Sempre que fizer alterações no arquivo, lembre de salvar, então volte ao OBS, selecione o elemento, e clique no botão "Atualizar" (Refresh) para que o arquivo seja carregado novamente, já que o mesmo não é atualizado automaticamente.

Por padrão, o arquivo atualiza as informações da API a cada 30 segundos, portanto uma alteração na ficha do personagem pode demorar até 30 segundos para aparecer na transmissão. Recomendamos deixar este valor como está ou deixar, no mínimo, em 15 segundos, já que diminuir demais irá fazer com que várias requisições sejam enviadas ao servidor, que pode pensar que é um ataque e cortar o acesso do seu IP por um tempo por questões de segurança e auto-preservação.

Para outros elementos, veja a documentação sobre personagens de nossa API aberta: [Obter personagem específico](https://github.com/burobrasil/olddragon-api/blob/main/capitulos/personagens.md#obter-personagem-espec%C3%ADfico)

## Colaborações

Criou um overlay maneiro e quer compartilhar? Abra um PR neste repositório!

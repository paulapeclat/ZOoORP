# zoorp

**zoorp** (ZOoO RP) é um jogo de roleplay no Roblox ambientado em uma cidade com zoológico. Ele foi criado e é mantido por [Paula Peclat](https://paulapeclat.com.br).

> Este repositório apresenta o projeto. O código-fonte e os dados do jogo são privados e não fazem parte dele.

![HUD do jogo](imagens/hud.jpg)

## O jogo

O jogador explora uma cidade com zoológico, aquário, lojas, parque, skate park e casas. Durante o dia o zoo fica aberto para visitação. À noite o portão fecha e aparecem os bandidos.

- **Zoológico vivo** com ciclo de dia e noite, música própria para cada período e NPCs visitantes
- **Casas** em terrenos que o jogador compra, com cinco modelos para escolher
- **Carros** chamados pelo menu, com sedãs, SUVs, picapes, esportivos, viatura e motos
- **Roupas e acessórios** com loja, guarda-roupa e equipar por ID
- **Celular** dentro do jogo, com aplicativos de telefone, mensagens e banco
- **Recompensa diária** em uma sequência de 7 dias
- **Eventos** sazonais e o evento especial Aurora
- **Emblemas** e ranking de tempo jogado

## Interface

As telas seguem um único padrão visual, chamado *Zoo aventura*: painéis creme com borda de madeira, títulos em faixa verde, ações em verde e fechar em vermelho.

| Roupas | Carros |
| --- | --- |
| ![Roupas](imagens/roupas.jpg) | ![Carros](imagens/carros.jpg) |

| Prêmio diário | Loja |
| --- | --- |
| ![Prêmio diário](imagens/diario.jpg) | ![Loja](imagens/loja.jpg) |

| Busca de itens | |
| --- | --- |
| ![Busca de itens](imagens/busca.jpg) | Os botões usam ícones em vez de texto, para que crianças de qualquer idade entendam a ação sem precisar ler. |

## Feedback ao jogador

O jogo responde a cada ação com som, movimento e texto, como fazem os jogos mais jogados da plataforma.

- moedas que saem do personagem e voam até a carteira, com um "+N" flutuante e o contador subindo
- tela de recompensa com raios girando, confete e um botão de coletar
- avisos curtos no topo da tela para compras, erros e eventos
- borda vermelha, número de dano e tremor de câmera quando o jogador é atingido
- uma tela aberta por vez, com animação ao abrir e botão para fechar

![Tela de recompensa](imagens/recompensa.jpg)

## Arquitetura (visão geral)

- **Servidor autoritativo**: compras, moedas e casas são validadas no servidor, com limite de frequência e checagem de tipos em todos os eventos remotos.
- **Controlador de interface** no cliente, que coordena as telas e aplica o padrão de botões.
- **Módulo de recompensas visuais** reutilizado por todos os sistemas.
- **Streaming** do mapa ligado para rodar melhor em celulares.

## Tecnologias

Roblox Studio · Luau

## Autoria

Projeto de Paula Peclat, educadora e desenvolvedora de jogos.
Site: [paulapeclat.com.br](https://paulapeclat.com.br) · Instagram: [@paulapeclat.oficial](https://instagram.com/paulapeclat.oficial)

Todos os direitos reservados. As imagens e a descrição deste repositório não podem ser reutilizadas sem autorização.

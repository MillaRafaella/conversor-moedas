🪙 Conversor de Moedas — Java + API ExchangeRate

Este projeto é um Conversor de Moedas em Java, desenvolvido como parte de um desafio prático.
Ele utiliza a ExchangeRate-API para obter taxas de câmbio em tempo real e oferece uma interface simples via console, permitindo que o usuário escolha opções de conversão, informe valores e visualize o resultado.

Além disso, inclui recursos extras como histórico de conversões com registro de data e hora e suporte a múltiplas moedas.

📌 Funcionalidades
✔ Conversão entre diferentes moedas

As conversões seguem o menu principal:

USD → ARS
ARS → USD
USD → BRL
BRL → USD
USD → COP
COP → USD

✔ Consulta de taxas via API

As taxas são obtidas através da ExchangeRate-API utilizando a rota:

https://v6.exchangerate-api.com/v6/SUA-CHAVE/pair/MOEDA_ORIGEM/MOEDA_DESTINO

✔ Extra: Histórico de Conversões (opcional)

O sistema registra:

Moeda de origem
Moeda de destino
Valor original
Valor convertido
Data e hora da operação

O usuário pode visualizar esse histórico pelo menu.

✔ Extra: Suporte a mais moedas

Foi adicionada uma lista expandida de moedas aceitas:

ARS
BOB
BRL
CLP
COP
USD
EUR
MXN
PEN
PYG
UYU

✔ Extra: Logs com timestamp

Cada registro inclui data e hora formatadas com java.time.

🧱 Estrutura do Projeto
src/
 ├── Main.java                 # Menu e interação com o usuário
 ├── ClienteHttp.java          # Requisições HTTP usando HttpClient
 ├── ConversorMoedas.java      # Lógica da conversão
 ├── ConversorJson.java        # Leitura do JSON usando Gson
 ├── FiltroMoedas.java         # Lista de moedas permitidas
 └── RegistroConversao.java    # Histórico e logs de conversões

🛠 Tecnologias Utilizadas

Java 17+
HttpClient (Java)
Gson — análise de JSON
ExchangeRate-API
Scanner — entrada do usuário
java.time.LocalDateTime — logs
Estruturas de dados (List)

▶️ Como Executar

1- Clone o repositório:
git clone https://github.com/SEU_USUARIO/conversor-moedas.git

2- Importe no IntelliJ IDEA (ou outro editor).
3- Certifique-se de adicionar a biblioteca Gson.
4- Execute a classe:
Main.java

🧩 Como usar

Ao rodar o programa, um menu será exibido:

1- Dólar           => Peso Argentino
2- Peso Argentino  => Dólar
3- Dólar           => Real Brasileiro
4- Real Brasileiro => Dólar
5- Dólar           => Peso Colombiano
6- Peso Colombiano => Dólar
7- Ver histórico de conversões
8- Sair


O usuário deve:

Escolher uma opção numérica
Informar o valor que deseja converter
Receber o valor convertido

Exemplo:
Digite o valor que deseja converter:
100
Valor 100.00 [USD] corresponde ao valor final de 486.65 [BRL]


O histórico também pode ser visto:
=== Histórico de conversões ===
[16/11/2025 21:42:45] 100.00 USD -> 486.65 BRL


🔧 Possíveis Melhorias Futuras

Interface gráfica (JavaFX)
Salvamento do histórico em arquivo
Carregar histórico ao iniciar
Testes unitários com JUnit
Conversão livre (digitando qualquer moeda)
Tratamento avançado de erros da API

📜 Licença

Este projeto é livre para estudos, melhorias e personalização.



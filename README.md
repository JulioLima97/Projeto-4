Don't read Portuguese? [Read this page in English](https://github.com/JulioLima97/Projeto-4/blob/main/README-en.md)
# Projeto-4

## Descrição do Projeto
Neste projeto eu trabalho como analista para a empresa de telecomunicações Megaline. A empresa oferece aos seus cliente planos pré-pagos, Surf e Ultimate. O departamento comercial quer saber quais dos planos dão mais receita para ajustar o orçamento de publicidade.

Eu vou realizar uma primeira análise dos planos baseados em uma pequena seleção de clientes, onde terei dados de 500 clientes da Megaline: que clientes são, de onde eles são, qual plano usam, o número de chamadas que eles fizeram e mensagens que eles enviaram em 2018. O meu trabalho é analisar o comportamento dos clientes e determinar quais planos pré-pagos dão mais receita.

## Descrição dos dados

Lembre-se! A Megaline arredonda segundos para minutos e megabytes para gigabytes. Para chamadas, cada chamada individual é arredondada para cima: mesmo se uma chamada tenha durado apenas um segundo, será contado como um minuto. Para trafego de web, sessões individuais de web não são arredondadas para cima.. Ao invés disso, o total do mês é arredondado para cima. Se alguém usar 1025 megabytes esse mês, eles serão cobrados por 2 gigabytes.

A tabela `users` (dados sobre usuários):
- `user_id`: identificação do usuário
- `first_name`: nome do usuário
- `last_name`: último sobrenome do usuário
- `age`: idade do usuário (em anos)
- `reg_date`: data da inscrição (dd, mm, aa)
- `churn_date`: a data que o usuário parou de usar o serviço (se o valor for ausente, o plano estava sendo usado quando esse dado foi gerado)
- `city`: cidade de residência do usuário
- `plan`: nome do plano
A tabela `calls` (dados sobre as chamadas)  

- `id`: identificador de chamada unívoco
- `call_date`: data da chamada
- `duration`: duração da chamada (em minutos)
- `user_id`: o identificador do usuário que faz a chamada  
  
A tabela `messages` (dados nas mensagens de texto):
- `id`: identificador unívoco de mensagem de textos
- `message_date`: data da mensagem de texto
- `user_id`: o identificador do usuário que envia a mensagem de texto  

A tabela `internet` (dados sobre sessões web):
- `id`: identificador de sessão unívoco
- `mb_used`: — o volume de dados gasto durante a sessão ( em megabytes)
- `session_date` — data da sessão web
- `user_id`: identificador do usuário  
  
A tabela `plans`(dados sobre os planos):
- `plan_name`: o nome do plano de chamadas
- `usd_monthly_fee`: preço mensal em dólares dos EUA
- `minutes_included`: pacote de minutos mensal
- `messages_included`: pacote de mensagens de texto mensal
- `mb_per_month_included`: pacote de volume de dados (em megabytes)
- `usd_per_minute`: preço por minuto depois de exceder o limite do pacote (por exemplo, se o pacote inclui 100 minutos, o primeiro minuto excedente será cobrado)
- `usd_per_message`: preço por mensagem de texto depois de exceder o limite do pacote
- `usd_per_gb`: preço por gigabyte extra de dados após exceder o limite do pacote (1 GB = 1024 megabytes)

# monitor de preços
Ira acessar sites de lojas e mandar alertas no email caso haja alterações nos preços dos produtos.

                            Objetivos do sistema

-> O sistema acessa links de produtos inseridos pelo usuário

-> O sistema comparara o preço atual com o preço definido pelo
usuário.

-> O sistema utliza inteligencia artificial para coletar os preços
encontrados no html retornado pela classe BeautifulSoup.

-> O sistema irá integrar a inteligência artificial usando uma API

-> A inteligência artificial auxiliara também na descoberta de falhas na 
requisição aos links.  

-> Caso o sistema identifique uma baixa nos preços (conforme o valor
definido pelo usuário), o sistema enviara um email para o usuário
com as informações do produto e da loja.


                        Pré-requisitos e Instalação
-> Antes de utilizar o sistema, certifique-se de que o python tenha
as dependências necessárias executando o seguinte o comando no seu
terminal: pip install requests beautifulsoup4 google-genai python-dotenv


                        Como utilizar o sistema

-> 1°: Execute todas as bibliotecas presentes na 1° celula.

-> 2°: Acesse o GOOGLE IA STUDIO e crie uma chave de API: https://aistudio.google.com/apps

-> 3°: Adicione a chave de API na variável CHAVE_API

-> 4°: Coloque o seu email na variável EMAIL da seguinte forma: "seuemail@gmail.com" (utilizando as aspas)

-> 5°: Crie uma senha de app na sua conta do google na parte de segurança e login (ou pesquise
por 'senhas de app' na barra de busca da sua conta do google).

-> 6°: Coloque a sua senha de app na variável SENHA do sistema da seguinte forma: "suasenhadeapp" (junto e utilizando as aspas)

-> 7°: Execute as demais células do sistema.

-> 8°: A celula de inserção de links só é obrigatória no primeiro acesso,
pois, os links serão salvos em um arquivo json.

                        Observações
-> O sistema pode não funcionar para alguns sites, pois, eles possuem
mecanismos que impedem o acesso de bots de automação.

-> A quantidade de requisição do sistema será definida de acordo com
o seu plano da Google Ia Studio.

                        Possiveis status do servidor

-> 503: Problemas de multiplas requisições no servidor

-> 429: Ira aparacer quando o limite de requisições a API do gemini for atingido (a quantidade irá variar de acordo com o seu plano na google ia studio).


                        Ferramentas Utilizadas
-> Python 3.12: Linguagem utilizada na criação do script que irá realizar requisições (aos sites e a API do Google IA Studio), 
comparar preços e enviar emails.

-> Google IA Studio: API que irá possibilitar a comunicação com a inteligência artificial que irá coletar
os preços do HTML retornado pela classe BeautifulSoup.


                        Arquivos do Sistema

monitor.ipynb: Script que contém todos os códigos e a lógica do sistema

produtos.json: Ira conter os links e as informações dos produtos inseridos pelo usuário.
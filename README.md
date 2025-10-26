Otimizando Processos: Automação de Cadastro de Produtos em Python

Este projeto demonstra como a automação pode otimizar tarefas repetitivas, como o cadastro de dados em um sistema web. Utilizando as bibliotecas pyautogui, pandas e time, o script automatiza o preenchimento de formulários a partir de uma planilha, economizando tempo e minimizando erros.

💻 Tecnologias Utilizadas
Python: Linguagem de programação principal.

pyautogui: Biblioteca para controle de mouse e teclado, simulando a interação humana.

pandas: Usada para importar e manipular dados de uma planilha (.csv).

time: Biblioteca para controlar o tempo de espera entre as ações, garantindo que o sistema tenha tempo para carregar as páginas.

⚙️ Como Funciona o Projeto
O script segue uma sequência lógica de passos:

Acesso ao Sistema: O pyautogui abre o navegador padrão, navega até a URL de login e insere as credenciais (e-mail e senha) para acessar o sistema.

Importação de Dados: O pandas lê um arquivo produtos.csv, convertendo os dados em uma tabela (DataFrame).

Automação do Cadastro: O script percorre cada linha da tabela. Para cada produto, ele:

Clica nos campos do formulário de cadastro.

Preenche cada campo com os dados correspondentes da tabela.

Lida com campos opcionais (OBS) de forma inteligente.

Clica no botão de "Enviar" para registrar o produto.

Rola a página para cima, preparando-se para o próximo cadastro.

🔧 Capturando Coordenadas da Tela
Para que a automação funcione em qualquer resolução de tela, é necessário obter as coordenadas exatas onde o mouse deve clicar. Para isso, usei um script simples que detecta a posição do cursor.

Execute o código abaixo, posicione o mouse sobre o local desejado na tela (campo de e-mail, botão, etc.) e a coordenada será impressa no terminal.

Python

import time
import pyautogui

time.sleep(5) # 5 segundos para você mover o cursor para a posição desejada
print(pyautogui.position())
🚀 Como Executar o Código
Clone este repositório.

Instale as bibliotecas necessárias:

Bash

pip install pyautogui pandas
Certifique-se de que o arquivo produtos.csv está no mesmo diretório do script.

Substitua as coordenadas do pyautogui.click() no código principal pelas coordenadas que você capturou.

Execute o script:

Bash

python nome_do_arquivo.py

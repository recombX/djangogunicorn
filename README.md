# Tutorial de como utilizar Gunicorn com Django
## Pré-Requisitos
1) Python 3 instalado no linux
2) Pip instaldo no Linux

### Verificando a versão do Python e do Pip

Para verificar a versão do Python digite o seguinte comando:

```
python --version

```
Para saber a versão do PIP digite o seguinte comando:
```
pip --version
``` 

## Instalando o Gunicorn

Para instalar o Gunicorn basta digitar o seguinte comando 

```
pip install gunicorn
```
Para verificar a versão instalada:

```
gunicorn --version
```
Para mais detalhes veja a referência **1** e **2**.

## Django e Gunicorn

Para rodar o django utilizando o Gunicorn basta executar o seguinte padrão de comando:

```bash
gunicorn <nome_projeto>.wsgi:application --bind 0.0.0.0:<porta>
```
1) **nome_projeto**: pasta do projeto do django que contem o wsgi.

2) **porta**: porta que deseja disponibilizar para a aplicação.

### Exemplo de uso

Para exemplificar o uso, criamos uma aplicação django de teste simples. Basicamente, a aplicação apresenta a página inicial do django.

Primeiro clone o projeto para o seu computador.

```bash
git clone https://github.com/recombX/djangogunicorn.git
```

Depois, para instalar as dependências da aplicação, execute o comando abaixo dentro da pasta que contem o arquivo **requirements.txt**:

```bash
pip install -r requirements.txt
```

Esse comando instala todas as bibliotecas necessárias para rodar a aplicação django, inclusive o gunicorn. 

Após a conclusão da instalação das dependência rode o seguinte comando no terminal para executar a aplicação.

```
gunicorn projeto_teste.wsgi:application --bind 0.0.0.0:8000
```
ou execute o run-linux.sh

```bash
./run-linux.sh
```

Após executar o comando abra o seu browser de preferência e digite: localhost:8000. A página do Django deve ser apresentada. Para mais referências entre Django e Gunicorn veja a referência **3**.

## Referências:
1) [Documentação de instalação do Gunicorn](https://docs.gunicorn.org/en/stable/install.html)
2) [Documentação oficial do Gunicorn](https://gunicorn.org/)
3) [Como usar o Gunicron e Django](https://docs.djangoproject.com/en/3.2/howto/deployment/wsgi/gunicorn/)

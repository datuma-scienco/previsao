# Dashboard de Previsão Macroeconomica

## Poetry

1. Instale o gerenciador de dependências Poetry com o comando `curl -sSL https://install.python-poetry.org | python3 -`

2. Localize o arquivo `pyproject.toml` no material desta aula, clique sobre o mesmo e arraste para o painel Explorer do VS Code online
3. No Terminal, execute o comando `poetry lock`
4. No Terminal, execute o comando `poetry self add poetry-plugin-export`
5. No Terminal, execute o comando `poetry export -f requirements.txt --output requirements.txt --without-hashes`
6. Abrir o arquivo `requirements.txt` criado e editar o mesmo de forma a manter somente dependências necessárias para a dashboard, tal como abaixo:

```txt
fastparquet==2024.5.0
mizani==0.11.4
pandas==2.2.2
plotnine==0.13.6
pyarrow==17.0.0
shiny==1.0.0
shinyswatch==0.7.0
faicons==0.2.2
numpy==2.1.0
skforecast==0.13.0
statsmodels==0.14.2
scikit-learn==1.5.1
openpyxl==3.1.5
jinja2==3.1.2
```
7. Instalar `poetry self add poetry-plugin-shell`

8. Abrir o virtual env do poetry com o comando `poetry shell`

## Variáveis de ambiente

- É preciso setar uma variável de ambiente com a API KEY do GEMINI dentro do prompt do python ou ipython

`os.environ["GEMINI_API_KEY"] = "COLE AQUI A SUA CHAVE"`

[Gerar API do GEMINI](https://aistudio.google.com/app/u/0/apikey)

## Para executar o shiny

`python -m shiny run --reload app.py`

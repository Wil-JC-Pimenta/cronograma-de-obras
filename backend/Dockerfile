# Use uma imagem base do Python
FROM python:3.9-slim

# Defina o diretório de trabalho
WORKDIR /app

# Copie o arquivo de dependências
COPY requirements.txt .

# Instale as dependências e atualize o pip
RUN pip install --upgrade pip && pip install -r requirements.txt

# Copie o restante do código da aplicação para o container
COPY . .

# Exponha a porta que o backend vai rodar
EXPOSE 8000

# Defina o comando para rodar o backend
CMD ["uvicorn", "app.main:app", "--host", "0.0.0.0", "--port", "8000"]

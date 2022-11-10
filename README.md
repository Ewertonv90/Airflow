# Airflow
Configuração de conexão do airflow no docker no windows


Dentro do VSCODE e da pasta escolhida  executar o comando "docker-compose up airflow-init" e depois ""docker-compose up".


# configurando com python 

- Criar ambiente virtual do python

mkdir datapipeline
cd datapipeline
python3 -m venv .env
source .env/bin/activate

- Criar variavel de ambiente para onde o Airflow vai ser instalado

export AIRFLOW_HOME=$(pwd)/airflow

# Bixar o Airflow 

pip install apache-airflow==1.16.10-constraint "https://raw.githubusercontent.com/apache/airflow/constraints-1.10.14/constraints-3.7.txt"

 Alterar versão conforme necessario
 
 # iniciar o banco de dados da ferramenta( SQL lite)
 
 airflow initdb
 
 # Iniciar o Scheduler
 
 airflow scheduler
 
 # Iniciar o Airflow 
 
 airflow webserver

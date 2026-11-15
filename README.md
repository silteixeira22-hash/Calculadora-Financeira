📊 Calculadora Financeira de Aluguéis por Temporada

Este projeto consiste em uma análise e manipulação de dados utilizando a biblioteca Pandas em Python. O objetivo principal é estruturar dados de locação temporária para calcular métricas financeiras cruciais de desempenho, auxiliando na precificação e na estimativa de faturamento de propriedades.

📝 Contexto do Projeto
Na gestão de aluguéis de temporada, taxas adicionais (como taxa de limpeza) podem distorcer a percepção real de valor por parte dos hóspedes. Para otimizar a clareza financeira, este projeto realiza:

O cálculo do Custo Real por Noite consolidando a tarifa base e as taxas obrigatórias.
A projeção do Faturamento Mensal obtido por cada imóvel com base em sua ocupação recente.
🚀 Funcionalidades da Calculadora
Cálculo do Custo Total da Diária (Custo_Total_Noite): Soma o preço da diária base (Preco_Noite_BRL) com a taxa de limpeza (Taxa_Limpeza_BRL).
Projeção de Faturamento (Faturamento_Ultimo_Mes): Multiplica o custo real consolidado da diária pela quantidade de noites reservadas no último mês (Noites_Reservadas_Ultimo_Mes).
🛠️ Tecnologias Utilizadas
Python 3.x
Pandas (para manipulação e análise de dados)
Google Colab (ambiente de desenvolvimento)
📂 Estrutura dos Dados Analisados
O dataset alugueis_temporada.csv contém informações detalhadas das propriedades, incluindo:

ID_Imovel: Identificador único do imóvel
Tipo_Propriedade: Apartamento, Casa, Studio, Cobertura, etc.
Cidade / Bairro: Localização do imóvel
Preco_Noite_BRL: Preço base da diária
Taxa_Limpeza_BRL: Taxa de higienização cobrada por estadia
Noites_Reservadas_Ultimo_Mes: Taxa de ocupação recente
💻 Como Executar o Projeto
Clone este repositório:
git clone https://github.com/seu-usuario/calculadora-aluguel-temporada.git
Certifique-se de possuir o arquivo alugueis_temporada.csv no diretório de execução.
Instale o Pandas caso não tenha:
pip install pandas
Execute o notebook ou script contendo as etapas de cálculo:
import pandas as pd

# Carregar dados
df = pd.read_csv("alugueis_temporada.csv")

# Executar cálculos
df["Custo_Total_Noite"] = df["Preco_Noite_BRL"] + df["Taxa_Limpeza_BRL"]
df["Faturamento_Ultimo_Mes"] = df["Custo_Total_Noite"] * df["Noites_Reservadas_Ultimo_Mes"]
Desenvolvido com 💻 e ☕ por Silvana Teixeira.

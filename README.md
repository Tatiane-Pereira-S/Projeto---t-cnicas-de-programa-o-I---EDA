# Análise do Uso de Redes Sociais e Impacto na Produtividade
## Introdução
Nos últimos anos, as redes sociais se tornaram parte essencial da vida cotidiana. Este projeto visa explorar o tempo médio gasto em diferentes plataformas de redes sociais por usuários de várias faixas etárias e profissões, em países como Brasil, Estados Unidos e Índia. Nosso objetivo é identificar padrões de comportamento e entender como o tempo gasto nessas plataformas pode afetar a produtividade e o bem-estar dos usuários.

# Objetivo
## O objetivo desta análise é fornecer insights sobre:

O impacto do uso de redes sociais na produtividade.
As plataformas mais populares por grupo demográfico.
Correlações entre tempo gasto nas redes e satisfação pessoal, idade, profissão, etc.
Estrutura do Projeto
Leitura e Limpeza dos Dados: O arquivo Time-Wasters on Social Media.csv contém informações detalhadas sobre o uso de redes sociais. Começamos a análise carregando os dados, verificando a existência de valores nulos, duplicados e corrigindo inconsistências (ex: corrigindo a grafia de "Barzil" para "Brazil").

## Análise Descritiva:

Distribuição de usuários por localização.
Análise da média de tempo gasto por plataforma.
Média de idade de usuários de cada plataforma por país.
Categorização do motivo para assistir a vídeos e seu impacto no tempo total gasto.
Visualizações Gráficas: Utilizamos gráficos para ilustrar as informações, como:

Tempo médio gasto nas plataformas por usuários de diferentes países.
Número de usuários por país.
Comparação de tempo gasto por razões como entretenimento e educação.
Bibliotecas Utilizadas
pandas: Manipulação e análise dos dados.
numpy: Operações numéricas avançadas.
matplotlib: Criação de gráficos e visualizações.
Como Utilizar
Pré-requisitos
Certifique-se de ter as bibliotecas necessárias instaladas:

bash
Copiar código
!pip install pandas numpy matplotlib
Execução
Carregue os dados a partir do arquivo CSV:
python
Copiar código
import pandas as pd
df_SocialMedia = pd.read_csv('Caminho_do_arquivo/Time-Wasters on Social Media.csv')
Realize a análise exploratória, verificando a integridade dos dados:
python
Copiar código
df_SocialMedia.info()
df_SocialMedia.isnull().sum()
Visualize os principais insights com gráficos:
python
Copiar código
import matplotlib.pyplot as plt

df_SocialMedia.groupby(['Platform'])['Total Time Spent'].mean().sort_values(ascending=False).plot(kind='bar', color=['blue', 'red', 'grey', 'purple'])
plt.title('Average Total Time Spent on Platform by User')
plt.ylabel('Average Time Spent')
plt.show()
Resultados Esperados
A partir das análises, esperamos obter uma visão clara de como os diferentes fatores (como idade, profissão e localização) influenciam o tempo gasto nas redes sociais. Além disso, os resultados podem ser usados para promover um uso mais equilibrado das plataformas e aumentar a produtividade pessoal e profissional.

Conclusão
Este projeto oferece uma perspectiva valiosa sobre o impacto das redes sociais na vida moderna. As descobertas podem ajudar indivíduos e empresas a gerenciar melhor o tempo gasto nas plataformas digitais.


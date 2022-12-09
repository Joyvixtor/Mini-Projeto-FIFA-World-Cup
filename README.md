# Mini-Projeto FIFA World Cup
Mini-projeto criado para trabalhar em cima dos dados fornecidos pela FIFA das equipes que jogaram o mundial de 2006, 2010, 2014 e 2018.

## Instruções de uso
Para upar os quatro arquivos CSV dentro do arquivo .ipynb, rode o trecho o seguinte trecho do código:

```
from google.colab import files
uploaded = files.upload()
```
E selecione a opção "Escolher arquivos" que irá aparecer logo em seguida. Ao abrir no seu diretório local, selecione os quatro arquivos CSV que foram fornecidos neste repositório.

##Bibliotecas escolhidas
```
import panda as pd
```
A Biblioteca *panda* foi escolhida para ajudar no tratamento dos dados dos quatro arquivos CSV do mini-projeto. Ela apresenta uma gama de funcionalidades que se mostraram úteis no desenvolvimento das especificações.
```
import io
```
Biblioteca simples usada apenas para o tratamento de parâmetros de entrada do mini-projeto. 
```
import matplotlib.pyplot as plt
```
Apesar de a biblioteca *panda* já apresentar algumas funcionalidades que permitem a plotagem de gráficos no código, a utilização da *matplotlib* se deu por ser uma biblioeteca criada especialmente para a criação gráfica e para o tratamento de dados matemáticos contidos nestas funções.

##Tratamento de Dados
Através da biblioteca *panda*, os arquivos importados manualmente pelo usuário foram tratados pela função ".read_csv". Através dos parâmetros *nrows* e *usecols*, foram selecionadas as colunas especificadas no mini-projeto (Goals For e Goals Against) e o número de linhas limites da tabela (os 15 primeiros colocados).
Dei preferência pela utilização de um loop for para perspassar pelos 4 arquivos CSV e coletar os dados Goals For e Goals Against. Estes dados foram coletados e concatenados em duas listas que representam as listas de valores de interesse do mini-projeto.

##Análise Estatística
As duas listas foram transformadas em Dataframes para que as funções .std() e .mean() da biblioteca *panda* pudesse funcionar. São duas funções simples que coletam o desvio padrão e a média, respectivamente.
Para o limite superior e o limite inferior, duas funções foram codadas por mim para realizar o cálculo simples que é informado no mini-projeto.

##Plotagem de Gráficos
Como foi dito anteriormente, foi preferível a utilização da biblioteca *matplotlib* para a plotagem dos gráficos. Utilizando .axhline, criei as linhas horizontais de limite superior e inferior. Por fim, uso plt.plot para plotar os dados coletados nas listas de variáveis. 

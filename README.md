## Código da Dissertação – UFSCar

Este repositório reúne os códigos desenvolvidos e utilizados ao longo do processo de pesquisa da dissertação de mestrado, incluindo versões exploratórias, testes intermediários e a implementação final utilizada para a obtenção e validação dos resultados apresentados no trabalho.

Observações:
-
- IA_2: Primeiro teste em Python para um banco de dados.
- O Código (2): Aplicação de rede neural e geração de um gráfico 3D em função de camada/neurônio.
- Testes: Contém todos os testes realizados para alcançar o resultado desejado, incluindo todas as falhas durante o processo, nas metricas MSRE e MAPE.
- Yuri (1): Base do código.
- Final: Código final onde a regressão foi usada nos dados de 2022 para validação, sem a criação de rede neural, utilizando apenas a regressão para permitir uma árvore de decisões.

Os códigos fornecem a regressão não linear por mínimos quadrados da função de emissão de CO₂ das usinas termelétricas do Brasil.

## Nota sobre reaproveitamento de base de código

A estrutura inicial de leitura e organização dos dados teve como referência uma base de código previamente desenvolvida por Giovanni Aurelio Grizante, no contexto de um projeto de iniciação científica.
Essa base foi legitimamente reaproveitada como ponto de partida, sendo posteriormente substancialmente modificada, expandida e reestruturada para atender aos objetivos específicos desta dissertação, incluindo:

definição do modelo matemático adotado;
construção da metodologia de validação;
implementação das métricas de erro;
separação temporal dos conjuntos de dados;
análise comparativa entre valores estimados e reais.

A concepção metodológica, a modelagem, a validação e os resultados finais apresentados são de autoria do autor da dissertação. sendo o reaproveitamento da base inicial devidamente citado e restrito à estrutura de organização de dados.

## Mecanismo de Funcionamento do Código: 
   - Coleta de dados de geração elétrica da ONS e IEMA.
   - Concatenação dos dados, separando apenas as usinas termelétricas, dos anos de 2020 a 2023.
   - Geração da regressão não linear por mínimos quadrados da função de emissão de CO₂.
   - Obtenção dos coeficientes da função de emissão de CO₂ das usinas termelétricas.
   - Realização das métricas MSE, MSRE, MAPE para estimar os erros relativos.
   - Geração de gráficos da geração e emissão de CO₂, com base nos resultados dos coeficientes.
   - Criação e treinamento de uma rede neural.
   - Cálculo dos erros e geração de um gráfico 3D em função da rede neural.
   - Validação da regressão com os dados de 2020 e 2021, utilizada para calcular a emissão nos dados de 2022, comparando o resultado calculado com o real e o erro relativo.

## Processos para Replicação em Trabalhos Futuros:
- Baixar os dados da ONS e IEMA e alterar os diretorios de acesso a esses dados;
- Realizar a instalação correta do solver Ipopt;
- Tomar o cuidado de se ter a intersecção entre os dados, é necessario que se for considerado 3 anos ou 4 anos, as pastas devem refletir essa igualdade, pois, caso contrário, não havera concatenação de dados.

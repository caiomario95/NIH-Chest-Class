# NIH Chest X-ray Disease Classification

Este projeto é uma implementação de um modelo de aprendizado profundo para a classificação de doenças em imagens de raios-X de tórax. Utilizamos um modelo de rede neural convolucional (CNN) para identificar condições como Pneumonia, Pneumotórax, Efusão, Infiltração, entre outras, a partir de imagens médicas.

## Dataset

O dataset utilizado neste projeto é o **NIH Chest X-rays**, que é uma coleção pública de imagens de raios-X de tórax disponibilizada pelo National Institutes of Health (NIH). Este dataset contém mais de 100.000 imagens de raios-X de tórax de mais de 30.000 pacientes, com rótulos para 14 condições diferentes:
- Atelectasia
- Cardiomegalia
- Efusão
- Infiltração
- Massa
- Nódulo
- Pneumonia
- Pneumotórax
- Consolidação
- Edema
- Enfisema
- Fibrose
- Espessamento Pleural
- Hérnia

### Onde Conseguir o Dataset

O dataset NIH Chest X-rays pode ser baixado diretamente do site oficial do NIH. Você pode acessar o dataset através do seguinte link:

- [NIH Chest X-rays Dataset](https://nihcc.app.box.com/v/ChestXray-NIHCC)

## Estrutura do Projeto

- `cnn_model.ipynb`: Notebook Jupyter contendo o código para carregar, pré-processar e treinar o modelo de CNN.
- `data/`: Diretório onde as imagens de raios-X e os arquivos CSV de metadados são armazenados.
- `requirements.txt`: Lista de dependências necessárias para executar o projeto.

## Requisitos

Para executar este projeto, você precisará das bibliotecas Python listadas no arquivo `requirements.txt`. As principais bibliotecas incluem:

- `torch` e `torchvision` para construção e treinamento do modelo
- `pandas` e `numpy` para manipulação de dados
- `scikit-learn` e `imbalanced-learn` para pré-processamento e avaliação
- `PIL` e `opencv-python` para processamento de imagens
- `matplotlib` e `seaborn` para visualização
- `scikit-fuzzy` para técnicas de lógica fuzzy
- `tqdm` para barras de progresso
- `jupyter` e `notebook` para execução do notebook

Você pode instalar todas as dependências usando o seguinte comando:
```bash
pip install -r requirements.txt
```

## Sobre o Projeto

Este projeto foi desenvolvido com o objetivo de criar um modelo de aprendizado profundo capaz de classificar doenças em imagens de raios-X de tórax. Utilizamos técnicas avançadas de processamento de imagens e aprendizado de máquina para treinar um modelo de rede neural convolucional (CNN) que pode identificar várias condições médicas a partir das imagens. Pretense-se adicionar outras tecnicas de classificação ao projeto.

### Carregamento e Preparação dos Dados

O dataset NIH Chest X-rays é carregado e pré-processado para garantir que as imagens estejam no formato adequado para o treinamento do modelo. Isso inclui a remoção de entradas duplicadas, balanceamento das classes e aplicação de técnicas de oversampling como o BorderlineSMOTE para lidar com o desbalanceamento das classes.

### Arquitetura do Modelo

A arquitetura do modelo é baseada na rede neural convolucional MobileNetV3, que é conhecida por sua eficiência e precisão em tarefas de classificação de imagens. A rede foi adaptada para o nosso problema específico, com camadas adicionais de dropout e fully connected para melhorar a generalização e a capacidade de aprendizado.

### Treinamento e Avaliação

O modelo é treinado utilizando o PyTorch, com técnicas de ajuste de taxa de aprendizado baseadas em lógica fuzzy para melhorar a convergência durante o treinamento. O desempenho do modelo é avaliado utilizando métricas como a acurácia, a perda de validação e a matriz de confusão.

### Resultados

Os resultados do modelo são salvos e analisados para garantir que ele esteja performando bem nas diferentes classes de doenças. O melhor modelo é salvo e carregado para a avaliação final, garantindo que ele possa ser utilizado para a classificação de novas imagens de raios-X de tórax.

### Conclusão

Este projeto demonstra a aplicação de técnicas avançadas de aprendizado profundo e processamento de imagens para a classificação de doenças em imagens médicas. A utilização de um dataset público como o NIH Chest X-rays permite que outros pesquisadores e desenvolvedores repliquem e aprimorem este trabalho, contribuindo para o avanço da área de diagnóstico assistido por computador.


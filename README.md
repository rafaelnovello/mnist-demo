# Aplicativo de identificação de digitos escritos manualmente. MNIST.

## [Demo Online](https://flask-mnist.herokuapp.com/)

## Instalação

Clone o repositório ou baixe o pacote zip.

Instale os pacotes necessários:

```bash
$ pip install -r requirements.txt
```

## Treinar o modelo

O aplicativo web depende do modelo treinado. Este processo acontece no arquivo TFLearn_Digit_Recognition.ipynb. Basta executar todo o notebook para iniciar, treinar e salvar o modelo treinado como MNIST.tfl

## Executar o aplicativo web

Com as dependencias instaladas, execute os seguintes passos para rodar o web app:

```bash
$ export FLASK_APP=app.py
$ flask run
```
## Sobre o modelo

Esta rede neural foi construida e treinada com [TFLearn](http://tflearn.org/), uma API de alto nível para [Tensorflow](https://www.tensorflow.org/).

A arquitetura segue o modelo mais simples de rede neural, chamado de [feedforward](https://en.wikipedia.org/wiki/Feedforward_neural_network), e esta organizada da seguinte forma:

- 2 camadas ocultas 'fully connected' com 300 e 100 neurônios respectivamente e função de ativação [ReLU](https://en.wikipedia.org/wiki/Rectifier_(neural_networks))
- 1 camada de saída 'fully connected' com 10 neurônios (um para cada opção de 0 a 9) e função de ativação [softmax](https://en.wikipedia.org/wiki/Softmax_function).

Redes neurais convolucionais performam melhor na classificação de imagens, mas este é um bom exemplo de aplicação do modelo mais simples, feedforward.

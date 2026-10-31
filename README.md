# Flappy Bird com IA – NEAT

Uma implementação do Flappy Bird baseada em IA, utilizando **NeuroEvolution of Augmenting Topologies (NEAT)** e Python. O projeto explora a neuroevolução ao treinar redes neurais para jogar o jogo de forma autônoma ao longo de gerações sucessivas.

## Sobre o projeto

Este projeto foi desenvolvido como um experimento prático para explorar conceitos de Inteligência Artificial e Aprendizado de Máquina, particularmente a neuroevolução.

Em vez de controlar manualmente o pássaro, cada um deles é controlado por uma rede neural independente. As redes recebem informações sobre a posição do pássaro e os obstáculos à frente e, então, decidem se o pássaro deve pular.

Por meio de um processo evolutivo, as redes com melhor desempenho são selecionadas e evoluem ao longo das gerações, melhorando progressivamente sua capacidade de jogar o jogo.

## Tecnologias

- **Python** – Linguagem de programação principal.
- **Pygame** – Desenvolvimento de jogos, renderização, animações e detecção de colisões.
- **NEAT-Python** – Implementação da NeuroEvolution of Augmenting Topologies.

## Como funciona

O projeto utiliza o NEAT para evoluir redes neurais sem a necessidade de um conjunto de dados de treinamento predefinido.

### Entradas da rede neural

Cada rede neural recebe três valores de entrada:

| Entrada | Descrição |
|---|---|
| Posição Y do pássaro | Posição vertical atual do pássaro. |
| Distância até o topo do tubo | Distância vertical entre o pássaro e o limite superior do tubo. |
| Distância até o fundo do tubo | Distância vertical entre o pássaro e o limite inferior do tubo. |

### Saída da Rede Neural

A rede produz uma saída que determina se o pássaro deve pular:

- **Saída > 0,5:** O pássaro pula.
- **Saída ≤ 0,5:** O pássaro continua seu movimento atual.

### Evolução e Aptidão

Cada pássaro representa um indivíduo controlado por sua própria rede neural.

A função de aptidão avalia o desempenho de cada indivíduo:

- Sobreviver aumenta a aptidão ao longo do tempo.
- Passar pelos tubos proporciona aptidão adicional.
- Colidir com obstáculos reduz a aptidão.

O NEAT usa esses valores de aptidão para fazer a população evoluir, ajustando os pesos, as conexões e a topologia da rede ao longo das gerações.

## Estrutura do projeto

```text
.
├── imgs/
│   ├── bird1.png
│   ├── bird2.png
│   ├── bird3.png
│   ├── pipe.png
│   ├── base.png
│   └── bg.png
├── config.txt
├── main.py
└── README.md
```

## Introdução

### Pré-requisitos

- Python 3.x
- pip

### Instalação

1. Clone o repositório:

```bash
git clone <url-do-repositório>
cd <pasta-do-repositório>
```

2. Instale as dependências:

```bash
pip install pygame neat-python
```

3. Execute o projeto:

```bash
python main.py
```

A simulação será iniciada automaticamente, exibindo a população de pássaros à medida que as redes neurais aprendem a jogar o jogo.

## Objetivos de aprendizagem

Este projeto foi uma oportunidade para explorar:

- Fundamentos de Inteligência Artificial e Aprendizado de Máquina.
- Redes neurais e tomada de decisão.
- NeuroEvolution of Augmenting Topologies (NEAT).
- Algoritmos genéticos e computação evolutiva.
- Funções de aptidão e avaliação da população.
- Integração de algoritmos de IA com um ambiente de jogo utilizando o Pygame.

## Considerações Finais

Desenvolvido como um projeto pessoal de aprendizagem voltado para a exploração da Inteligência Artificial e da neuroevolução utilizando Python.
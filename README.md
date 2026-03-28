# Jogo da Vida (Game of Life) em C

## Descrição do Projeto

Este projeto implementa o Jogo da Vida, um autômato celular proposto por John Conway, utilizando a linguagem C e o padrão arquitetural MVC (Model-View-Controller).

A aplicação simula a evolução de células em uma matriz bidimensional, onde cada célula pode estar viva ou morta, seguindo regras específicas a cada geração.

---

## Objetivo

Desenvolver uma simulação interativa do Jogo da Vida, permitindo ao usuário:

* Criar e remover células vivas
* Visualizar o estado do mundo
* Evoluir o sistema por gerações
* Salvar e recuperar configurações iniciais

---

## Conceitos Utilizados

* Estruturas de dados (listas encadeadas)
* Manipulação de matrizes
* Alocação dinâmica de memória
* Arquitetura MVC
* Leitura e escrita em arquivos
* Lógica de simulação (autômatos celulares)

---

## Estrutura do Projeto

O projeto está organizado em três camadas principais:

### Model (JVida_JJIB_Model)

Responsável pelos dados e estruturas:

* Matriz do mundo (vida)
* Listas encadeadas de células:

  * Vivas
  * Mortas (vizinhas)
  * Próxima geração

### View (JVida_JJIB_View)

Responsável pela interface com o usuário:

* Exibição da matriz
* Menu interativo
* Entrada de dados (coordenadas)
* Impressão de listas

### Controller (JVida_JJIB_Controller)

Responsável pela lógica do sistema:

* Controle do menu principal
* Regras de evolução das células
* Manipulação das listas
* Geração de novas gerações
* Salvamento e recuperação de estados

---

## Funcionalidades

### Manipulação do Mundo

* Definir dimensão da matriz (entre 10x10 e 60x60)
* Inicializar e limpar o mundo

### Controle de Células

* Inserir células vivas manualmente
* Remover células existentes
* Visualizar células vivas e mortas

### Evolução

* Calcular próxima geração com base nas regras:

  * Célula nasce com exatamente 3 vizinhos vivos
  * Sobrevive com 2 ou 3 vizinhos
  * Morre caso contrário

### Persistência

* Salvar estado inicial em arquivo (CONFIG_INIC)
* Recuperar estado salvo

---

## Regras do Jogo da Vida

Para cada célula:

* Morre se tiver menos de 2 vizinhos (solidão)
* Morre se tiver mais de 3 vizinhos (superpopulação)
* Sobrevive com 2 ou 3 vizinhos
* Nasce se uma célula morta tiver exatamente 3 vizinhos

---

## Como Executar

1. Compile os arquivos:

```bash
gcc Jvida_JJIB_Projeto.c JVida_JJIB_Controller.c JVida_JJIB_View.c -o jogo
```

2. Execute:

```bash
./jogo
```

3. Escolha a dimensão da matriz e utilize o menu interativo.

---

## Exemplo de Uso

* Definir dimensão: 20
* Inserir células: 3,4
* Visualizar mundo
* Iniciar simulação
* Observar evolução das gerações

---

## Autores

* Isabella Rubio Venancio
* Beatriz Lopes Rizzo
* Julia Gachido Schmidt
* João Pedro Figols Neco

---

## Considerações

Este projeto demonstra a aplicação prática de estruturas de dados e organização em camadas, além de simular um sistema dinâmico clássico da computação.

Ideal para estudos de:

* Algoritmos
* Simulação
* Estruturas dinâmicas
* Organização de software

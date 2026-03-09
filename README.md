# Sistema de Hierarquia de Veículos (POO em Python) 🚗✈️🛥️

## Visão Geral do Projeto
Este projeto é uma aplicação desenvolvida em Python que modela um ecossistema de veículos. O objetivo principal é demonstrar a aplicação prática dos conceitos fundamentais de Programação Orientada a Objetos (POO), estruturando diferentes meios de transporte de acordo com suas características e comportamentos. O projeto foi desenvolvido como um trabalho acadêmico para consolidar os pilares de design de software.

## Conceitos de POO Aplicados
* **Abstração:** O projeto utiliza o módulo `abc` nativo do Python para definir a classe base `Veiculo` como uma Classe Abstrata. Ela estabelece um contrato rigoroso no sistema, exigindo que todos os veículos concretos implementem obrigatoriamente os métodos `ligar()` e `mover()`.
* **Herança:** A arquitetura apresenta múltiplos níveis de herança para evitar repetição de código. A classe abstrata `Veiculo` serve de base para categorias genéricas (`Automovel`, `Motocicleta`, `Bicicleta`, `VeiculoAquatico` e `VeiculoAereo`). A partir daí, classes mais específicas herdam os atributos e comportamentos dessas categorias pai (ex: a classe `Carro` herda de `Automovel`, enquanto `Scooter` herda de `Motocicleta`).
* **Polimorfismo:** Cada classe de veículo específico implementa sua própria maneira de responder aos métodos definidos na classe base. A chamada do método é padronizada para todos os objetos, mas o comportamento varia: ao chamar o método `ligar()`, um `Carro` exibe "Ligando carro com chave ou botão", enquanto um `Aviao` exibe "Avião ligando turbinas".

## Estrutura de Classes
A hierarquia foi dividida da seguinte maneira:

- `Veiculo` *(Classe Abstrata)*
  - `Automovel` ➔ `Carro`, `Caminhao`, `Onibus`, `SUV`, `Conversivel`
  - `Motocicleta` ➔ `Scooter`, `Esportiva`, `Custom`, `Naked`, `Trail`
  - `Bicicleta` ➔ `Urbana`, `Montanha`, `Eletrica`, `Dobravavel`, `Speed`
  - `VeiculoAquatico` ➔ `Lancha`, `Iate`, `JetSki`, `Submarino`, `BarcoPesca`
  - `VeiculoAereo` ➔ `Aviao`, `Helicoptero`, `Drone`, `Planador`, `Balao`

## Demonstração (Execução)
O projeto conta com uma função `main()` que atua como um *driver code*. Ela instancia uma lista diversificada contendo vários tipos de veículos com suas respectivas marcas, modelos e anos. Em seguida, um laço de repetição itera sobre essa lista, acionando os métodos `exibir_info()`, `ligar()` e `mover()` para cada instância, comprovando o funcionamento do polimorfismo no terminal.

## Como Executar
Como este projeto foi originalmente desenvolvido em um Jupyter Notebook (Google Colab), você pode executá-lo das seguintes formas:

1. **Via Google Colab/Jupyter:** Basta abrir o arquivo `Projeto_Veiculo_python.ipynb` e rodar a célula contendo o código.
2. **Via Terminal (Python padrão):** Se você extraiu o código para um arquivo `.py` (ex: `veiculos.py`), execute no terminal:
   ```bash
   python veiculos.py# POO

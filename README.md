# IME-Def-Ciber-Kyber-Python

# Implementação do Kyber com AES em Python

## Visão Geral

Este projeto demonstra a **implementação do algoritmo de criptografia pós-quântica Kyber** em Python, utilizando **AES** para encapsulamento de chaves e criptografia de dados. A implementação foi feita unicamente para **validação de conceito**, com o objetivo de testar a viabilidade da integração do Kyber em cenários de criptografia pós-quântica.

O Kyber é um dos candidatos do processo de padronização de criptografia pós-quântica do NIST, e este repositório contém exemplos práticos que utilizam as variantes **Kyber-512**, **Kyber-768**, e **Kyber-1024** para criptografia e decapsulamento.

## Estrutura do Projeto

O projeto contém scripts e notebooks que realizam as seguintes operações:
- **Encapsulamento de chave pública** utilizando o Kyber.
- **Criptografia de dados** usando AES com a chave de sessão gerada pelo encapsulamento.
- **Desencapsulamento e descriptografia** da mensagem, usando a chave privada do Kyber.

## Requisitos

Para rodar a implementação, certifique-se de instalar as dependências:

```bash
pip install pycryptodome numpy cryptography psutil memory-profiler
```

## Scripts Disponíveis

1. **Testes Automáticos**: Scripts que validam a implementação do Kyber por meio de benchmarks automatizados. Esses testes verificam o desempenho das operações de encapsulamento e desencapsulamento para garantir a robustez da implementação.
   
   - Scripts disponíveis:
     - `test_ccakem.py`
     - `test_cpake.py`
     - `test_indcpa.py`
     - `test_ntt.py`
     - `test_prf.py`
     - `test_util.py`

2. **Encapsulamento e Desencapsulamento com AES**: Implementa o processo de encapsulamento usando Kyber e criptografia de dados com AES. O processo de teste foi realizado com **Kyber-512**, **Kyber-768**, e **Kyber-1024**, e os resultados são exibidos em termos de tempo de execução, consumo de CPU e uso de memória.

## Resultados dos Testes

### Testes Automáticos

Os benchmarks automáticos mediram o tempo de execução, uso de CPU e memória durante os testes com 100 execuções de cada variante do Kyber. Os resultados mostraram que:

- O tempo médio de execução variou entre 0.18 e 0.20 segundos.
- A memória média utilizada foi de **0.00 MiB**, com um pico de **0.03 MiB**.
- O uso máximo de CPU foi de **1.25%**.

### Teste de Performance com Criptografia AES

Os testes de encapsulamento e criptografia com **AES** mostraram o seguinte desempenho:

- **Kyber-512**: 
  - Tempo total: 4.5973 segundos
  - Consumo máximo de CPU: 36.6250%
  - Consumo máximo de memória: 0.0703 MiB

- **Kyber-768**: 
  - Tempo total: 7.2055 segundos
  - Consumo máximo de CPU: 24.4125%
  - Consumo máximo de memória: 0.0117 MiB

- **Kyber-1024**: 
  - Tempo total: 10.2172 segundos
  - Consumo máximo de CPU: 18.9000%
  - Consumo máximo de memória: 0.0156 MiB

### Teste de Estresse

O teste de estresse foi realizado com 100 encapsulamentos consecutivos para cada variante do Kyber, confirmando a eficiência do algoritmo:

- **Kyber-512**: 3.9417 segundos, uso máximo de CPU: 26.0375%
- **Kyber-768**: 6.2780 segundos, uso máximo de CPU: 26.0375%
- **Kyber-1024**: 9.1690 segundos, uso máximo de CPU: 18.9000%

## Validação de Conceito

Esta implementação foi desenvolvida exclusivamente para **validação de conceito**, demonstrando a viabilidade técnica de integrar o **Kyber** em sistemas reais. Os testes realizados mostram que o Kyber é eficiente e seguro para ambientes com recursos limitados, como dispositivos **IoT** e **sistemas embarcados**.

## Conclusão

O Kyber se mostrou uma opção robusta para criptografia pós-quântica, oferecendo **baixo consumo de recursos** e **alta segurança**. A integração com AES adiciona uma camada de criptografia simétrica eficiente, garantindo a proteção dos dados. Esta implementação serve como um exemplo prático para futuras integrações do Kyber em sistemas pós-quânticos.

---

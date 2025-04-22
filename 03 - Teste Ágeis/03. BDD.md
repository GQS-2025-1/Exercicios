🍔 **Exercício de Testes Ágeis com Cucumber - Sistema de Hamburgueria**

🎯 **Objetivo**

Este exercício tem como objetivo aplicar os conceitos de BDD (Behavior-Driven Development) utilizando Gherkin, Cucumber e Java para automatizar testes de um sistema de pedidos de uma hamburgueria.

Você irá:

- Criar cenários em linguagem Gherkin.

- Implementar os passos em Java.

- Executar os testes.

📚 Contexto
A hamburgueria **🐷 Peppa Lanches** desenvolveu um sistema de pedidos que permite que clientes solicitem hambúrgueres informando o nome do item. O sistema verifica se o hambúrguer existe no cardápio e responde se o pedido pode ou não ser realizado.

🧪 Regras de Negócio
- Um hambúrguer só pode ser pedido se ele estiver disponível no cardápio.

- Se o hambúrguer não existir, o sistema deve avisar que o item está indisponível.

📂 Estrutura Esperada do Projeto
```bash
src/
├── main/java/com/hamburgueria/Pedido.java
├── test/java/steps/PedidoSteps.java
├── test/java/runner/HamburgueriaRun.java
└── test/resources/pedido.feature
```
✅ **Funcionalidade (Gherkin)**

- pedido.feature
```gherkin
# language: pt

Funcionalidade: Pedido de hambúrguer

  Cenário: Cliente faz um pedido válido
    Dado que o cardápio está carregado
    Quando o cliente pedir o hambúrguer "Cheddar Bacon"
    Então o sistema deve confirmar o pedido de "Cheddar Bacon"

  Cenário: Cliente pede um hambúrguer que não existe
    Dado que o cardápio está carregado
    Quando o cliente pedir o hambúrguer "X-Monstro"
    Então o sistema deve informar que o hambúrguer não está disponível
```

📦 **Comportamento Esperado**

| Entrada do Cliente	| Resultado Esperado                  |
| --------------------- | ----------------------------------- |
| Cheddar Bacon	        | Pedido confirmado                   |
| X-Monstro	            | Item não está disponível no cardápio|
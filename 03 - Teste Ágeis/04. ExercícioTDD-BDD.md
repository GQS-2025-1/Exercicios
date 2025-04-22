# 🚗 Exercício: Reserva de Carro por Aplicativo (TDD + BDD)

## 🎯 Objetivo

Desenvolver uma funcionalidade de **reserva de carro** em um aplicativo de mobilidade, utilizando **TDD** e **BDD com Gherkin + Cucumber**.

---

## 📝 História de Usuário

**Como** passageiro de um aplicativo de transporte,  
**Quero** reservar um carro informando meu local,  
**Para** que eu possa me deslocar com comodidade e segurança.

---

## ✅ Funcionalidades Esperadas

- Validar se a localização informada está dentro da **área de cobertura** do serviço.
- Confirmar a reserva e retornar uma **mensagem adequada**.
- Testar a lógica com **TDD**.
- Validar o comportamento com **BDD (Gherkin + Cucumber)**.

---

## 🔧 Estrutura esperada

```bash
reserva_carro/
├── pom.xml
├── src/
│   ├── main/
│   │   └── java/
│   │       └── reserva/
│   │           └── ReservaService.java
│   └── test/
│       ├── java/
│       │   └── runner/
│       │       └── ReservaServiceTest.java   
│       │       └── ReservaRun.java   
│       │   └── steps/
│       │       └── ReservaSteps.java          
│       └── resources/
│           └── features/
│               └── reserva.feature                   
```

## 🔁 Etapas do Desenvolvimento

### 1. 📌 TDD

- Implemente a classe `ReservaService` com um método `reservar(String cidade, String endereco)` que retorna uma mensagem com base na cidade.

Regras:
- Se a cidade for `"Belo Horizonte"` ou `"Contagem"` → reservar e retornar `"Motorista a caminho"`.
- Caso contrário → retornar `"Área fora de cobertura"`.

### 2. 🧾 BDD com Cucumber + Gherkin

- Crie o arquivo **reserva.feature** com os seguintes cenários:

    - Cenário 1: Reserva dentro da área de cobertura
    - Cenário 2: Reserva fora da área de cobertura

- Implemente os steps em `ReservaSteps.java`.

- Implemente as classes de teste `ReservaServiceTest.java` e `ReservaRun.java`.
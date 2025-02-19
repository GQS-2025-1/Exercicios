# 🏢 Exercício: Controle de Funcionários

## 📌 Descrição
Crie um sistema de gerenciamento de funcionários. Cada funcionário deve ter:
- **Nome** (String)
- **ID** (int)
- **Salário** (double)

Os funcionários devem ser armazenados em um `HashMap<Integer, Funcionario>`, onde a chave é o ID do funcionário.

### 🎯 Funcionalidades do sistema:
1. **Adicionar funcionários**
2. **Remover funcionários pelo ID**
3. **Exibir todos os funcionários cadastrados**

---

📂 Arquivos esperados:
- `Funcionario.java` (classe representando um funcionário)
- `GerenciadorFuncionarios.java` (classe contendo as funcionalidades)

---
📌 **Dicas**:
- Utilize `Scanner` para entrada de dados.
- Teste seu código criando uma interface simples no console.

## 📌 Exemplo de Uso (Java)
```java
GerenciadorFuncionarios gerenciador = new GerenciadorFuncionarios();

gerenciador.adicionarFuncionario(101, "Ana Souza", 5000.00);
gerenciador.adicionarFuncionario(102, "Carlos Silva", 4800.00);

gerenciador.exibirFuncionarios();
gerenciador.removerFuncionario(101);

# 🛡️ Projeto SistemaRobusto

Este projeto é uma aplicação de console em **C# utilizando .NET** que simula um **sistema de cadastro resistente a erros de entrada do usuário**.

O objetivo da atividade foi aplicar a **5ª Heurística de Nielsen: Prevenção de Erros**, garantindo que o sistema não "quebre" ao receber dados inválidos, mas sim responda com mensagens claras e amigáveis.

---

## 🛠️ Comandos Utilizados

* `dotnet new console -n SistemaRobusto`
  Cria a estrutura inicial do projeto.

* `dotnet build`
  Compila o projeto.

* `dotnet run`
  Executa o programa no terminal.

---

## 📦 Estrutura do Projeto

Arquivos principais:

1. `Program.cs`
   Contém a lógica do sistema, incluindo o tratamento de erros com `try-catch`.

2. `SistemaRobusto.csproj`
   Arquivo de configuração do projeto.

Arquivos adicionais:

* `minha-evidencia-1.png` → Execução com sucesso (entrada válida)
* `minha-evidencia-2.png` → Execução com erro tratado (entrada inválida)

Framework utilizado:

* `.NET`

---

## ⚙️ Funcionamento do Programa

O sistema solicita ao usuário que digite sua idade.

Durante a execução:

* Se o usuário digitar um número válido:

  * O sistema converte o valor
  * Exibe mensagem de sucesso em verde

* Se o usuário digitar um valor inválido (letras ou texto):

  * O sistema captura o erro
  * Exibe uma mensagem amigável em vermelho
  * Orienta o usuário a corrigir a entrada

O programa utiliza o bloco:

```
try → tenta executar
catch → trata o erro
finally → finaliza a execução
```

Isso evita que o sistema seja encerrado de forma abrupta.

---

## 🧠 O que é Try-Catch?

O `try-catch` é uma estrutura usada para **capturar e tratar erros em tempo de execução**.

* `try`: contém o código que pode gerar erro
* `catch`: captura o erro e permite tratá-lo
* `finally`: executa sempre, independente do resultado

No projeto, ele é usado para evitar que o programa feche caso o usuário digite um valor inválido.

---

## 🧠 Heurística de UX Aplicada

**5ª Heurística de Nielsen — Prevenção de Erros**

O sistema foi projetado para evitar falhas críticas causadas por erros simples do usuário (como digitar letras em vez de números).

Em vez de exibir uma mensagem técnica confusa ou encerrar o programa, ele:

* Informa claramente o problema
* Orienta como corrigir
* Mantém o sistema funcionando

Isso melhora significativamente a experiência do usuário.

---

## 📸 Evidência de Execução

### ✅ Caminho Feliz (Entrada válida)

![Execução com sucesso](./minha-evidencia-1.png)

### ❌ Caminho do Erro (Entrada inválida)

![Execução com erro](./minha-evidencia-2.png)

---

## 💭 Reflexão (IHC)

Quando o programa simplesmente "crasha" ao receber uma entrada inválida, o sentimento do usuário geralmente é de **frustração, insegurança e falta de confiança no sistema**.

Isso acontece porque o usuário não entende o que deu errado e não sabe como corrigir o problema.

Já quando o sistema utiliza tratamento de erros com mensagens amigáveis:

* O erro é explicado de forma clara
* O usuário recebe orientação sobre como corrigir
* O sistema continua funcionando normalmente

Isso aumenta a **confiança**, pois o usuário percebe que o software é robusto, confiável e preparado para lidar com falhas humanas.

---

## 🚀 Insight Extra (Nível Profissional)

Embora o `try-catch` seja eficiente, em cenários de validação de entrada, uma abordagem mais moderna é utilizar:

```
int.TryParse()
```

Ele evita exceções e retorna apenas `true` ou `false`, tornando o código mais limpo e performático.

---

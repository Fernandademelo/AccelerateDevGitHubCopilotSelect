# Library App

## Descrição
Library App é uma aplicação de console para gerenciar um sistema de biblioteca. Ela permite que os usuários pesquisem patronos, visualizem detalhes dos patronos e gerenciem empréstimos de livros.

A aplicação é construída usando .NET 8 e segue uma arquitetura modular, com projetos separados para a lógica principal da aplicação, infraestrutura e interface de console.

Este projeto faz parte do **GitHub Copilot Bootcamp**, demonstrando as capacidades do GitHub Copilot em auxiliar no desenvolvimento de software.

## Estrutura do Projeto
```
src
├── Library.ApplicationCore
│   ├── Entities
│   │   ├── Author.cs
│   │   ├── Book.cs
│   │   ├── BookItem.cs
│   │   ├── Loan.cs
│   │   └── Patron.cs
│   ├── Enums
│   │   ├── CommonActions.cs
│   │   ├── ConsoleState.cs
│   │   ├── LoanExtensionStatus.cs
│   │   ├── LoanReturnStatus.cs
│   │   └── MembershipRenewalStatus.cs
│   ├── Interfaces
│   │   ├── ILoanRepository.cs
│   │   ├── ILoanService.cs
│   │   ├── IPatronRepository.cs
│   │   └── IPatronService.cs
│   └── Library.ApplicationCore.csproj
├── Library.Infrastructure
│   ├── Data
│   │   ├── JsonData.cs
│   │   ├── JsonLoanRepository.cs
│   │   └── JsonPatronRepository.cs
│   └── Library.Infrastructure.csproj
├── Library.Console
│   ├── Json
│   │   ├── Authors.json
│   │   ├── Books.json
│   │   ├── BookItems.json
│   │   ├── Loans.json
│   │   └── Patrons.json
│   ├── ConsoleApp.cs
│   ├── Program.cs
│   └── Library.Console.csproj

 tests
 └── UnitTests
     └── UnitTests.csproj
```

## Principais Classes e Interfaces

### **Entities**
- `Author`: Representa um autor na biblioteca.
- `Book`: Representa um livro na biblioteca.
- `BookItem`: Representa uma cópia física de um livro.
- `Loan`: Representa um empréstimo de um livro para um patrono.
- `Patron`: Representa um patrono da biblioteca.

### **Enums**
- `CommonActions`: Define ações comuns que podem ser realizadas na aplicação de console.
- `ConsoleState`: Define os diferentes estados da aplicação de console.
- `LoanExtensionStatus`: Define o status de uma extensão de empréstimo.
- `LoanReturnStatus`: Define o status de uma devolução de empréstimo.
- `MembershipRenewalStatus`: Define o status de uma renovação de associação.

### **Interfaces**
- `ILoanRepository`: Interface para operações de repositório de empréstimos.
- `ILoanService`: Interface para operações de serviço de empréstimos.
- `IPatronRepository`: Interface para operações de repositório de patronos.
- `IPatronService`: Interface para operações de serviço de patronos.

### **Infrastructure**
- `JsonData`: Lida com o carregamento e salvamento de dados de/para arquivos JSON.
- `JsonLoanRepository`: Implementa `ILoanRepository` usando dados JSON.
- `JsonPatronRepository`: Implementa `IPatronRepository` usando dados JSON.

### **Console**
- `ConsoleApp`: Classe principal para a aplicação de console.
- `Program`: Ponto de entrada para a aplicação de console.

## Como Usar

### 1. **Clone o repositório**
```sh
https://github.com/Fernandademelo/AccelerateDevGitHubCopilotSelect.git
```

### 2. **Compile o projeto**
```sh
dotnet build
```

### 3. **Execute os testes unitários**
```sh
dotnet test
```

## Licença
Este projeto é licenciado sob a Licença MIT. Veja o arquivo [LICENSE](LICENSE) para mais detalhes.


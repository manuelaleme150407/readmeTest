# 📑 To-Do List

Desenvolvimento de um software To-Do List com o objetivo de auxiliar na organização, e, posteriormente, a conclusão de tarefas. A aplicação possuirá um campo para Login, funcionalidades como: adicionar, excluir, atualizar tarefas, apresentará animações quando concluída a tarefa e mostrará notificações e status das tarefas.

## 🚀 Começando

Para acessar as instruções que permitirão que você obtenha uma cópia do projeto em operação na sua máquina local para fins de desenvolvimento e teste
consulte **[Instruções](#-implanta%C3%A7%C3%A3o)** para saber as instruções e como implantar o projeto.

### 📋 Pré-requisitos

1. Processador: Compatível com a arquitetura do software, 32 bits ou 64 bits.
2. Memória RAM: 2 GB ou mais é suficiente para programas leves.
3. Armazenamento: 100 MB a 1 GB de espaço livre, dependendo do software.
4. Permissões de Administrador: Necessárias para instalar a maioria dos aplicativos.

### 🔧 Instalação

A primeira etapa será a verificação do tipo de processador presente em sua máquina 

```
Entrar nas configurações e pesquisar sobre o processador
```

Além disso, verificar se você obtem a permissão de Administrador

```
Acessar Prompt de Comando
```

## ⚙️ Executando os testes

1. Planejamento: Verificar se funcionalidades como adicionar, editar, excluir e listar tarefas funcionam corretamente
```
- O usuário consegue adicionar uma tarefa com sucesso?
- O sistema exibe um erro ao tentar adicionar uma tarefa vazia?
- A lista de tarefas é atualizada corretamente após uma exclusão?
```

2. Tipos de Testes Automatizados: Analizar e definir o tipo de teste que será utilizado
   
- Testes Unitários
```
Exemplo de Teste Unitário com Jest:

   const { addTask } = require('./taskController');

test('Deve adicionar uma nova tarefa com sucesso', () => {
  const task = { id: 1, title: "Estudar testes", completed: false };
  const result = addTask(task);
  expect(result).toEqual(task);
});
```
- Testes de Interface (UI)
```
Exemplo de Teste de UI com Cypress:

describe('Testes da To-Do List', () => {
  it('Deve adicionar uma nova tarefa', () => {
    cy.visit('http://localhost:3000'); // URL da aplicação
    cy.get('input[name="task"]').type('Nova tarefa');
    cy.get('button[name="addTask"]').click();
    cy.contains('Nova tarefa');
  });
});
```

### 🔩 Analise os testes de ponta a ponta

Os testes de ponta a ponta verificam o funcionamento completo do sistema do ponto de vista do usuário, simulando interações reais desde o início (entrada de dados) até o fim (resultado esperado). Eles garantem que todos os componentes (frontend, backend e banco de dados) funcionem corretamente em conjunto.

- Exemplo 1: Adicionar Tarefa / Ferramenta: Cypress
```
describe('Adicionar Tarefa - Teste E2E', () => {
  it('Deve adicionar uma nova tarefa com sucesso', () => {
    cy.visit('http://localhost:3000'); // Acessa a aplicação
    cy.get('input[name="task"]').type('Estudar testes E2E'); // Insere o título
    cy.get('button[name="addTask"]').click(); // Clica no botão "Adicionar"
    cy.contains('Estudar testes E2E').should('exist'); // Verifica se a tarefa foi adicionada
  });
});

```
### ⌨️ E testes de estilo de codificação

Os testes de estilo de codificação verificam se o código segue padrões definidos de formatação e boas práticas. Eles ajudam a manter o código legível, consistente e fácil de manter, especialmente em projetos colaborativos. 

Exemplo de Configuração e Testes

- Configuração com ESLint (JavaScript)
```
{
  "env": {
    "browser": true,
    "es2021": true
  },
  "extends": ["eslint:recommended"],
  "parserOptions": {
    "ecmaVersion": 12,
    "sourceType": "module"
  },
  "rules": {
    "indent": ["error", 2],
    "quotes": ["error", "double"],
    "semi": ["error", "always"]
  }
}
```
## 📦 Implantação

Integrar testes de estilo de codificação em um sistema ativo envolve configurar ferramentas que possam ser executadas automaticamente e assegurar que o código existente esteja alinhado aos padrões definidos. Aqui estão os passos e notas adicionais para uma implantação eficaz:

1. Revisar o Código Existente
- Objetivo: Identificar discrepâncias no código atual com os padrões desejados.
- Ferramentas:
  - Execute o linter em todo o código-base para gerar relatórios sobre problemas de estilo.
  - Use ferramentas como ESLint (eslint .) ou Black (black --check .) para uma verificação inicial.
- Ação:
  - Planeje correções incrementais para não interromper o desenvolvimento ativo.
  - Configure correções automáticas, como o comando --fix no ESLint, para problemas mais simples.


## 🛠️ Construído com

* [Dropwizard](http://www.dropwizard.io/1.0.2/docs/) - O framework web usado
* [Maven](https://maven.apache.org/) - Gerente de Dependência
* [ROME](https://rometools.github.io/rome/) - Usada para gerar RSS

## 🖇️ Colaborando

Por favor, leia o [COLABORACAO.md](https://gist.github.com/usuario/linkParaInfoSobreContribuicoes) para obter detalhes sobre o nosso código de conduta e o processo para nos enviar pedidos de solicitação.

## 📌 Versão

Nós usamos [CVS](https://www.devmedia.com.br/conheca-o-cvs-mais-controle-no-desenvolvimento-em-equipe/9627) para controle de versão. Para as versões disponíveis, observe as [tags neste repositório](https://github.com/suas/tags/do/projeto). 

## ✒️ Autores

* **Matheus Almeida** - *Desenvolvimento Front-End* - [matheusalmeida](https://github.com/linkParaPerfil)
* **Murilo Moreno** - *Desenvolvimento Back-End* - [murilomoreno](https://github.com/linkParaPerfil)
* **Gabriel Luis** - *Desenvolvimento Back-End e Fron-End* - [galuis](https://github.com/linkParaPerfil)
* **Manuela Leme** - *Documentação* - [manuleme](https://github.com/linkParaPerfil)
* **João Vittor** - *Design do software* - [jvamorim](https://github.com/linkParaPerfil)
* **Gustavo Barrinha** - *Design do software* - [gbarrinha](https://github.com/linkParaPerfil)

## 📄 Licença

Este projeto está sob a licença TimeDEV - veja o arquivo [LICENSE.md](https://github.com/usuario/projeto/licenca) para detalhes.

## 🎁 Expressões de gratidão

* Conte a outras pessoas sobre este projeto 📢;
* Um agradecimento publicamente 🫂;

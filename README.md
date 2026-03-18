# Full Cycle 3.0 - DDD: Patterns

Este projeto faz parte do curso Full Cycle 3.0 e foca na implementação de padrões de Domain Driven Design (DDD) em TypeScript.

## Desafio: Implementação de OrderRepository

O objetivo deste desafio foi completar a implementação do `OrderRepository` seguindo os conceitos de DDD e TDD.

### Métodos Implementados:
- `create`: Criação de um novo pedido com seus itens.
- `update`: Atualização de um pedido existente e seus itens (utilizando transações para garantir consistência).
- `find`: Localização de um pedido pelo ID, incluindo seus itens.
- `findAll`: Listagem de todos os pedidos cadastrados.

## Segurança e Compatibilidade

Durante o desenvolvimento, foram realizadas as seguintes melhorias técnicas:
- **Segurança**: Os pacotes `sqlite3` e `typescript` foram atualizados para versões mais recentes para mitigar vulnerabilidades críticas relatadas pelo `npm audit`.
- **Compatibilidade Jest 30**: A versão do Jest utilizada no projeto removeu o alias `toThrowError`. Todas as ocorrências foram atualizadas para `toThrow` para garantir que os testes continuem funcionando corretamente.

## Como rodar o projeto

### Pré-requisitos
- Node.js instalado
- NPM instalado

### Clonar o repositório
```bash
git clone https://github.com/rubenfabio/full-cycle-3-ddd-patterns.git
```

### Instalação de dependências
Execute o comando abaixo na raiz do projeto:
```bash
npm install
```

### Executar Testes
Para rodar todos os testes automatizados:
```bash
npm test
```

Para rodar os testes em modo verbose e sem cache:
```bash
npx jest --verbose --no-cache
```

## Autor
Projeto desenvolvido como parte dos estudos de DDD no Full Cycle.

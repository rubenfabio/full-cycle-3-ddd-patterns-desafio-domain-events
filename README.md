# Full Cycle 3.0 - DDD: Patterns

Este projeto faz parte do curso Full Cycle 3.0 e foca na implementação de padrões de Domain Driven Design (DDD) em TypeScript.

## Desafio: Domain Events do Customer

Implementação do padrão Domain Events para o agregado `Customer`, garantindo que o sistema reage a mudanças de estado (criação e alteração de endereço).

### Eventos Implementados:
- `CustomerCreated`: Disparado na criação de um novo cliente.
    - `EnviaConsoleLog1Handler`: Exibe o primeiro log de criação.
    - `EnviaConsoleLog2Handler`: Exibe o segundo log de criação.
- `CustomerAddressChanged`: Disparado quando o endereço é alterado.
    - `EnviaConsoleLogHandler`: Exibe log com ID, Nome e novo Endereço.

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

Para rodar apenas os testes de eventos de Customer:
```bash
npm test src/domain/customer/event/customer-events.spec.ts
```

## Autor
Projeto desenvolvido como parte dos estudos de DDD no Full Cycle.

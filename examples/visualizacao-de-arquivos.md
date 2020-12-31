```console
abantes@AB4NT5S:~/files$ cat script.js
const string = 'colorBackgroundPrimary'

const transformKey = key => {
        return `--${key.replace( /([A-Z])/g , '-$1' ).toLowerCase()}`
}

console.log( transformKey( string ) ) // --color-background-primary
abantes@AB4NT5S:~/files$
```

```console
abantes@AB4NT5S:~/files$ cat Planejamento.md
### Conhecimentos Gerais

- Estrutura de Dados e Algoritmos
- Test/Debugging
- Codificações de Caracteres
- Padrões de Design
- Básico de Segurança da Informação
- Básico de Hardwares

### SO e Conhecimentos Gerais

- Como SOs funcionam no geral
- Ultilização Básica do Terminal
- Gerenciamento de processos
- Gerenciamento de Memória
- Threads e Concorrência
- Comunicação entre processos
- Gerenciamento de E/S
- POSIX básico

### Internet

- Navegadores e como funcionam
- Como a internet funciona?
- O que é HTTP?
- Verbos HTTP
- Status de respostas
- DNS e como ele funciona?
- O que é Nome de Domínio?
- O que é hospedagem?
- SSH
abantes@AB4NT5S:~/files$
```
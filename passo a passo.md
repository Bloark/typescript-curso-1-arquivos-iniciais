# Passo a Passo

1. npm install
2. npm run server
3. npm install typescript@4.2.2 --save-dev
4. todo codigo de typescript deve ser escrito da estrutura 
    app>>
    controllers
    model
    views
5. configurar os arquivos typescript para rodar na pasta dist
6. criar a pasta na raiz tsconfig.json e configurar

```js
{
    "compilerOptions": {
        "outDir": "dist/js",
        "target": "ES6"
    },
    
    "include": [
        "app/**/*"
    ]
}
```

7. configurando package.json para rodar, incluso a linha abaixo em script.
```js
    "compile":"tsc"
```

8. adicionado um parametro em tsconfig.json para não criara o arquivo em js enquanto nos erros não forem corrigidos.
```js
    "noEmitOnError": true
```
9. automatizando a compilação de arquivos
10. incluir no package.json em script "watch" : "tsc -w"
11. inicializar com npm run start 
12. criar controller para intergagir com a pagina.
```js
        export class NegociacaoController {

            private inputData; 
            private inputQuantidade;
            private inputValor;

            constructor() {
                this.inputData = document.querySelector('#data');
                this.inputQuantidade = document.querySelector('#quantidade');
                this.inputValor = document.querySelector('#valor');
            }

            adiciona() {
                console.log(this.inputData);
                console.log(this.inputQuantidade);
                console.log(this.inputValor);
            }
        }
```

13. tipagem no typescript
14. adicionado no tsconfig.json "noImplicitAny": true, para não aceitar o tipo any como padrão;
15. exemplo de uso de tipos de variaveis constructor(data: Date, quantidade: number, valor: number);
16. refatorado todo o codigo inserido o tipo para cada função e variavéis.
17. criado negociacoes.ts 

```js
    import { Negociacao } from "./negociacao.js";

    export class Negociacoes {
        private negociacoes: Array<Negociacao> = [];

        adiciona(negociacao : Negociacao) {
            this.negociacoes.push(negociacao);
        }
        
        lista(): Array<Negociacao> {
            return this.negociacoes;        
        }
    }
```

18.



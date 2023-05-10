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




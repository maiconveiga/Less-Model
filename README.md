# Instalações de dependências
- Less é um pre processador para css, assim como o sass
```bash
npm i --g less
npm i --g less-watch-compiler
npm init
npm i --save-dev less
npm i --save-dev less-watch-compiler
```
## Criar arquivo .gitignore
- Adicionar node_modules
```bash 
git init 
```
## Inserir no package.json o script abaixo
- "less":"less-watch-compiler ./src/styles build/styles",

# Declarar variável no less e chamando no less
- @variavel: atributo;
- @import 'arquivo.less';

# Escaping (Dentro do main.less)
- @breakpointModile: ~"(max-width:767px)";
- @breakpointTablet: ~"(min-width:768px) and (max-width:1023px)";
- @breakpointPC: ~"(min-width:1024px)";
- @media @breakpointMobile{ background-color:red}

# Mixins
- &-nome . O & refere-se ao nome da classe mãe
- .valoreeRepetifos{background-color: red; padding 8px}
- Dentro das classes, chamar .valoreeRepetifos();
- Chamar como uma função
- Ela deve estar antes de todas as chamadas

# Criar mapas -> Usar no lugar de var.less
- criar novo arquivo mapa.less
- dentro dele #colors(){bgcolor: red; btcolor:blue}
- depois importar no main.less @import "mapa.less";
- #colors[btcolor];

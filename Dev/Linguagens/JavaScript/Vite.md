Vite é uma ferramenta de construção de projetos de frontend que se destina a oferecer uma experiência de desenvolvimento mais rápida e leve para projetos de web modernos. Ela consiste em duas partes principais:

 - Um servidor de desenvolvimento que oferece melhorias de funcionalidade ricas sobre módulos de ECMAScript nativo, por exemplo Substituição de Módulo Instantânea extremamente rápida.

 - Um comando de construção que empacota o nosso código com a Rollup, pré-configurado para produzir recursos estáticos altamente otimizados para produção.
#### Características principais

**A rapidez**  
Quando você inicia um projeto em Vite a primeira coisa que ele faz é dividir seu código em duas partes: código fonte e dependências. As dependências geralmente são arquivos de Javascript que não sofrerão alterações, então elas são pré-compiladas usando o [[esbuild]], que é escrito em [[Go]] e é de 10-100 x mais rápido do que bundlers feitos com [[JavaScript]].

Já o código fonte, que geralmente vai ser um código que vai precisar sofrer alguma alteração ([[JSX]], [[TypeScript]], etc) são servidos como módulos [[JavaScript]] nativos, deixando que o [[Browser]] auxilie no trabalho do [[Bundler]]. Quando você faz uma alteração em um arquivo, o browser faz a requisição apenas dele, tornando muito mais rápidas as operações que permitem mudanças em ambiente de desenvolvimento reflitam no navegador em tempo real.

#### Pontos negativos

- O Vite até o presente momento ainda possui alguns bugs então deve ser usado em produção por sua conta e risco.
- O suporte 'direto da caixa' conta que você esteja escrevendo Javascript moderno, não oferecendo suporte legado pra IE por padrão.
- Vite ainda não possui um bom suporte SSR (Server Side Rendering ou [[Server Component]]), ainda é mais recomendado usar meta-frameworks como [[Next.js]] ou Nuxt até um release mais estável.
- Não tem suporte pra streaming imports como Snowpack e WMR tem.
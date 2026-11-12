# Desenvolvimento de aplicações multiplataforma com interfaces gráficas nativas a partir de uma base única de código

Trabalho de Conclusão de Curso em Ciência da Computação, Instituto de Computação, Universidade Federal de Alagoas (UFAL).

- **Autor:** Eduardo Maciel Alexandre
- **Orientador:** Prof. Fábio José Coutinho da Silva
- **Status:** pré-proposta (em elaboração)

## Sobre o trabalho

Frameworks multiplataforma como Electron, Flutter e React Native reduzem o custo de manter um mesmo aplicativo em vários sistemas, mas costumam fazer isso renderizando a própria interface ou embutindo uma WebView, o que resulta em aplicações que destoam do design system de cada sistema operacional e, muitas vezes, em desempenho inferior ao das ferramentas nativas (SwiftUI, WinUI 3, Jetpack Compose). Este trabalho investiga uma alternativa intermediária: construir a interface a partir de uma única base de código, mas traduzindo-a para os componentes nativos de cada plataforma, de modo que o resultado seja visual e funcionalmente indistinguível de um aplicativo escrito à mão para aquele sistema.

## Pergunta de pesquisa

> Como desenvolver aplicativos multiplataforma que fazem uso dos componentes nativos de interface em uma base única de código?

## Escopo

O foco é deliberadamente restrito: aplicações desktop simples para Windows e macOS, com interface declarativa e lógica compartilhada. A ideia central é automatizar de forma sistemática e determinística a geração dos projetos nativos de cada plataforma, preservando a possibilidade de abandonar a ferramenta a qualquer momento e continuar o desenvolvimento diretamente com as ferramentas oficiais de cada sistema. A escolha da linguagem do framework e do núcleo compartilhado faz parte da investigação e ainda não está fechada.

## Metodologia

O trabalho combina uma revisão da literatura sobre desenvolvimento multiplataforma e tradução de componentes de interface entre plataformas (buscas no Scopus e no Web of Science, organizadas com Zotero e Better BibTeX) com o desenvolvimento de um protótipo e de aplicações de referência, cujo design é feito no Figma com as bibliotecas oficiais de componentes de cada sistema. A avaliação compara aderência visual ao design system nativo e desempenho em relação a aplicações equivalentes feitas com as ferramentas recomendadas de cada plataforma.

## Estrutura do repositório

```
.
├── tcc/            # fontes LaTeX (template TCC do IC/UFAL)
├── referencias/    # arquivos .bib (Scopus, Web of Science)
├── prototipo/      # código do protótipo do framework
└── README.md
```

## Compilando o documento

```bash
cd tcc
latexmk -pdf main.tex
```

## Licença

A definir

<!-- definir (ex.: CC BY 4.0 para o texto, MIT para o código) -->

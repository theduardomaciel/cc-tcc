# Gerando interfaces nativas para desktop com código único

Trabalho de Conclusão de Curso em Ciência da Computação, Instituto de Computação, Universidade Federal de Alagoas (UFAL).

- **Autor:** Eduardo Maciel Alexandre
- **Orientador:** Prof. Dr. Fábio José Coutinho da Silva
- **Status:** pré-proposta (novembro de 2026)

## Sobre o trabalho

Frameworks multiplataforma reduzem a duplicação de código, mas costumam desenhar a própria interface ou embutir uma WebView, o que compromete a aderência ao *design system* de cada sistema operacional e tende a custar desempenho e consumo de recursos. Manter implementações nativas independentes evita esses problemas, mas exige bases de código separadas. Este trabalho propõe gerar projetos nativos para Windows (WinUI 3) e macOS (SwiftUI) a partir de uma única fonte declarativa, sem camada de renderização própria, e avaliar o resultado em relação ao código nativo escrito à mão.

## Pergunta de pesquisa

> Como gerar aplicações multiplataforma com interfaces nativas para diferentes sistemas operacionais a partir de uma única fonte declarativa, preservando o desempenho e respeitando as convenções de interface de cada plataforma?

## Escopo

O foco é deliberadamente restrito: aplicações desktop simples para Windows e macOS. A fonte única será escrita em Kotlin, com sintaxe declarativa, e o gerador será desenvolvido preferencialmente em Rust. Como o gerador produz projetos nativos padrão, o código resultante pode ser mantido diretamente com as ferramentas oficiais de cada sistema. Linux fica como trabalho futuro.

## Metodologia

A pesquisa é aplicada e experimental. Duas aplicações de referência, projetadas no Figma com as bibliotecas oficiais de componentes de cada sistema, serão implementadas em três versões: (A) escrita à mão em SwiftUI e WinUI 3; (B) gerada a partir da fonte única; (C) multiplataforma convencional, inicialmente com Electron. A avaliação compara uso de CPU, memória, tempo de resposta e tamanho de armazenamento, além da similaridade visual (SSIM) e da cobertura de componentes nativos. A revisão da literatura foi feita nas bases Scopus e Web of Science.

## Estrutura do repositório

```
.
├── README.md
├── main.tex                 # documento principal
├── ic.cls                   # classe do template de TCC do IC
├── referencias.bib
├── pre-textuais/            # preâmbulo, resumo, abstract, declaração de uso de IA
├── capitulos/               # introdução, objetivos, relevância, métodos, cronograma
├── pos-textuais/            # referências
└── res/                     # imagens do template
```

## Compilando o documento

É necessária uma distribuição TeX Live completa (o template usa `babel` em português, `bbm`, `tracklang`, entre outros pacotes).

```bash
latexmk -pdf main.tex
```

## Licença

A definir.
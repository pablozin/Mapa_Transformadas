# Sinais e Sistemas Lineares — Mapas de Transformadas (B. P. Lathi)

Material complementar de estudos para a disciplina de **Sinais e Sistemas**, focado na análise de sistemas em tempo contínuo e discreto usando **Transformada de Laplace** e **Transformada Z**, rigorosamente alinhado com o livro-texto de **B. P. Lathi**.

> [!NOTE]
> **Créditos e Referências:** A seleção de tópicos e o banco de exercícios foram estruturados com base na metodologia pedagógica e no guia de estudos do **Dr. Pedro Thiago** ([@pedrothiag](https://github.com/pedrothiag)), tomando como referência o repositório da disciplina: [signals-and-systems](https://github.com/pedrothiag/signals-and-systems).

---

## Como estudar por este repositório

Você pode utilizar este material de duas formas:

### 1. Diretamente pelo Navegador (Sem instalar nada)
- **Mapas Visuais:** Visualize as imagens completas dos mapas mentais na seção abaixo ou na pasta [`img/`](img/).
- **Tabelas de Pares:** Consulte formulários prontos com expressões e RDC em [`Formulários/`](Formulários/).
- **Resoluções:** Acesse problemas clássicos de prova resolvidos passo a passo em [`Banco de Questões/`](Banco%20de%20Questões/) (renderizados com fórmulas em $\LaTeX$).

### 2. Pelo Obsidian (Recomendado para estudo interativo)
- Faça o clone do repositório (`git clone`) ou baixe como arquivo `.zip`.
- Abra a pasta baixada como um **Cofre (Vault)** no aplicativo gratuito [Obsidian](https://obsidian.md).
- Navegue pelos arquivos interativos em [`Mapas Mentais/`](Mapas%20Mentais/) no formato `.canvas`, aproveitando o zoom dinâmico e conexões clicáveis entre os conceitos teóricos e as questões do banco.

---

## Mapas Mentais

### Transformada de Laplace (Tempo Contínuo)
Aborda definição unilateral ($0^-$), propriedades operacionais, frações parciais com método polar de resíduos, resolução de EDOs ($y_0$ vs $y_\phi$, $y_n$ vs $y_f$), estabilidade assintótica, critério de **Routh-Hurwitz** e **realização de sistemas** (formas canônicas).

<p align="center">
  <img src="img/MAPA%20Laplace.png" alt="Mapa Mental da Transformada de Laplace" width="100%">
</p>

---

### Transformada Z (Tempo Discreto)
Cobre definição unilateral, anel de convergência (RDC), propriedades com condições passadas ($n-1, n-2$) e avanço ($n+1, n+2$), inversão pela regra clássica $\frac{X(z)}{z}$, resolução de equações de diferenças, estabilidade no círculo unitário, **critério de Jury**, **transformação bilinear** e a **ponte conformal** $z = e^{sT}$.

<p align="center">
  <img src="img/MAPA%20Z.png" alt="Mapa Mental da Transformada Z" width="100%">
</p>

---

## Estrutura do Repositório

```text
├── Mapas Mentais/       # Arquivos .canvas para navegação interativa no Obsidian
├── Formulários/         # Tabelas de pares imediatos e regras de resíduos
├── Banco de Questões/   # Questões do Lathi resolvidas (dicas + passo a passo)
├── img/                 # Imagens em alta resolução dos mapas mentais
└── README.md            # Guia de estudo e navegação
  ```

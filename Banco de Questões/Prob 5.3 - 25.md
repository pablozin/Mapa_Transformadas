---
tags:
  - transformada_z
  - sistemas_inversos
  - causalidade
  - nivel_medio
origem: Lathi Prob. 5.3-25
---
### Problema 5.3-25
Um sistema possui resposta ao impulso $h[n] = u[n - 3]$.
a) Determine a resposta ao impulso do sistema inverso $h_i[n]$.
b) O sistema inverso é causal? É estável?

> [!tip]- Dica de Resolução
> A função de transferência do sistema inverso é o inverso algébrico: $H_i[z] = \frac{1}{H[z]}$. Observe as potências de $z$ resultantes: potências positivas $z^{+k}$ correspondem a avanços no tempo ($n+k$).

> [!success]- Resolução Passo a Passo
> Transformando a resposta ao impulso $h[n] = u[n - 3]$ pelo par do degrau com atraso:
> 
> $$H[z] = z^{-3} \left( \frac{z}{z - 1} \right) = \frac{1}{z^2(z - 1)}$$
> 
> Encontrando a função do sistema inverso:
> 
> $$H_i[z] = \frac{1}{H[z]} = z^2(z - 1) = z^3 - z^2$$
> 
> Invertendo diretamente para o tempo com a propriedade do avanço:
> 
> $$h_i[n] = \delta[n + 3] - \delta[n + 2]$$
> 
> Análise de estabilidade e causalidade:
> 
> Como a saída depende de instantes futuros ($n = -3$ e $n = -2$), o sistema inverso é **NÃO CAUSAL**.
> 
> A soma de sua resposta ao impulso é absolutamente somável ($\sum |h_i[n]| = 1 + 1 = 2 < \infty$), portanto ele é **ESTÁVEL**.
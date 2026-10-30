---
tags:
- transformada_z
- estabilidade
- realimentacao
- jury
- transformacao_bilinear
- nivel_dificil
origem: Lathi Prob. 5.5-4
---
### Problema 5.5-4
Considere um sistema de controle discreto em malha fechada com realimentação negativa unitária, cuja função de transferência de malha direta é dada por:

$$G(z) = \frac{K(z + 0{,}5)}{(z - 1)(z - 0{,}2)}$$

Determine a faixa de valores do ganho $K$ para a qual o sistema em malha fechada é assintoticamente estável.

> [!tip]- Dica de Resolução
> A função de transferência em malha fechada é $T(z) = \frac{G(z)}{1 + G(z)}$. Obtenha a equação característica $Q(z) = 0$ a partir do denominador.
> Para que o sistema seja assintoticamente estável, todas as raízes de $Q(z)$ devem estar estritamente dentro da circunferência unitária ($|z| < 1$).
> Você pode resolver de duas formas equivalentes comumente cobradas em prova:
> 1. **Critério de Jury:** Aplicar diretamente as 3 condições para polinômios de 2º grau ($Q(1) > 0$, $(-1)^n Q(-1) > 0$ e $|a_0| < a_2$).
> 2. **Transformação Bilinear:** Fazer a substituição conforme $z = \frac{w + 1}{w - 1}$, obtendo $Q'(w) = 0$, e aplicar o critério de **Routh-Hurwitz** clássico no plano $w$.
>
> A resposta final deve ser a interseção de todas as inequações encontradas para o ganho $K$.

> [!success]- Resolução Passo a Passo
> **1. Determinação da Equação Característica em Malha Fechada:**
> 
> A função de transferência do sistema em malha fechada com realimentação unitária é:
> 
> $$T(z) = \frac{G(z)}{1 + G(z)} = \frac{\frac{K(z + 0{,}5)}{(z - 1)(z - 0{,}2)}}{1 + \frac{K(z + 0{,}5)}{(z - 1)(z - 0{,}2)}} = \frac{K(z + 0{,}5)}{(z - 1)(z - 0{,}2) + K(z + 0{,}5)}$$
> 
> O denominador igualado a zero fornece a equação característica $Q(z) = 0$:
> 
> $$(z - 1)(z - 0{,}2) + K(z + 0{,}5) = 0$$
> 
> Desenvolvendo os produtos:
> 
> $$z^2 - 1{,}2z + 0{,}2 + Kz + 0{,}5K = 0$$
> 
> Agrupando os termos em potências de $z$:
> 
> $$Q(z) = z^2 + (K - 1{,}2)z + (0{,}5K + 0{,}2) = 0$$
> 
> Coeficientes do polinômio $Q(z) = a_2 z^2 + a_1 z + a_0$:
> - $a_2 = 1$
> - $a_1 = K - 1{,}2$
> - $a_0 = 0{,}5K + 0{,}2$
> 
> ---
> 
> **2. Aplicação do Critério de Estabilidade de Jury:**
> 
> Para um sistema de segunda ordem ($n = 2$), as raízes estarão no interior do círculo unitário ($|z| < 1$) se e somente se as três condições a seguir forem simultaneamente satisfeitas:
> 
> - **Condição I: $Q(1) > 0$**
>   $$Q(1) = 1^2 + (K - 1{,}2)(1) + (0{,}5K + 0{,}2) > 0$$
>   $$1 + K - 1{,}2 + 0{,}5K + 0{,}2 > 0 \implies 1{,}5K > 0 \implies K > 0$$
> 
> - **Condição II: $(-1)^2 Q(-1) = Q(-1) > 0$**
>   $$Q(-1) = (-1)^2 + (K - 1{,}2)(-1) + (0{,}5K + 0{,}2) > 0$$
>   $$1 - K + 1{,}2 + 0{,}5K + 0{,}2 > 0$$
>   $$2{,}4 - 0{,}5K > 0 \implies 0{,}5K < 2{,}4 \implies K < 4{,}8$$
> 
> - **Condição III: $|a_0| < a_2 \implies |a_0| < 1$**
>   $$|0{,}5K + 0{,}2| < 1$$
>   Desdobrando a inequação modular:
>   $$-1 < 0{,}5K + 0{,}2 < 1$$
>   Subtraindo $0{,}2$ em todos os membros:
>   $$-1{,}2 < 0{,}5K < 0{,}8$$
>   Multiplicando por 2:
>   $$-2{,}4 < K < 1{,}6$$
> 
> ---
> 
> **3. Interseção dos Intervalos:**
> 
> Combinando todas as restrições obtidas:
> 
> $$\begin{cases}
> K > 0 \\
> K < 4{,}8 \\
> -2{,}4 < K < 1{,}6
> \end{cases}$$
> 
> A faixa de valores do ganho $K$ para estabilidade assintótica é:
> 
> $$0 < K < 1{,}6$$
> 
> ---
> 
> **4. Verificação Opcional via Transformação Bilinear:**
> 
> Substituindo $z = \frac{w + 1}{w - 1}$ em $Q(z)$ e multiplicando por $(w - 1)^2$:
> 
> $$Q'(w) = (w + 1)^2 + (K - 1{,}2)(w + 1)(w - 1) + (0{,}5K + 0{,}2)(w - 1)^2 = 0$$
> 
> Expandindo e agrupando em potências de $w$:
> 
> $$Q'(w) = (1{,}5K)w^2 + (1{,}6 - K)w + (2{,}4 - 0{,}5K) = 0$$
> 
> Pelo critério de Routh-Hurwitz para 2ª ordem, todos os coeficientes devem ser estritamente positivos (mesmo sinal):
> 1. $1{,}5K > 0 \implies K > 0$
> 2. $1{,}6 - K > 0 \implies K < 1{,}6$
> 3. $2{,}4 - 0{,}5K > 0 \implies K < 4{,}8$
> 
> Confirmando com exatidão a mesma faixa:
> 
> $$0 < K < 1{,}6$$
---
tags: [laplace, formulario, tabelas, pares_transformada]
origem: "B. P. Lathi - Sinais e Sistemas Lineares (Tabela 4.1)"
---
# Tabela de Pares da Transformada de Laplace

Esta tabela reúne os principais pares da **Transformada de Laplace Unilateral** ($\int_{0^-}^{\infty} x(t)e^{-st}dt$) de acordo com o livro de B. P. Lathi.

> [!important] Convenção do Limite $0^-$
> No livro do Lathi, a transformada unilateral inicia em $t = 0^-$. Isso garante que o impulso $\delta(t)$ e suas derivadas centradas na origem sejam integralmente capturados pela transformada.

---

## 1. Pares Elementares e Polinomiais

| No. | Sinal no Tempo $x(t)$ | Transformada $X(s)$ | Região de Convergência (RDC) |
| :---: | :--- | :---: | :---: |
| **1** | $\delta(t)$ | $1$ | Todo o plano $s$ |
| **2** | $\delta(t - t_0) \quad (t_0 \ge 0)$ | $e^{-st_0}$ | Todo o plano $s$ |
| **3** | $\dot{\delta}(t) = \frac{d\delta(t)}{dt}$ | $s$ | Todo o plano $s$ |
| **4** | $u(t)$ | $\frac{1}{s}$ | $\text{Re}\{s\} > 0$ |
| **5** | $t \, u(t)$ | $\frac{1}{s^2}$ | $\text{Re}\{s\} > 0$ |
| **6** | $t^n \, u(t) \quad (n \in \mathbb{N})$ | $\frac{n!}{s^{n+1}}$ | $\text{Re}\{s\} > 0$ |

---

## 2. Pares Exponenciais e Amortecidos

| No. | Sinal no Tempo $x(t)$ | Transformada $X(s)$ | Região de Convergência (RDC) |
| :---: | :--- | :---: | :---: |
| **7** | $e^{-\lambda t} \, u(t)$ | $\frac{1}{s + \lambda}$ | $\text{Re}\{s\} > -\text{Re}\{\lambda\}$ |
| **8** | $t e^{-\lambda t} \, u(t)$ | $\frac{1}{(s + \lambda)^2}$ | $\text{Re}\{s\} > -\text{Re}\{\lambda\}$ |
| **9** | $\frac{t^n}{n!} e^{-\lambda t} \, u(t)$ | $\frac{1}{(s + \lambda)^{n+1}}$ | $\text{Re}\{s\} > -\text{Re}\{\lambda\}$ |

---

## 3. Pares Trigonométricos e Oscilatórios

| No. | Sinal no Tempo $x(t)$ | Transformada $X(s)$ | Região de Convergência (RDC) |
| :---: | :--- | :---: | :---: |
| **10** | $\cos(\omega_0 t) \, u(t)$ | $\frac{s}{s^2 + \omega_0^2}$ | $\text{Re}\{s\} > 0$ |
| **11** | $\sin(\omega_0 t) \, u(t)$ | $\frac{\omega_0}{s^2 + \omega_0^2}$ | $\text{Re}\{s\} > 0$ |
| **12** | $\cos(\omega_0 t + \theta) \, u(t)$ | $\frac{s \cos\theta - \omega_0 \sin\theta}{s^2 + \omega_0^2}$ | $\text{Re}\{s\} > 0$ |
| **13** | $e^{-\alpha t} \cos(\omega_0 t) \, u(t)$ | $\frac{s + \alpha}{(s + \alpha)^2 + \omega_0^2}$ | $\text{Re}\{s\} > -\alpha$ |
| **14** | $e^{-\alpha t} \sin(\omega_0 t) \, u(t)$ | $\frac{\omega_0}{(s + \alpha)^2 + \omega_0^2}$ | $\text{Re}\{s\} > -\alpha$ |
| **15** | $t \cos(\omega_0 t) \, u(t)$ | $\frac{s^2 - \omega_0^2}{(s^2 + \omega_0^2)^2}$ | $\text{Re}\{s\} > 0$ |
| **16** | $t \sin(\omega_0 t) \, u(t)$ | $\frac{2\omega_0 s}{(s^2 + \omega_0^2)^2}$ | $\text{Re}\{s\} > 0$ |

---

## 4. Fórmula Direta de Polos Complexos Conjugados (Forma de Lathi)

Para frações parciais com par de polos conjugados $p_{1,2} = -\alpha \pm j\omega_0$:

$$\frac{r e^{j\theta}}{s + \alpha - j\omega_0} + \frac{r e^{-j\theta}}{s + \alpha + j\omega_0} \iff 2r e^{-\alpha t} \cos(\omega_0 t + \theta) \, u(t)$$

> [!tip] Como usar o resíduo polar
> 1. Encontre apenas o resíduo do polo com $+j\omega_0$: $A_1 = \left. X(s)(s + \alpha - j\omega_0) \right|_{s = -\alpha + j\omega_0}$.
> 2. Escreva o número complexo na forma polar: $A_1 = r e^{j\theta} = |A_1| \angle A_1$.
> 3. Escreva imediatamente a resposta no tempo como $2|A_1| e^{-\alpha t} \cos(\omega_0 t + \angle A_1) u(t)$ sem passar por frações reais.

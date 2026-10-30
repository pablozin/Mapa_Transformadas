---
tags: [transformada_z, formulario, tabelas, pares_transformada]
origem: "B. P. Lathi - Sinais e Sistemas Lineares (Tabela 5.1)"
---
# Tabela de Pares da Transformada Z

Esta tabela reúne os principais pares da **Transformada Z Unilateral** ($\sum_{n=0}^{\infty} x[n]z^{-n}$) de acordo com o livro de B. P. Lathi.

> [!important] Regra da Tabela de Z
> Praticamente todas as formas elementares na tabela do Lathi possuem $z$ no numerador (ex: $\frac{z}{z - \gamma}$). Portanto, para inverter por frações parciais, sempre expanda $\frac{X(z)}{z}$ e multiplique $z$ de volta no final antes de consultar a tabela.

---

## 1. Pares Elementares e Polinomiais

| No. | Sequência no Tempo $x[n]$ | Transformada $X(z)$ | Região de Convergência (RDC) |
| :---: | :--- | :---: | :---: |
| **1** | $\delta[n]$ | $1$ | Todo o plano $z$ |
| **2** | $\delta[n - m] \quad (m \ge 0)$ | $z^{-m}$ | $|z| > 0$ |
| **3** | $u[n]$ | $\frac{z}{z - 1} = \frac{1}{1 - z^{-1}}$ | $|z| > 1$ |
| **4** | $n \, u[n]$ | $\frac{z}{(z - 1)^2}$ | $|z| > 1$ |
| **5** | $n^2 \, u[n]$ | $\frac{z(z + 1)}{(z - 1)^3}$ | $|z| > 1$ |

---

## 2. Pares Exponenciais (Geométricos)

| No. | Sequência no Tempo $x[n]$ | Transformada $X(z)$ | Região de Convergência (RDC) |
| :---: | :--- | :---: | :---: |
| **6** | $\gamma^n \, u[n]$ | $\frac{z}{z - \gamma} = \frac{1}{1 - \gamma z^{-1}}$ | $|z| > |\gamma|$ |
| **7** | $n \gamma^n \, u[n]$ | $\frac{\gamma z}{(z - \gamma)^2}$ | $|z| > |\gamma|$ |
| **8** | $n^2 \gamma^n \, u[n]$ | $\frac{\gamma z(z + \gamma)}{(z - \gamma)^3}$ | $|z| > |\gamma|$ |
| **9** | $(n + 1)\gamma^n \, u[n]$ | $\frac{z^2}{(z - \gamma)^2}$ | $|z| > |\gamma|$ |
| **10** | $\frac{(n + 1)(n + 2)}{2!} \gamma^n \, u[n]$ | $\frac{z^3}{(z - \gamma)^3}$ | $|z| > |\gamma|$ |

---

## 3. Pares Trigonométricos e Oscilatórios Amortecidos

| No. | Sequência no Tempo $x[n]$ | Transformada $X(z)$ | Região de Convergência (RDC) |
| :---: | :--- | :---: | :---: |
| **11** | $\cos(\Omega_0 n) \, u[n]$ | $\frac{z(z - \cos\Omega_0)}{z^2 - 2z\cos\Omega_0 + 1}$ | $|z| > 1$ |
| **12** | $\sin(\Omega_0 n) \, u[n]$ | $\frac{z\sin\Omega_0}{z^2 - 2z\cos\Omega_0 + 1}$ | $|z| > 1$ |
| **13** | $r^n \cos(\Omega_0 n) \, u[n]$ | $\frac{z(z - r\cos\Omega_0)}{z^2 - 2r z \cos\Omega_0 + r^2}$ | $|z| > |r|$ |
| **14** | $r^n \sin(\Omega_0 n) \, u[n]$ | $\frac{z(r\sin\Omega_0)}{z^2 - 2r z \cos\Omega_0 + r^2}$ | $|z| > |r|$ |
| **15** | $r^n \cos(\Omega_0 n + \theta) \, u[n]$ | $\frac{z(z\cos\theta - r\cos(\Omega_0 - \theta))}{z^2 - 2r z \cos\Omega_0 + r^2}$ | $|z| > |r|$ |

---

## 4. Fórmula Direta de Polos Complexos Conjugados em $\frac{X(z)}{z}$

Quando a expansão em frações parciais de $\frac{X(z)}{z}$ apresentar o par de polos conjugados $d_{1,2} = r e^{\pm j\Omega_0}$:

$$\frac{X(z)}{z} = \dots + \frac{A_1}{z - r e^{j\Omega_0}} + \frac{A_1^*}{z - r e^{-j\Omega_0}} + \dots$$

Multiplicando $z$ de volta:

$$X(z) = \dots + \frac{A_1 z}{z - r e^{j\Omega_0}} + \frac{A_1^* z}{z - r e^{-j\Omega_0}} + \dots$$

Escrevendo o resíduo na forma polar $A_1 = |A_1| e^{j\theta_1}$:

$$x[n] = \dots + 2|A_1| r^n \cos(\Omega_0 n + \theta_1) \, u[n] + \dots$$

> [!tip] Resumo da Inversa Imediata
> Se $A_1 = |A_1| \angle \theta_1$ e o polo é $r \angle \Omega_0$, o sinal no tempo correspondente é diretamente:
> $$2|A_1| r^n \cos(\Omega_0 n + \theta_1) u[n]$$

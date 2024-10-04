# Distributions Overview

## Discrete Distributions

| Distribution                      | Definition                                                                                     | p.m.f.                                             | m.g.f.                                        |
|-----------------------------------|-----------------------------------------------------------------------------------------------|---------------------------------------------------|-----------------------------------------------|
| **1.1 Bernoulli Distribution**    | Represents a single trial with two outcomes: success (1) and failure (0).                   | P(X = x) = p^x (1 - p)^(1 - x), x ∈ {0, 1}      | M(t) = (p * e^t) / (1 - (1 - p) * e^t)     |
| **1.2 Binomial Distribution**     | Represents the number of successes in n independent Bernoulli trials.                        | P(X = k) = C(n, k) * p^k * (1 - p)^(n - k), k = 0, 1, 2, ..., n | M(t) = (1 - p + p * e^t)ⁿ                     |
| **1.3 Poisson Distribution**      | Models the number of events occurring in a fixed interval of time or space, given a known constant mean rate λ. | P(X = k) = (λ^k * e^(-λ)) / k!, k = 0, 1, 2, ...  | M(t) = e^(λ * (e^t - 1))                      |
| **1.4 Geometric Distribution**    | Models the number of trials needed to get the first success.                                 | P(X = k) = (1 - p)^(k - 1) * p, k = 1, 2, 3, ...  | M(t) = (p * e^t) / (1 - (1 - p) * e^t)       |
| **1.5 Negative Binomial Distribution** | Models the number of trials needed to achieve a fixed number of successes r.            | P(X = k) = C(k + r - 1, r - 1) * p^r * (1 - p)^k, k = 0, 1, 2, ... | M(t) = (p / (1 - (1 - p) * e^t))^r              |

## Continuous Distributions

| Distribution                      | Definition                                                                                     | p.d.f.                                             | m.g.f.                                        |
|-----------------------------------|-----------------------------------------------------------------------------------------------|---------------------------------------------------|-----------------------------------------------|
| **2.1 Uniform Distribution**      | A distribution where all intervals of the same length within the distribution's range are equally probable. | f(x) = 1 / (b - a), a ≤ x ≤ b                     | M(t) = (e^(b * t) - e^(a * t)) / (t * (b - a))  |
| **2.2 Normal Distribution**       | A continuous distribution that is symmetric around the mean μ and characterized by its mean and standard deviation σ. | f(x) = (1 / √(2πσ²)) * e^(-((x - μ)² / (2σ²)))   | M(t) = e^(μ * t + (σ² * t²) / 2)              |
| **2.3 Exponential Distribution**  | Models the time between events in a Poisson process.                                         | f(x) = λ * e^(-λx), x ≥ 0                            | M(t) = λ / (λ - t), t < λ                     |
| **2.4 Gamma Distribution**        | A two-parameter family of continuous distributions, generalizing the exponential distribution. | f(x) = (λ^k * x^(k - 1) * e^(-λx)) / (k - 1)!, x ≥ 0 | M(t) = (λ / (λ - t))^k                        |
| **2.5 Beta Distribution**         | A family of continuous distributions defined on the interval [0, 1].                        | f(x) = (x^(α - 1) * (1 - x)^(β - 1)) / B(α, β), 0 < x < 1 | M(t) = [B(α + β, β) * B(α + t, β)] / B(α, β)   |
| **2.6 Chi-Squared Distribution**  | A special case of the gamma distribution and arises in the context of hypothesis testing.    | f(x) = [1 / (2^(k/2) * Γ(k/2))] * x^((k/2) - 1) * e^(-x/2), x ≥ 0 | M(t) = (1 - 2t)^(-k/2), t < 1/2               |
| **2.7 t-Distribution**            | A distribution used in hypothesis testing and constructing confidence intervals, particularly with small sample sizes. | f(x) = [Γ((v + 1) / 2)] / [√(vπ) * Γ(v / 2)] * (1 + (x² / v))^{-(v + 1) / 2} | Does not exist for t-distribution when v ≤ 2 |
| **2.8 F-Distribution**            | A ratio of two scaled chi-squared distributions and used primarily in analysis of variance (ANOVA). | f(x) = [Γ((d_1 + d_2) / 2)] / [Γ(d_1 / 2) * Γ(d_2 / 2)] * (d_1 / d_2)^(d_1 / 2) * x^((d_1 / 2) - 1) * (1 + (d_1 / d_2)x)^{-(d_1 + d_2) / 2}, x ≥ 0 | M(t) = (1 - d_1 / d_2 * t)^(-d_1 / 2), t < d_2 / d_1 |


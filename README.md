# Asymptotic Equivalences

In the lectures, we said that logarithms with different bases don't affect the
asymptotic complexity of an algorithm. Prove that $O(\log_{2} n)$ is the same as
$O(\log_{5} n)$. Use the mathematical definition of $O$ -- do a formal proof,
not just the intuition.

I have started with the formal definition of $O$ below. Add your answer to this
markdown file. [This
page](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/writing-mathematical-expressions)
might help with the notation for mathematical expressions.

$T(n) \in O(f(n)) \iff \exists c, n_0: T(n) \leq c \cdot f(n) \forall n \geq n_0$

## Proof
- In the definition of Big $O$ $T(n) \in O(f(n)) \iff \exists c, n_0: T(n) \leq c \cdot f(n) \forall n \geq n_0$
- We want to show that $T(n) \le c \cdot \log_{5}n$ using $T(n) = \log_{2}n$
- Substitute $\log_{2}n$ into the Big $O$ definition
- Use the change of base formula to convert the expression in terms of $\log_{5}n$
- Change of base formula:
  - $log_{b}(a) = \frac{\log_{x}(a)}{\log_{x}(2)}$
  - $\log_{2}n = \frac{\log_{5}(n)}{\log_{5}(2)}$
- This gives us:
  - $T(n) \le c \cdot \frac{\log_{5}n}{\log_{5}2}\space\forall n \geq n_0$
- pull out the constant factor:
  - $\frac{1}{\log_{5}(2)}$
- This give us:
  - $T(n) \leq c \cdot \frac{1}{\log_{5}(2)}\cdot \log_{5}(n)\space\forall n \geq n_0$
- This shows that $T(n) \in O(\log_{5}(n)$
- In the definition of Big $O$, $c$ can be any constant we can switch the bases without it affecting the Big $O$ notation


I used this website to verify I had the change of base formula correct. 
- https://www.khanacademy.org/math/algebra2/x2ec2f6f830c9fb89:logs/x2ec2f6f830c9fb89:change-of-base/a/logarithm-change-of-base-rule-intro

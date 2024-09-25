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
- First use the definition of Big $0$ and substitute in $\log_{2}n \forall n \ge n_0$
- Use the change of base formula to convert the expression in terms of $\log_{5}n$
- Change of base formula
- $log_{b}(a) = \frac{\log_{x}(a)}{\log_{x}(2)}$
- Writeout expression in converted form
- pull out the constant variable $\frac{1]{\log_{5}(2)}
- This give us $\log_{5}(n)$ by itself
- Again going beck to the definition we can see that $T(n) \in O(\log_{2}(n))$
- since in the definition of Big $O$ $c$ can be any constant we can switch the bases without it affecting the Big $O$ notation


I used this website to verify I had the change of base formula correct. 
- https://www.khanacademy.org/math/algebra2/x2ec2f6f830c9fb89:logs/x2ec2f6f830c9fb89:change-of-base/a/logarithm-change-of-base-rule-intro

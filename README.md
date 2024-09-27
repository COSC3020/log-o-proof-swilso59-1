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
- We want to show that if $T(n) \in O(\log_{2}(n))$, then $T(n) \in O(\log_{5}(n))$
- Since $T(n) \in O(\log_{2}(n))$
- We can substitute $\log_{2}n$ into the Big $O$ definition
- Use the change of base formula to convert the expression in terms of $\log_{5}n$
- Change of base formula:
  - $log_{b}(a) = \frac{\log_{x}(a)}{\log_{x}(2)}$
  - $\log_{2}n = \frac{\log_{5}(n)}{\log_{5}(2)}$
- This gives us:
  - $T(n) \le c \cdot \frac{\log_{5}(n)}{\log_{5}(2)}\space\forall n \geq n_0$
- pull out the constant factor:
  - $\frac{1}{\log_{5}(2)}$
- This give us:
  - $T(n) \leq c \cdot \frac{1}{\log_{5}(2)}\cdot \log_{5}(n)\space\forall n \geq n_0$
- This shows that $T(n) \in O(\log_{5}(n)$
- In the definition of Big $O$, $c$ can be any constant. Meaning we can switch the bases without it affecting the Big $O$ notation


I used this website to verify I had the change of base formula correct. 
- https://www.khanacademy.org/math/algebra2/x2ec2f6f830c9fb89:logs/x2ec2f6f830c9fb89:change-of-base/a/logarithm-change-of-base-rule-intro

Based off what was covered in lecture. I remembered alot of this assigment and using the change of base formula. 

I was getting stuck in a few spots so looked at a few repositories.
- https://github.com/COSC3020/log-o-proof-noah-mulvaney
- https://github.com/COSC3020/log-o-proof-Powerfuljackell
- https://github.com/COSC3020/log-o-proof-swilso59

“I certify that I have listed all sources used to complete this exercise, including the use
of any Large Language Models. All of the work is my own, except where stated
otherwise. I am aware that plagiarism carries severe penalties and that if plagiarism is
suspected, charges may be filed against me without prior notice.”


There are many variants of hierarchical clustering; here we explore 3.
The key difference is how you measure the distance between two clusters S<sub>1</sub> and S<sub>2</sub>.

Single-Link measures the shortest link ![alt text](https://wikimedia.org/api/rest_v1/media/math/render/svg/4d5208d4d05986c52be1b10e84608e4972a07ca4)

\textbf{Complete-Link: } measures the longest link $\displaystyle{\textbf{d}(S_1,S_2) = \max_{(s_1,s_2) \in S_1 \times S_2} \|s_1 - s_2\|_2}$. \\

\textbf{Mean-Link: } measures the distances to the means. \\
 First computes $a_1 = \frac{1}{|S_1|} \sum_{s \in S_1} s$ and 
$a_2 = \frac{1}{|S_2|} \sum_{s \in S_2} s$ then
$\displaystyle{\textbf{d}(S_1, S_2) = \|a_1 - a_2\|_2}$ 

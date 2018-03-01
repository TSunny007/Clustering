# Hierarchical-Clustering
Comparing the usability of different kinds of Hierarchical clustering

There are many variants of hierarchical clustering; here we explore 3.  The key difference is how you measure the distance ![equation]http://latex.codecogs.com/gif.latex?%24%5Ctextbf%7Bd%7D%28S_1%2C%20S_2%29%24 between two clusters http://latex.codecogs.com/gif.latex?%24S_1%24 and http://latex.codecogs.com/gif.latex?%24S_2%24.  
\begin{itemize}
\item[\textsf{Single-Link: }] measures the shortest link $\displaystyle{\textbf{d}(S_1,S_2) = \min_{(s_1,s_2) \in S_1 \times S_2} \|s_1 - s_2\|_2}$. 

\item[\textsf{Complete-Link: }] measures the longest link $\displaystyle{\textbf{d}(S_1,S_2) = \max_{(s_1,s_2) \in S_1 \times S_2} \|s_1 - s_2\|_2}$. 

\item[\textsf{Mean-Link: }] measures the distances to the means.  First compute 
$a_1 = \frac{1}{|S_1|} \sum_{s \in S_1} s$ and 
$a_2 = \frac{1}{|S_2|} \sum_{s \in S_2} s$ then
$\displaystyle{\textbf{d}(S_1, S_2) = \|a_1 - a_2\|_2}$ .
\end{itemize}

# Central Piecewise Mechanism

We propose the central piecewise mechanism (CPM), a novel $\epsilon$-differentially private mechanim for a numeric query. The CPM has no complex hyper-parameters, and the variance of the output values is theoretically analyzed. By capturing the characteristics of global sensitivity in detail, the amount of noise can be reduced compared with that of the state-of-the-art method.  
Furthermore, we enhance the CPM for handling multiple numeric queries, which are independent of each other. This study considers, for the first time to our knowledge, a situation in which each query is assigned its own privacy level. Under this condition, the proposed method achieves the strongest privacy guarantees for the queries in their entirety when using the CPM. Moreover, we propose an efficient heuristic algorithm that provides a sub-optimal privacy guarantee within a practical time frame even when the number of queries increases.

In "Output Variance" folder, we evaluated the output variance of the CPM. (The theoretical analysis is provided in the paper.) We also explored an appropriate value for the parameter $b$ in the CPM.

In "Single Numeric Query" folder, we compared the output errors for a single numeric query among the CPM, Laplace mechanism (LM), and the state-of-the-art composite differentially private mechanism (CDPM).  
← For the ${\it unbounded}$ mechanism for comparison evaluation, several mechanisms other than the LM exist [[Geng et al., 2015](https://doi.org/10.1109/JSTSP.2015.2425831), [Soria-Comas and Domingo-Ferrer, 2013](https://doi.org/10.1016/j.ins.2013.07.004)]; however, their accuracy is almost equivalent to the LM (especially when $\epsilon$ is relatively small) [[Wang et al., 2019](https://doi.org/10.1109/ICDE.2019.00063)]. Therefore, we employed the most conventional LM in this study. Although detailed discussion and development of ${\it unbounded}$ mechanisms are out of scope for this study (because we focus on bounded and unbiased mechanisms), they would be still an important future research direction.

In "Multiple Numeric Queries" folder, we demonstrated the utility of the enhanced CPM and its heuristic algorithm by comparing with a straightforward approach, in terms of privacy guarantees and accuracy. When the required privacy level is assigned to each query, the proposed methods guarantee stronger privacy for the queries in their entirety. This conversely implies that given an overall privacy level, more privacy budget can be distributed to each query; therefore, the analysis accuracy can be improved. In the evaluation of accuracy, we used real census data (from [IPUMS International](https://international.ipums.org/international/)) as well.

In "RunTime.ipynb", we measured the run time of solving the minimization problems in the enhanced CPM and heuristic algorithm. 

## Future Directions
・Incorporating the concept of smooth (local) sensitivity for generating noise more in line with reality.

・Improving the heuristic algorithm by performing a detailed theoretical analysis and developing methods for a larger $k$.

・Considering situations where there are non-independent queries. (The computational complexity might be reduced by lowering the number of dimensions.)

・Refining the method of determining the value of $b$. (e.g., Representing it as a function of $m$ and $\epsilon$.)

・Finding appropriate initial values and bounds when solving optimization problems. (Actually, 'Positive directional derivative for linesearch' situation often occurs, so the results in our experiments may not be truly optimal. We do not yet know how to deal with this, and this will be another important future issue.)

## Note

For details of our methods and discussion, please see our paper entitled "Central Piecewise Mechanism for Numeric Queries".  
(cf. [Privacy-Optimized Randomized Response](https://github.com/ay0408/Optimized-RR), [Privacy-Optimized Piecewise Mechanism](https://github.com/ay0408/Generalized-PM))

### Contact
Akito Yamamoto

Division of Medical Data Informatics, Human Genome Center,

the Institute of Medical Science, the University of Tokyo

a-ymmt@ims.u-tokyo.ac.jp

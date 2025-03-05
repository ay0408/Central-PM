# Central Piecewise Mechanism (CPM)

In "Output Variance" folder, we evaluated the output variance of the CPM. (The theoretical analysis is provided in the paper.) We also explored an appropriate value for the parameter $b$ in the CPM.

In "Single Numeric Query" folder, we compared the output errors for a single numeric query among the CPM, Laplace mechanism (LM), and the state-of-the-art composite differentially private mechanism (CDPM). 

In "Multiple Numeric Queries" folder, we demonstrated the utility of the enhanced CPM and its heuristic algorithm by comparing with a straightforward approach, in terms of privacy guarantees and accuracy. When the required privacy level is assigned to each query, the proposed methods guarantee stronger privacy for the queries in their entirety. This conversely implies that given an overall privacy level, more privacy budget can be distributed to each query; therefore, the analysis accuracy can be improved. In the evaluation of accuracy, we used real census data (from [IPUMS International](https://international.ipums.org/international/)) as well.

In "RunTime.ipynb", we measured the run time of solving the minimization problems in the enhanced CPM and heuristic algorithm. 

## Future Directions
・

## Note

For details of our methods and discussion, please see our paper entitled "Central Piecewise Mechanism for Numeric Queries".

### Contact
Akito Yamamoto

Division of Medical Data Informatics, Human Genome Center,

the Institute of Medical Science, the University of Tokyo

a-ymmt@ims.u-tokyo.ac.jp

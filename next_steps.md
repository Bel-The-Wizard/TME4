# Next steps

1. **Complete the statistics of this study.**
   - Run the permutation tests: `python run_analysis.py --only q2 q3 --jobs <cores>`. Q2 needs about 3 h on one core.
   - Check the post-hoc size-control test against the full paper of Dinga et al. (2020).
2. **Settle the open choices and re-run** (minutes):
   - COVARIANCE site weights;
   - classifier penalty;
   - correlation threshold for blocks;
   - minimum sizes per line;
   - transformations of skewed features;
   - central charges for J1-J2, ANNNI, cluster-Ising and XY (to look up and cite).
3. **Richer structure: the Hodge route.**
   - Build each problem as a simplicial complex from its factor graph (each term's sites, closed under subsets).
   - Read its Hodge Laplacians and Betti numbers.
   - Test whether this recovers what the factor graph missed (Q3b). For example, the three-body term of XOR-3 becomes a filled triangle, while three pairwise terms leave a hollow one.
   - Quantum algorithms for these quantities come with both hardness and dequantization results (Lloyd, Garnerone & Zanardi 2016; Gyurik, Cade & Dunjko 2022; Berry et al. 2024).
4. **Build circuits from the extracted structure** (step 3 of the chain).
5. **Simulate them and measure:**
   - trainability, through gradient variance and the dimension of the dynamical Lie algebra (Ragone et al. 2024);
   - classical simulability (Cerezo et al. 2023).
6. **Learn the predictor** from structure to those measurements, validated by holding out whole sources (the lesson of Q2 and Q3).
7. **Extend n** where possible, so that scaling laws can be named rather than left undetermined.

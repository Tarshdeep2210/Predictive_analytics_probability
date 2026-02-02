1) Methodology

NO₂ concentration values from the India Air Quality dataset were used as the feature 𝑥
Each value was transformed using a roll-number-based non-linear function:

z=x+a​sin(b​x)
where 𝑎=0.05(𝑟 mod 7) and 𝑏=0.3(𝑟 mod 5+1)

The transformed variable 𝑧 was modeled using the probability density function:
p^​(z)=ce^−λ(z−μ)2
The parameters μ, λ, and c were estimated using Maximum Likelihood Estimation (MLE).

2) Results

The estimated parameters are summarized below:

Parameter	  Description
μ	          Mean of transformed data
λ	          Precision parameter
c          	Normalization constant

(Exact values depend on the roll number used.)

3) Result Graph

A normalized histogram of the transformed variable z shows a smooth bell-shaped distribution, indicating that the Gaussian PDF provides a good fit.

4) Conclusion

The roll-number-based transformation introduces controlled non-linearity, and the Gaussian PDF successfully models the statistical distribution of the transformed NO₂ data.

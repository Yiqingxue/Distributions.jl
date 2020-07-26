using Pkg

Pkg.status()  # display installed packages

using Distributions,StatsPlots  
# If you haven't installed the above two packages, try the following command to install
# Pkg.add("Distributions")
# Pkg.add("StatsPlots")

d=Binomial(12,.65)  # assign the Binomial distribution with n=12 trials P(S)=.65 to variable d

plot(d)

# thef following computes the probability of EXACTLY 5 successes of
# the binomial distr "d" defined early
pdf(d,5)  

# thef following computes the CUMULATIVE probability of at most 5 successes of 
# the binomial distr "d" defined early
cdf(d,5)

# define a function
f(x)=x^3+2

# evaluate the function value at 2
f(2)

# assign a vector to x (from -2 to 2, increment=0.1)
x = -2 : 0.1 : 2

# this is to plot the function. Consult ?plot for help
# Note there is dot (".") after "f"
plot(x,f.(x)) 

# Binomial distribtion

# define the function "f" with 3 inputs n, p and x
f(n,p,x)=cdf.(Binomial.(n,p),x)

x = 0.01:0.01:0.48  # x is a vector

plot(x,f(30,0.65,x),ylim=(-0.001,0.001)) #

# You may also use "p" as variable
L(p) = f(20,p,3)  # this is the same as "cdf.(Binomial.(n=20,p),x=3)" 

# for a series of "p" values
p=0.01:.01:.49  # this syntax is the same as Matlab and R

plot(p,L(p))

# add two points (p1, L(p1)) and (.1, 0.5) to the plot
p1=0.05
scatter!([(p1,L(p1)), (0.1,0.5)])



# Optimization focused papers; respective titles and abstracts 


# Learning to Solve Optimization Problems with Hard Linear Constraints

Constrained optimization problems appear in a wide variety
of challenging real-world problems, where constraints often
capture the physics of the underlying system. Classic methods
for solving these problems rely on iterative algorithms
that explore the feasible domain in the search for the best solution.
These iterative methods are often the computational
bottleneck in decision-making and adversely impact timesensitive
applications. Recently, neural approximators have
shown promise as a replacement for the iterative solvers that
can output the optimal solution in a single feed-forward providing
rapid solutions to optimization problems. However,
enforcing constraints through neural networks remains an
open challenge. This paper develops a neural approximator
that maps the inputs to an optimization problem with hard
linear constraints to a feasible solution that is nearly optimal.
Our proposed approach consists of four main steps: 1) reducing
the original problem to optimization on a set of independent
variables, 2) finding a gauge function that maps the `1-
norm unit ball to the feasible set of the reduced problem, 3)
learning a neural approximator that maps the optimization’s
inputs to an optimal point in the `1-norm unit ball, and 4)
find the values of the dependent variables from the independent
variable and recover the solution to the original problem.
We can guarantee hard feasibility through this sequence
of steps. Unlike the current learning-assisted solutions, our
method is free of parameter-tuning and removes iterations altogether.
We demonstrate the performance of our proposed
method in quadratic programming in the context of the optimal
power dispatch (critical to the resiliency of our electric
grid) and a constrained non-convex optimization in the context
of image registration problems. Our results support our
theoretical findings and demonstrate superior performance in
terms of computational time, optimality, and the feasibility of
the solution compared to existing approaches

# End-to-End Feasible Optimization Proxies for Large-Scale Economic Dispatch

The paper proposes a novel End-to-End Learning
and Repair (E2ELR) architecture for training optimization
proxies for economic dispatch problems. E2ELR combines deep
neural networks with closed-form, differentiable repair layers,
thereby integrating learning and feasibility in an end-to-end
fashion. E2ELR is also trained with self-supervised learning,
removing the need for labeled data and the solving of numerous
optimization problems offline. E2ELR is evaluated on industrysize
power grids with tens of thousands of buses using an economic
dispatch that co-optimizes energy and reserves. The results
demonstrate that the self-supervised E2ELR achieves state-ofthe-
art performance, with optimality gaps that outperform other
baselines by at least an order of magnitude.
Index Terms—Economic Dispatch, Deep Learning, Optimization
Proxies

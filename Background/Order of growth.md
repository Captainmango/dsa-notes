Can see when an algo becomes less efficient than one wiht constant time. Basically use the [[Asymptotic analysis]] as a line equation.

Low order of growth == efficeint algo

We always talk in terms of infinite input size when talking about algo efficiency. This makes it so the order of growth is more important than other factors (machine stuff etc.)

We can have quadratic algos that are faster than linear ones. Depends on number of items. Evaluate with n being infinite, but don't ignore algo speed.

Order of terms

C < log(log(n)) < log(n) < n^1/3 < n^1/2 < n < n^2 < n^3 < n^4 < 2^n < n^n

Basically constant is best and running operations that are as many steps as there are items for each item is bad (obvs, you have to intentionally code that bad.)

f1(n) = C1 log(n) + C2
f2(n) = C3 n + C4 log(log(n)) + C5

In the above, we remove the constants

f1(n) = log(n)
f2(n) = n + log(log(n))

Then we compare the leading terms. As n is worse than log(n), f2 is the worse function in terms of efficiency.

We can also cancel powers. Treat it like algebra and reduce to the simplest terms possible.

We can have multiple terms in order of growth. The above still applies.

When dealing with additive loops (i++) the complexity will be linear in arrays. this is because we need to loop the number of times in the array.

For anything multiplicative, it will be log(n). This is because the rate of change of k is slower than the change in n. In the additive example, the rate of change in n is directly linked to k and they increase proportionaly.

In examples with multiple constants (iterator var isn't 1 and another constant in the loop) we need to combine these these concepts.

```jupyter
int n = 5;
for (int i = 2; i < n; i = pow(i,2)) {
	// Some work
}

```

The above would use the following logic to work out the time complexity:
- The loop runs k-1 times
	- a^2^0, a^2^1, a^2^2 ...
	- We can simplify this to be a^2^k-1 as we know the result would be this equation (last iteration of the loop).
- We know that the number of times the loop can run cannot be more than the input size
	- a^2^k-1 < input size
- To evaluate the time complexity, we need to understand how many times the iterator var will change. This will be how many times a can be multiplied to equal the input size.
	- 2^k-1 < log a (n)
- Now we know that the iterator var multiplied by 2 will change log a (n) times. We do log 2 now to know exactly how many times the iterator will change.
	- k-1 < log 2(log a (n))

Now we know exactly how many times k will change when executing the loop.

In the above:
- a = 2
	- Our iterator var starts here. Can be 1 or any number really.
- n = 5
	- This is our input size

Working out order of growth for recursive functions is not as simple as with iterative algos. This is because the amount of work is dependent on the number of 'worlds' created when computing the result. To do this, we have to create a recurrence relation.

If an algorithm has a recursive call, we can say the time take is a function of the input size, as normal. This is how we could express a recursive fibonacci function.

T(n) = T(n-1 + n-2) + 1
T(1) = Theta(1)

If there is any constant work (base cases or single ops) these can be considered constant using Theta notation.

The recursive calls are noted as a function. As the time taken is a function of the input size and the number of sub problems, its calculation relies on the algos implementation.

[[Recursion tree method]]




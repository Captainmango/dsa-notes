We write down the amount of work done in all sub problems.

consider the recurrence relation:
T(n) = 2T(n/2) + c
T(1) = c

To solve this using the recursion tree method, we first have to express each of the sub problems in tree form:

												cn
											  /  \
									T(n/2)   T(n/2)
								/     \     /     \
						T(n/2)  T(n/2) T(n/2) T(n/2)
						
When we solve a layer, we can replace the sub problem with the result. In the case above, the result will be constant (if first order func was returned, then it would be whatever the Theta of that function is.)

												cn
											  /  \
								 	   cn/2   cn/2
								/     \     /     \
						T(n/2)  T(n/2) T(n/2) T(n/2)
						
The idea behind this is to work out the order of growth to the number of sub problems. If we use an input size (n) of 14, the depth of the recursion tree will be 4 layers, this would look like this:

												14
											  /  \
											7    7
										 / \   / \
									   3   3 3   3
									/ \  /\/\  /\
								  1   1 1111 1  1
								  
As shown above, we simply calc the product of the trees problems until it reaches the base case, in this case n = 1.

Now that we know the work being down at each sub problem, we use our normal [[Order of growth]] calculation rules to work out the time complexity. In our case here, the time complexity is n log(n). This is because the loop will run n times (simplifiying 2T(n/2) is equal to T(n)) and the work done in the loop (the recursion tree) in creases multiplicatively, so is therefor log(n) in complexity.

Again, we're looking for the total work done by the algo. This method just helps us to express it

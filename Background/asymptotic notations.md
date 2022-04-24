[[Big O notation]] - exact or upper bound on order of growth
[[Theta notation]] - exact order of growth
[[Omega notation]] - Exact or lower bound on order of growth

```jupyter

int search(int arr[], int n, int x)
{
	for (int i = 0; i < n; i++) {
		if (arr[i] == x) {
			return i;
		}
	}
	
	return -1;
}

int[] nums = {2,6,4,8};

System.out.println(search(nums, nums.length, 3));

```

This is a linear search algo. Big O allows us to say the most time a thing could take. the Big O of the above is O(n) as at worst it has to traverse the input size provided.

The Omega value desribes the best case (basically it can only get worse than this.). In the above, it could be constant (element we're looking for is at the start of the array.)

Theta describes the exact case. In the above, it isn't possible to have one.

These are ways of expressing the [[Order of growth]] mathematically. We see theta and Big O the most.


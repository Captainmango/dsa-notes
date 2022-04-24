Loops add time complexity. try and find a pattern or formula to make things as simple as possible.

```jupyter

int i = 123;

int calcNaturalNumsOne(int num)
{
	int output = 0;
	for (int i = 1; i <= num; i++) {
		output += i;
	}
	
	return output;
}

System.out.println(calcNaturalNums(i));

```

Loops are always at least (n) time complexity (number of elements in iterable). Finding a formula or relationship simplifies this.

```jupyter

int i = 123;

int calcNaturalNumsTwo(int num)
{
	return (num * (num + 1)) / 2;
}

System.out.println(calcNaturalNums(i));

```

System load can affect time complexity. We use [[Asymptotic analysis]] to rate algorithms.

We divide efficiency cases for algos into:
- best - lowest complexity (can't really be used as it's not realistic)
- worst - highest complexity (Should be used as we need to know the limitations)
- average - the most common case's complexity (not typically done as we need to make assumptions on input size)

We differentiate [[Order of growth]] of algos using these cases.

If there are complex conditions or operations, look for the actual work of the function. Base cases are always constant.
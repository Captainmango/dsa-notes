This is my solution to the following:
> Given two arrays, create a function that lets a user know if the two arrays contain any common items.


```jupyter

boolean findCommonItem(List<String> a, List<String> b)
{
	// Get stuff into a Set for reference
	Set<String> listOne = new HashSet<>(a);
	
	// Compare iteratively against the Set
	for (String item : b) {
		if listOne.contains(item) {
			return true;
		}
	}
	
	// Base case is false
	return false;
}

List<String> listOne = List.of("a", "b", "c");
List<String> listTwo = List.of("5", "d", "g");

System.out.println(findCommonItem(listOne, listTwo));

```

thinking about optimal work here was crucial. The brute force approach would work, but scales horribly. This linear solution is the best I could think of really. Due to having 2 lists, we need to compare against one of them. Using a Set IMO makes this simpler as it removes duplicates (question doesn't say there can't be dups).

Could be worth sticking both in Sets and finding intersection. I tried this and the implementation without helper libraries is still linear time.

[[Cheeky Big O cheat sheet]]
[[Cheeky interview cheat sheet]]
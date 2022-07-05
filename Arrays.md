## Arrays

Make them using square brackets

Insert and delete are linear time. look up (with index) and push (add item to end) are constant time

shift removes at start of the array. Unshift adds to the start of an array. Both are linear time as they iterate indexes

static arrays cannot be changed after initisalising. These are good for memory. But can be tricky to manage.

Dynamic arrays copy static and increase size (normally doubling)

When working with 2 arrays at once, think about them cooperating to minimise work. Comparing items to see who wins is a good strat

Sort arrays first. While it adds complexity, it manages memory better and simplifies consequent work.
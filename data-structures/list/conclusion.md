---
description: So, which one is better between ArrayList and LinkedList
---

# Conclusion

To choose the better implementation of list, it's depends. Yup it's depends on case of problem that we want to solve. One of the best considerations is complexity.

### Time Complexity&#x20;

<table><thead><tr><th width="145">Operations</th><th width="132">ArrayList</th><th width="128">LinkedList</th><th>Description</th></tr></thead><tbody><tr><td>Add Element</td><td><code>O(1)</code> or <code>O(n)</code></td><td><code>O(1)</code></td><td>ArrayList only need <code>O(1)</code> time complexity if current array size is enough. If array is not enough, time complexity can be <code>O(n)</code> because need operation to copy all of elements in existing array.<br><br>LinkedList need <code>O(1)</code> time complexity because LinkedList just need to connect new node with last node (which is in Java, last node is saved in variable <code>last</code>)</td></tr><tr><td>Access Element</td><td><code>O(1)</code></td><td><code>O(n)</code></td><td>ArrayList basically using array so to access element with index, it's just need <code>O(1)</code> complexity<br><br>To access element in LinkedList, program need to iterate all of nodes from the first until the target node</td></tr><tr><td>Update Element</td><td><code>O(1)</code></td><td><code>O(n)</code></td><td>ArrayList just need access element that need update using index<br><br>LinkedList also need iterate all of nodes from the start until the target node</td></tr><tr><td>Delete Element</td><td><code>O(n)</code></td><td><code>O(n)</code></td><td>ArrayList need to shift elements behind deleted element to the left<br><br>LinkedList also need iterate all of nodes from the start until the target node</td></tr></tbody></table>

So after we know about the complexity of both of implementations (ArrayList and LinkedList), you just need to know what kind operation that will be you use more frequently. But in my opinion, we better to use `LinkedList` only if these 2 conditions are met :&#x20;

* We use add operation more frequently than access or update element in the random index position
* And we don't have a clear range of the list size

Besides that 2 conditions above, IMO better to use `ArrayList` instead, what do you think?

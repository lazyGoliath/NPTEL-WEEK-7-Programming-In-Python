# Week 7 Quiz

## All questions carry equal weightage. All Python code is assumed to be executed using Python3. You may submit as many times as you like within the deadline. Your final submission will be graded.

# Note:

- If the question asks about a value of type string, remember to enclose your answer in single or double quotes.
- If the question asks about a value of type list, remember to enclose your answer in square brackets and use commas to separate list items.

## Given the following permutation of a,b,c,d,e,f,g,h,i,j, what is the next permutation in lexicographic (dictionary) order? Write your answer without any blank spaces between letters.

```bash
 fjadbihgec

```

### Answer : ```fjadcbeghi```

Feedback:

The prefix to change is bihgec. This becomes cbeghi

Accepted Answers:

(Type: Regex Match) [ ]*fjadcbeghi[ ]*
(Type: Regex Match) [ ]*\"fjadcbeghi\"[ ]*
(Type: Regex Match) [ ]*\'fjadcbeghi\'[ ]*


## We want to add a function length() to the class Node that implements user defined lists which will compute the length of a list. An incomplete implementation of length() given below. You have to provide expressions to put in place of XXX, YYY. and ZZZ.

```bash
def length(self):
  if self.value == None:
     return(XXX)
  elif self.next == None:
     return(YYY)
  else:
     return(ZZZ)
```

 - XXX: 0, YYY: 0, ZZZ: self.next.length()
 - XXX: 0, YYY: 0, ZZZ: 1 + self.next.length()
 - XXX: 0, YYY: 1, ZZZ: self.next.length()
 - XXX: 0, YYY: 1, ZZZ: 1 + self.next.length() (correct)

Feedback:

Inductive definition: if empty, return 0, if singleton return 1, else add 1 to 
the length of the list starting at self.next.

Accepted Answers:

XXX: 0, YYY: 1, ZZZ: 1 + self.next.length()

## Suppose we add this function foo() to the class Tree that implements search trees. For a name mytree with a value of type Tree, what would mytree.foo() compute?

```bash
def foo(self):
        if self.isempty():
            return(0)
        elif self.isleaf():
            return(1)
        else:
            return(self.left.foo() + self.right.foo()))
```

## The function f(n) given above returns True for a positive number n if and only if:

 - The number of nodes in mytree
 - The largest value in mytree.
 - The length of the longest path from root to leaf in mytree.
 - The number of leaves in mytree. (correct)

Feedback:
This computes the number of leaves in the tree. An empty tree has no leaves. A tree with just one node has a single leaf. Otherwise, compute the number of leaves in left and right subtrees and add them.

This does not compute the number of nodes in the tree. For that, we need to add 1 in the inductive case, to account for the current node. So the else: expression would be return(1 + self.left.foo() + self.right.foo()).

Accepted Answers:

The number of leaves in mytree.

## Inorder traversal of a binary tree has been defined in the lectures. A preorder traversal lists the vertices of a binary tree (not necessarily a search tree) as follows:

 * Print the root.
 * Print the left subtree in preorder.
 * Print the right subtree in preorder.

## Suppose we have a binary tree with 10 nodes labelled a, b, c, d, e, f, g, h, i, j, with preorder traversal gbhecidajf and inorder traversal ehbicgjafd. What is the right child of the root node?

### Answer : ```d```

Feedback:

From the preorder traversal, g is the root. The inorder traversal tells us that jafd lie to the right of the root. The preorder traversal of this segment says d is the root of this subtree, so d is the right child of the root.

Accepted Answers:

(Type: Regex Match) [ ]*d[ ]*
(Type: Regex Match) [ ]*"d"[ ]*
(Type: Regex Match) [ ]*'d'[ ]*

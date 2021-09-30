# Stack-in-c++
Stack is basically a container which work on LIFO Principle i.e last in first out.
Now what is LIFO Principle-
it means that the element which is added in the last will be deleted first.
let's take an example.
suppose we have elements 1,4,5,9,15 and we have to push these into stack.
                                   |____|
                                   |_15_|
                                   |__9_|
                                   |__5_|
                                   |__4_|
                                   |__1_|   Stack will look like this.
  Now when we will apply deletion operation firstly 15 will be deleted.
                                   |____|
                                   |__9_|
                                   |__5_|
                                   |__4_|
                                   |__1_|  And stack will look like this.
  Stack Syntax:-

For creating  a stack, <stack> header file is used in our code. We then use this syntax to define the std::stack:

template <class Type, class Container = deque<Type> > class stack;
 Type – is the Type of element contained in the std::stack such as int,float e.t.c.
Container – is the Type of underlying container object.
  The functions associated with stack are: 
empty() – Returns whether the stack is empty – Time Complexity : O(1) 
size() – Returns the size of the stack – Time Complexity : O(1) 
top() – Returns a reference to the top most element of the stack – Time Complexity : O(1) 
push(g) – Adds the element ‘g’ at the top of the stack – Time Complexity : O(1) 
pop() – Deletes the top most element of the stack – Time Complexity : O(1) 
  
  Code:-
  #include <iostream>
#include <stack>
using namespace std;
int main() {
	stack<int> stack;
	stack.push(1);
	stack.push(4);
	stack.push(5);
	stack.push(9);
	stack.push(15);
		stack.pop();
	stack.pop();

	while (!stack.empty()) {
		cout << ' ' << stack.top();
		stack.pop();
	}
}

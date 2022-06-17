/*
    Time Complexity: O(N) 
    Space Complexity:O(N) 

    Where 'N' is the no. of operations performed.
*/

class minStack
{
	stack<int> Stack, Min;
	
	public:
		
		// Constructor
		minStack() { }
		
		// Function to add another element equal to num at the top of stack.
		void push(int num)
		{
			Stack.push(num);
			if(Min.empty() || Min.top() >= num){
				Min.push(num);
			}
		}
		
		// Function to remove the top element of the stack.
		int pop()
		{
			if(!Min.empty() && Min.top() == Stack.top()) {
				Min.pop();
			}

			int ret = -1;

			if(!Stack.empty()) {
				ret = Stack.top();
				Stack.pop();
			}

			return ret;
		}
		
		// Function to return the top element of stack if it is present. Otherwise return -1.
		int top()
		{
			int ret = -1;
			if(!Stack.empty()){
				ret = Stack.top();
			}
			return ret;
		}
		
		// Function to return minimum element of stack if it is present. Otherwise return -1.
		int getMin()
		{
			int ret = -1;
			if(!Min.empty()) {
				ret = Min.top();
			}
			return ret;
		}
};

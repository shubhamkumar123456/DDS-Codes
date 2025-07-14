#include<iostream>
#include<cctype>
using namespace std;
#define size 100
char stack[size];
int top = -1;

void push(char c){
    top++;
    stack[top] = c;
}

char pop(){
    char ch = stack[top];
    top--;
    return ch;
}
                    // 52+83-*\0
int evaluatePostfix(char arr[]){
        int i=0;
        while(arr[i]!='\0'){
            char c = arr[i];
            if(isalnum(c)){
                push(c -'0');
            }
            else if(c=='+'|| c=='-'|| c=='*'|| c=='/'|| c== '^'){
                int b = pop();
                int a = pop();

                switch(c){
                    case '+':
                    push(b+a);
                    break;

                    case '-':
                    push(b-a);
                    break;

                    case '*':
                    push(b*a);
                    break;

                    case '/':
                    push(b/a);
                    break;

                    case '^':
                    push(b^a);
                }
            }
            i++;
        }
        return pop();
}
int main(){
    char postfix[size];
    cout<<"enter a expression : ";
    cin>>postfix;

  int ans = evaluatePostfix(postfix);
  cout<<ans;
}

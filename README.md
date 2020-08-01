
#include <bits/stdc++.h>
  using namespace std;
  
  int main()
  {
    
    int n;
    cin>>n;
    int arr[n];
    int temp;
    int front=-1;
    int rear=-1;
    int queue[n];
    for(int i=0;i<n;i++)
    {
     cin>>arr[i];
     rear=(rear+1)%n;
     if(front==rear)
     {
       break;
     }
     queue[rear]=arr[i];
       if(front==-1)
       {
         front=rear;
       }
    }
    for(int i=0;i<n;i++)
    {
      for(int j=0;j<=i;j++)
      {
        cout<<queue[j]<<" ";
      }
      cout<<endl;
    }
    for(int i=0;i<n-1;i++)
    {
      if(front==-1)
      {
        break;
      }
      if(front==rear)
      {
        front=rear=-1;
      }
      else{
        front=(front+1)%n;
      }
      for(int j=front;j<n;j++)
      {
        cout<<queue[j]<<" ";
      }
      cout<<endl;
    }
    return 0;
  }

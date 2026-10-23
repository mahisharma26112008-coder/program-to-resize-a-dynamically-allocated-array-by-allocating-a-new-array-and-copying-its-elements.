# program-to-resize-a-dynamically-allocated-array-by-allocating-a-new-array-and-copying-its-elements.

#include<iostream>
  using namespace std;
 int main(){
     int n,newsize;
     cout<<"enter size :"<<"\n";
     cin>>n;

     int *p= new int[n];
     for(int i=0;i<n;i++){
         cin>>p[i];
     }

     cout<<"enter new size "<<"\n";
     cin>>newsize;
     
     int *q=new int[newsize];

     for(int i=0;i<n && i<newsize ; i++){
         q[i]=p[i];
         }

     delete[] p;
     p=q;
cout<<"new array elements:"<<"\n";
     for(int i=0;i<newsize;i++){
         if(i<n){
             cout<<p[i]<<"\n";
         }
         else{
             cout<<"0";
         }
     }
         delete[] p;

         return 0;
     }

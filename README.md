#include <iostream>
using namespace std;
void dele(int a[],int n,int element){
    
    int pos;
    for(int i=0; i<n; i++){
        if(a[i]==element){
            pos=i;
            break;
        }
    }
    a[pos]=0;
    for(int i=pos; i<n-1; i++){
        a[i]=a[i+1];
    }
    for(int i=0; i<n-1; i++){
        cout<<a[i]<<" ";
    }
}

int main() {
    int a[]={1,2,3,4,5,6,7,8,9,12};
    int n=sizeof(a)/sizeof(a[0]);
    dele(a,n,7);
   

    return 0;
}

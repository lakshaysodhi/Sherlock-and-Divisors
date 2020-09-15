# Sherlock-and-Divisors
#include <bits/stdc++.h>
using namespace std;
#define ull unsigned long long
#define ll long long
#define ld long double


int main() {

    int t;
    cin>>t;
    while(t--){
        ll n;
        cin>>n;
        ll count=0;
        for(ll i=1;i<=sqrt(n);i++){//one sqrt(n)*sqrt(n)=n so 1 root is always going to be less than or equal to sqrt(n) so from that one we will calculate the other one without iterating
            if(n%i==0 && i%2==0) count++;
            if(n%i==0){//if i is a divisor then the second divisor will be n/i which is beyond sqrt(n)
            if((n/i)%2==0 && (n/i)!=i){
                count++;
            }
        }
        }
        cout<<count<<endl;
    }


}






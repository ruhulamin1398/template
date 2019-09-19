# template#include<bits/stdc++.h>
using namespace std;
#define ll              long long int
#define c(n)            scanf("%lld",&n)
#define c2(a,b)         scanf("%lld%lld",&a,&b)

#define pl(n)            printf("%lld\n",n)
#define pls(n)           printf("%s\n",n)
#define pl2(a,b)         printf("%lld %lld\n",a,b)

#define p(n)            printf("%lld",n)
#define ps(n)           printf("%s",n)
#define p2(a,b)         printf("%lld %lld",a,b)

#define carray(n,arr)   for( ll i =1 ; i<=n ; i++)scanf("%lld",arr+i)
#define loop(n)         while (n--)
#define tcase()         ll tc;scanf("%lld",&tc);for( ll t = 1; t<=tc ; t++)
#define MAX             250002






int main() {
    tcase() {
        ll n ;
        cin>>n ;
        multiset<ll> dq;
        multiset<ll> ::iterator it ;



        for( ll i=0 ; i<n ; i++) {
            int a;
            cin>>a;
            dq.insert(a);
        }


        it=dq.begin();
        int a = *(it);

        while(a<2048 and !dq.empty()) {
            it=dq.begin();
            a = *(it);
     //       cout<<a<<" ";
            dq.erase(it);


            if( a== *(dq.begin()) ) {
                it=dq.begin();
                dq.erase(it);
                dq.insert((a+a));
            }


        }


        if(a==2048)
            cout<<"YES"<<endl;
        else
            cout<<"NO"<<endl;


//
//for (it=dq.begin(); it!=dq.end(); ++it)
//    std::cout << ' ' << *it;






    }


    return 0;
}

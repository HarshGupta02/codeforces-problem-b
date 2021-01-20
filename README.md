    #include<iostream>
    #include<set>
    #include<vector>
    #include<string>
    #include<cmath>
    #include<algorithm>
    #include<string>
    #include<cstdlib>
    #include<math.h>
    #include<stack>
    #include<map>
    #include<iterator>
    #include<string.h>
    #include<unordered_map>
    #include<limits>
    using namespace std;
    #define ll long long int
    #define MOD 1000000007

    const int N=1e5+5;

    #define SIEVE
    int primes[N];
    vector<int>v;
    void sieve() 
    {
        for (int i = 2; i <N; ++i)
        {
            if(primes[i]==0)
            {
                v.push_back(i);
                for (int j = i*i; j <N ; j+=i)
                {
                    primes[j]=1;
                    
                }
            }
            primes[i]^=1;

        }
    }
    void solve()
    {
        int d;
        cin>>d;
        int x=*upper_bound(v.begin(),v.end(),d);
        int y=*upper_bound(v.begin(),v.end(),x+d-1);
        cout<<x*y<<endl;
    }
    signed main()
    {
           ios_base::sync_with_stdio(false);
           cin.tie(0);
           cout.tie(0);

           #ifndef ONLINE_JUDGE
             freopen("inputs.txt","r",stdin);
             freopen("output2.txt","w",stdout);
           #endif

            #ifdef SIEVE  
                sieve();
            #endif 

             int t=1;
             cin>>t;
             while(t--)
                 {
                    solve();
                 }

             return 0;
    }


           




           









          

































            








           

  
        


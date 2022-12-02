# Clock



#include<bits/stdc++.h>
using namespace std;
int main()
{
int t;
cin>>t;
while(t--){int n,co=0,ro=0,go=0;
string s,p;
cin>>s;

cin>>n;
s.erase(2,1);
p=s;
if(s[0]==s[3]&&s[1]==s[2])ro++;
while(true){
    co++;
    if(s[3]=='9'){
        s[3]='0';
        (int)s[2]++;
        if(s[2]=='6'){
            s[2]='0';
            if(s[1]=='9'){s[1]='0';
            (int)s[0]++;
            
            }
            else 
            (int)s[1]++;
            if(s[0]=='2'&& s[1]=='4'&& s[2]=='0'&&s[3]=='0'){
                s[0]='0';
                s[1]='0';
                s[2]='0';
                s[3]='0';
            }

        }

    }
    else{
        (int)s[3]++;
    }
    if(co==n){
         if(s==p)break;
    if(s[0]==s[3]&&s[1]==s[2]){
       ro++;   
    }
      if(s==p)break;
    co=0;
    
    }
    
    
}

cout<<ro<<endl;

}
 return 0;
}

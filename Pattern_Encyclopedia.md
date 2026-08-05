void solve(){
string s;cin>>s;
int t1=0;
int t2=0;
for(int i=0;i<s.size();i++){
    if(s[i]=='0'){
        t1++;
        if(t1%2==0){
         cout<<3<<" "<<1<<endl;
        }
        else{
           cout<<1<<" "<<1<<endl;  
        }
    }
    else{
          t2++;
        if(t2%2!=0){
         cout<<4<<" "<<3<<endl;
        }
        else{
           cout<<4<<" "<<1<<endl;  
        }
    }
}
 
 
 
}

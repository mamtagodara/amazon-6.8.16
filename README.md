# amazon-6.8.16
#include <iostream>
#include<bits/stdc++.h>
using namespace std;

int main() {
    multiset<int>s;
    int a[26]={0},k;
    string st;
    cin>>st>>k;
    for(int i=0;i<st.length();i++)
    {
        a[st[i]-'a']++;
    }
    for(int i=0;i<26;i++)
    {
        if(a[i]!=0)
       s.insert(a[i]);
    //cout<<a[i]<<"\n";
    }
    //set<int>::reverse_iterator itt;
    for(int i=0;i<k;i++)
    {
        int t=*s.rbegin();
        cout<<"p"<<t<<" ";
        auto y=s.find(t);
        s.erase(y);
        t--;
        s.insert(t);
    }
    int sum=0;
    for(set<int>::iterator it=s.begin();it!=s.end();it++)
    {
        cout<<*it<<" ";
        sum+=(*it)*(*it);
        
    }
    cout<<sum;
	//code
	return 0;
}

#include <iostream>
#include <vector>
using namespace std;

struct st
{
    string s;
    int i;
};

string poc(string s)
{
    st t;
    vector<st> st;
    t.s=s;
    t.i=0;
    st.push_back(t);
    while(st[st.size()-1].s[st[st.size()-1].s.find(')')+1]!='.')
    {   //ha az utolsó elem szövegében van ( vagy )
        if(st[st.size()-1].s.find('(')<st[st.size()-1].s.size() or st[st.size()-1].s.find(')')<st[st.size()-1].s.size()){
            if(st[st.size()-1].s.find('(')<st[st.size()-1].s.find(')'))
        {
            t.i++;
            t.s=st[st.size()-1].s.substr(st[st.size()-1].s.find('(')+1,st[st.size()-1].s.size()-st[st.size()-1].s.find('(')-1);
            st.push_back(t);
        }
        else
        {
            t.i--;
            t.s=st[st.size()-1].s.substr(st[st.size()-1].s.find(')')+1,st[st.size()-1].s.size()-st[st.size()-1].s.find(')')-1);
            st.push_back(t);
        }}

    }
    for(int i=st.size()-1;i>=0;i--)
      {
            if(st[i].i+1==st[st.size()-1].i )
            {
                s=st[i].s.substr(st[i].s.find('(')+1,st[i].s.find(").")-(st[i].s.find('(')+1));
            }
        }
return s;
}
string af(string s)
{//eseteket vizsgálni mikor alap függvény inverze és testvérei (pl arch meg ilyenek
    if(s.find("sin")<s.size()
        or (s.find("cos")<s.size())
        or (s.find("^")<s.size())
        or (s.find("ln")<s.size())
        or (s.find("log")<s.size())
        or (s.find("tg")<s.size())
        or (s.find("ctg")<s.size())
        or (s.find("sh")<s.size())
        or (s.find("ch")<s.size())
        or (s.find("th")<s.size()))
        {

        }
}
int main()
{
    string s="(1)*(2)*(3(4(5(6(7(8)9(10)11)12)sin(x-1).13)14)*(15)*(16)";//
    cout<<af(s);

    return 0;
}

#include<bits/stdc++.h>

struct node

{

int u,v,wt;

node(int first,int second,int weight)

{

 u=first;

 v=second;

 wt=weight;

}

};

int bellmonFord(int n, int m, int src, int dest, vector<vector<int>> &edges) {

   vector<node> edge;

for(auto it:edges)

{

 edge.push_back(node(it[0],it[1],it[2]));

}

int inf=1000000000;

vector<int> dist(n+1,inf);

dist[src]=0;

for(int i=1;i<=n-1;i++)

{

 for(auto it:edge)

 {

  if(dist[it.u]!=1000000000 and dist[it.u]+it.wt<dist[it.v])

  {

     dist[it.v]=dist[it.u]+it.wt;

  }

 }

}

return dist[dest];

}

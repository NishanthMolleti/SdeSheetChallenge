vector<int> dijkstra(vector<vector<int>> &vec, int vertices, int edges, int source) {
    // Write your code here.
    vector<pair<int,int>> adj[vertices];
    for(int i=0;i<edges;i++){
       adj[vec[i][0]].push_back({vec[i][1],vec[i][2]});
       adj[vec[i][1]].push_back({vec[i][0],vec[i][2]});
    }
    priority_queue<pair<int,int>> pq;
    pq.push({0,source});
    vector<int> dist(vertices,INT_MAX);
    dist[source] = 0;
    while(!pq.empty()){
        int node = pq.top().second;
        int d = pq.top().first * -1;
        pq.pop();
        
        if(dist[node] != d) continue;
            
        for(auto it: adj[node]){
            if(it.second + d < dist[it.first]){
                dist[it.first] = it.second + d;
                pq.push({dist[it.first]*-1, it.first});
            }
        }
    }
    return dist;
}

#include <bits/stdc++.h>

vector<int> topologicalSort(vector<vector<int>> &edges, int v, int e)  {
    vector<int> indegree(v, 0);
    vector<int> adj[v];
    for(auto x: edges){
          adj[x[0]].push_back(x[1]);
    }
    
    // store the indegree of each vertices.
    for(int i = 0; i < v; i++){
        for(auto x: adj[i]) indegree[x]++;
    }
    queue<int> q;
    vector<int> topoSort;
    // add all vecrtices with indegree as zero in queue
    for(int i = 0; i < v; i++){
        if(indegree[i] == 0)
            q.push(i);
    }
    
    while(!q.empty()){
        int u = q.front();
        q.pop();
        topoSort.push_back(u);
        // for every adjacent node of u
        for(int x: adj[u]){
            // reduce the indegree of node by 1
            // if indegree becomes 0 add node to queue
            if(--indegree[x] == 0)
                q.push(x);
        }
    }
    return topoSort;
}

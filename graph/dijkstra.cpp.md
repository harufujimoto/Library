---
data:
  _extendedDependsOn: []
  _extendedRequiredBy: []
  _extendedVerifiedWith: []
  _isVerificationFailed: false
  _pathExtension: cpp
  _verificationStatusIcon: ':warning:'
  attributes:
    links: []
  bundledCode: "#line 1 \"graph/dijkstra.cpp\"\ntemplate<class T> struct Dijkstra{\n\
    \  #define INF (numeric_limits<T>::max()/2)\n  using P = pair<T,int>;\n  Graph<T>\
    \ G;\n  vector<T> d;\n  vector<int> prev;\n  Dijkstra(Graph<T>& G):G(G){}\n  void\
    \ solve(int s){\n    d.assign(G.n,INF);\n    prev.assign(G.n,-1);\n    d[s] =\
    \ 0;\n    priority_queue<P,vector<P>,greater<P> > que;\n    que.push(P(0,s));\n\
    \    while(que.size()){\n      P p = que.top();que.pop();\n      int v = p.second;\n\
    \      if(d[v] < p.first) continue;\n      for(int i = 0;i < G[v].size();i++){\n\
    \        Edge<T>& e = G[v][i];\n        if(d[e.to] > d[v] + e.cost){\n       \
    \   d[e.to] = d[v] + e.cost;\n          prev[e.to] = v;\n          que.push(P(d[e.to]\
    \ , e.to));\n        }\n      }\n    }\n  }\n  bool reachable(int t){\n    return\
    \ d[t] != INF;\n  }\n  vector<int> get_path(int t){\n    vector<int> path;\n \
    \   for(;t != -1;t = prev[t]){ path.push_back(t); }\n    reverse(path.begin(),path.end());\n\
    \    return path;\n  }\n  T& operator[](int i){return d[i];}\n};\n"
  code: "template<class T> struct Dijkstra{\n  #define INF (numeric_limits<T>::max()/2)\n\
    \  using P = pair<T,int>;\n  Graph<T> G;\n  vector<T> d;\n  vector<int> prev;\n\
    \  Dijkstra(Graph<T>& G):G(G){}\n  void solve(int s){\n    d.assign(G.n,INF);\n\
    \    prev.assign(G.n,-1);\n    d[s] = 0;\n    priority_queue<P,vector<P>,greater<P>\
    \ > que;\n    que.push(P(0,s));\n    while(que.size()){\n      P p = que.top();que.pop();\n\
    \      int v = p.second;\n      if(d[v] < p.first) continue;\n      for(int i\
    \ = 0;i < G[v].size();i++){\n        Edge<T>& e = G[v][i];\n        if(d[e.to]\
    \ > d[v] + e.cost){\n          d[e.to] = d[v] + e.cost;\n          prev[e.to]\
    \ = v;\n          que.push(P(d[e.to] , e.to));\n        }\n      }\n    }\n  }\n\
    \  bool reachable(int t){\n    return d[t] != INF;\n  }\n  vector<int> get_path(int\
    \ t){\n    vector<int> path;\n    for(;t != -1;t = prev[t]){ path.push_back(t);\
    \ }\n    reverse(path.begin(),path.end());\n    return path;\n  }\n  T& operator[](int\
    \ i){return d[i];}\n};"
  dependsOn: []
  isVerificationFile: false
  path: graph/dijkstra.cpp
  requiredBy: []
  timestamp: '2021-05-04 22:44:16+09:00'
  verificationStatus: LIBRARY_NO_TESTS
  verifiedWith: []
documentation_of: graph/dijkstra.cpp
layout: document
redirect_from:
- /library/graph/dijkstra.cpp
- /library/graph/dijkstra.cpp.html
title: graph/dijkstra.cpp
---

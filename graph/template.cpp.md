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
  bundledCode: "#line 1 \"graph/template.cpp\"\ntemplate<class T> struct Edge{\n \
    \ int from,to,id; T cost;\n  Edge(int from,int to,T cost):from(from),to(to),cost(cost){}\n\
    \  Edge(int from,int to,int id,T cost):from(from),to(to),id(id),cost(cost){}\n\
    \  Edge(){}\n};\ntemplate<class T> struct Graph{\n  int n;\n  vector<vector<Edge<T>>>\
    \ g;\n  Graph(int n):n(n){ g.resize(n); }\n  void add_edge(int from,int to){ g[from].emplace_back(from,to,1);\
    \ }\n  void add_edge(int from,int to,T cost){ g[from].emplace_back(from,to,cost);\
    \ }\n  vector<Edge<T>>& operator[](int i){ return g[i]; }\n};\n"
  code: "template<class T> struct Edge{\n  int from,to,id; T cost;\n  Edge(int from,int\
    \ to,T cost):from(from),to(to),cost(cost){}\n  Edge(int from,int to,int id,T cost):from(from),to(to),id(id),cost(cost){}\n\
    \  Edge(){}\n};\ntemplate<class T> struct Graph{\n  int n;\n  vector<vector<Edge<T>>>\
    \ g;\n  Graph(int n):n(n){ g.resize(n); }\n  void add_edge(int from,int to){ g[from].emplace_back(from,to,1);\
    \ }\n  void add_edge(int from,int to,T cost){ g[from].emplace_back(from,to,cost);\
    \ }\n  vector<Edge<T>>& operator[](int i){ return g[i]; }\n};\n"
  dependsOn: []
  isVerificationFile: false
  path: graph/template.cpp
  requiredBy: []
  timestamp: '2021-05-04 22:44:16+09:00'
  verificationStatus: LIBRARY_NO_TESTS
  verifiedWith: []
documentation_of: graph/template.cpp
layout: document
redirect_from:
- /library/graph/template.cpp
- /library/graph/template.cpp.html
title: graph/template.cpp
---

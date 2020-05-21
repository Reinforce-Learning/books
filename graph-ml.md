---
description: cs224w
---

# 图机器学习

## Introduction of structure of Graphs

### Two Types of Networks/Graphs

* Natural Network
* Information Graphs

### Different Types of Graphs

![Different Types of Graphs From cs224w](.gitbook/assets/image%20%283%29.png)

### Network and Application

1. Predict the type/color of a given node
   * Node classification
2. Predict whether two nodes are linked
   * Link prediction
3. Identify densely linked clusters of nodes
   * Community detection
4. Measure similarity of two nodes/networks
   * Network similarity

### Structure of Graphs

![Component of a Network](.gitbook/assets/image%20%282%29.png)

### Choice of Network Representation

1. Directed and Undirected and degrees

![Node degrees](.gitbook/assets/image%20%284%29.png)

2. Complete Graph

N个节点的无向图最大边数为：

$$
E_{\max }=\left(\begin{array}{c}N \\ 2\end{array}\right)=\frac{N(N-1)}{2}
$$

$$
E=E_{max} \text{ 是完全图，它的平均度为：} N-1
$$

3. Adjacency Matrix\(邻接矩阵\)

邻接矩阵是很稀疏的。

对于有向图，出度是邻接矩阵的行和，入度是列和。

4. 更多图的类型

![More Type of Graphs](.gitbook/assets/image%20%285%29.png)

5. 图的连通性

连通图：每个顶点都可以被连通。

非连通图：由两个或者更多连通的component组成，其中最大的component 叫做Giant Componet。独立的点叫做isolated node。

通过邻接矩阵判定图的连通性

![](.gitbook/assets/image%20%286%29.png)

 

## Network Properties: 怎么去衡量网络

### Degree Distribution

$$
P(k)=N_k/N
$$

$$
N_k \text{指带有degree的Nodes}
$$

### Path in Graphs

#### 图的访问路径

![ACBDCDEG](.gitbook/assets/image%20%289%29.png)

#### 图的距离表示

若节点不可达，则距离为无限大♾

#### 网络直径\(Network Diameter\)

$$
\bar{h}=\frac{1}{2 E_{\max }} \sum_{i, j \neq i} h_{i j} \\
h_{ij} \text{是node i 到node j的距离} \\
E_{max} =\frac{n(n-1)}{2}  \text{是最大边数}\\
$$

#### 集群系数\(clustering coefficient\)

![Clustering Coefficient](.gitbook/assets/image%20%287%29.png)

$$
\begin{array}{l}C_{i} \in[0,1] \\ C_{i}=\frac{2 e_{i}}{k_{i}\left(k_{i}-1\right)} \quad \begin{array}{l}\text { where } e_{i} \text { is the number of edges } \\ \text { between the neighbors of node } i\end{array}\end{array}
$$

以图二为例：

$$
C_i = \frac{3 \times 2}{4 \times 3 } = 0.5 \\
e_i\text{为3，}k_i\text{为4}
$$

平均集群系数\(Average clustering coefficient\):



$$
C=\frac{1}{N} \sum_{i}^{N} C_{i}
$$

![&#x66F4;&#x591A;&#x4F8B;&#x5B50;](.gitbook/assets/image%20%288%29.png)

#### 连接性\(Connectivity\)




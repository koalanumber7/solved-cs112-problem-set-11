Download Link: https://assignmentchef.com/product/solved-cs112-problem-set-11
<br>
<strong>Problem Set 11</strong>

<strong>Graphs: Representation, Traversal</strong>

<ol>

 <li>Suppose a weighted undirected graph has <em>n</em> vertices and <em>e</em> The weights are all integers. Assume that the space needed to store an integer is the same as the space needed to store an object reference, both equal to one unit. <em>What is the minimum value of e</em> for which the adjacency matrix representation would require less space than the adjacency linked lists representation? Ignore the space needed to store vertex labels.</li>

 <li>The complement of an <strong>undirected</strong> graph, <strong>G</strong>, is a graph <strong>GC</strong> such that:</li>

</ol>

<strong>GC</strong> has the same set of vertices as <strong>G</strong>

For every edge <em>(i,j)</em> in <strong>G</strong>, there is no edge <em>(i,j)</em> in <strong>GC</strong>

For every pair of vertices <em>p</em> and <em>q</em> in <strong>G</strong> for which there is no edge <em>(p,q)</em>, there is an edge <em>(p,q)</em> in <strong>GC</strong>.

Implement a method that would return the complement of the <strong>undirected</strong> graph on which this method is applied.

class Edge {        int vnum;        Edge next;

}

public class Graph {

Edge[] adjlists;  // adjacency linked lists

…

public Graph complement() {           // FILL IN THIS METHOD

…

}     }

What would be the worst case running time (big O) of an implementation for a graph with <em>n</em> vertices and <em>e</em> edges?

This graph has <em>n+2</em> vertices and 2<em>n</em> edges. For every vertex labeled <em>i</em>, <em>1 &lt;= i &lt;= n</em>, there is an edge from <em>S</em> to <em>i</em>, and an edge from <em>i</em> to <em>T</em>.

<ol>

 <li>How many different depth-first search sequences are possible if the start vertex is <em>S</em>?</li>

 <li>How many different breadth-first search sequences are possible if the start vertex is <em>S</em>?</li>

 <li><strong>*</strong> You can use DFS to check if there is a path from one vertex to another in a directed graph.</li>

</ol>

Implement the method <strong>hasPath</strong> in the following. Use additional class fields/helper methods as needed:

public class Neighbor {       public int vertex;       public Neighbor next;

…

}

public class Graph {

Neighbor[] adjLists;  // adjacency linked lists for all vertices

// returns true if there is a path from v to w, false otherwise       public boolean hasPath(int v, int w) {         // FILL IN THIS METHOD

…

}

}
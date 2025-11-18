Discussion: Centrality and Community Structure

Based on the algorithm's output, two nodes consistently remain central,
but their metrics dramatically illustrate how community structure defines centrality.

Consistently Central Nodes: The faction leaders, Node 0 (Mr. Hi) and Node 33 (the Admin),
remain the most central figures within their respective partitions throughout the algorithm.
In the initial iterations (like Iteration 0, the full graph), they are global hubs.
After the first major split, Node 0 becomes the central hub of its new subgraph
(the "Mr. Hi" faction), and Node 33 becomes the hub of the "Admin" faction.

Influence of Community Structure: This analysis perfectly demonstrates that centrality is a
local and relative property, not a global, static one. This is visualized in the
"jagged" evolution plots:

    - Metrics are Context-Dependent: A node's metrics are only plotted when the
      community it belongs to is being processed. The "gaps" in the lines mean
      the node was in a "final" or "queued" community, not the one currently
      being analyzed.

    - Jumps in Centrality: The most telling feature is the sharp jump in a leader's
      centrality. For example, Node 0's local degree centrality might jump from
      ~0.48 (16 edges / 33 possible nodes) in the global graph to 1.0 in a later
      iteration. This happens because the algorithm has isolated its community
      into a subgraph where Node 0 is connected to every other node in that
      specific subgraph.

    - Changing Roles: A node's role changes. In the global graph, Node 0 and 33
      have high betweenness centrality because they act as bridges between the two
      factions. Once the factions are split, their local betweenness within
      their own faction may drop, as they are no longer bridging to the other side.
in summary, the community splits redefine the "context" for centrality.
The leaders (0 and 33) stay "central," but the algorithm shows their role
shifting from being global leaders of a full network to being the absolute,
high-centrality cores of their own isolated communities.


All tasks

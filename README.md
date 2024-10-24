Tool for Presorting and Visualization of UNGA-Voting Data

On the landing page users can select
(1) start and end of a time period
(2) subject
to presort all resolutions that were voted on in the United Nations General Assembly between 1946 and June of 2024.
The Voting Data is transformed into an edgelist of n * n-1 * 0.5 rows (where n is the number of UN-Members).
Each row shows a pair of countries and their average Voting coincidence over the selected resolutions.

The coincidence is considered to be the average of the following combinations of votes in favor (1), against (2) and abstentions (3):
(1) equal votes (1 && 1 || 2 && 2 || 3 && 3)   -> 1.0
(2) one abstention (1 && 3 || 2 && 3)          -> 0.5
(3) opposite votes (1 && 2)                    -> 0.0
Votes without representation of a state (8) or without UN-Membership in the time of the resolution (9) are filtered before.

The Edgelist is passed to the Visualization Tool which consists of three parts:

World Map: The world map can display the relationship between a selected state and all other states. Users can click on any state to update the map accordingly. To make it easier to find extreme values, there is a table with the 10 highest and lowest edge weights. There is also a table showing the internal coincidence within selected international organizations.

Coincidence Table: Here the edge weights are arranged in ascending order and tested for correlation with so-cio-economic factors. The R^2 and Spearman's rank correlation are calculated for this purpose. The latter measures the monotonic relationship of the ranks in-stead of the values themselves and is therefore particu-larly suitable for metrics with large ranges of values.

Network Graph: Here all states and their connections can be simulated simultaneously. For performance reasons and to spread out an otherwise quite dense graph, a slider is provided with which the user can de-fine which edge weight must be exceeded to simulate the edges. The traction of edges is proportional to the coincidence. The nodes don’t have weights, because there is no reasonable explanation for centrality measures in this context.

Interactive Website to be found here: https://pigeon-effect.github.io/UNGA-Website/

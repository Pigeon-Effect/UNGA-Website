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


# Data Source
Data in `results` is based on unofficial election results scraped from the NYC Board of Elections, last updated at 12:33 a.m. on June 25, 2025.

Shapefiles for election districts and neighborhood tabulation areas (NTA) are from the city Department of City Planning.

# Data Dictionary
Each row corresponds with an election district. Columns are as follows:

- `ed`: Election district ID
- `ct_{name}`: Number of votes a candidate recieved in the first round. Column name is based on a candidate's last name.
- `ct_total_votes`: Number of total votes casted in an election district
- `pct_{name}`: Percent of total votes a candidate recieved in the first round. Column name is based on a candidate's last name.
- `tied`: `yes` or `no` category indicating whether an election district is tied.
- `num_top_candidate`: Number of top-scoring candidates. For example: `1` for election districts with one winner; `2` for election districts where two candidates are tied; `3` for election districts where three candidates are tied, etc.
- `NTAName`: The neighborhood tabulation area (NTA) which an election district falls under. To determine the NTA which an election district falls under, the 2025 election district shapefile was merged with the 2020 NTA shapefile. In cases where election districts fall within more than one NTA, it is counted as being part of the NTA that included its largest area.
- `Candidate1`,`Candidate2`,`Candidate3`,`Candidate4`,`Candidate5`: Names of the five candidates with the most votes in an election district. In most elction districts, `Candidate1` indicates the winner, followed by `Candidate2`, who has recieved the second most numbers of votes, etc. In cases where an election district is tied, look to `num_top_candidate` for reference on ranking. For example, if `num_top_candidate` is `3`, then `Candidate1`,`Candidate2` and `Candidate3` are tied.
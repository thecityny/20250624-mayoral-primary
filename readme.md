# Data Source
Data in `results-96pct-1203am` is based on unofficial election results scraped from the NYC Board of Elections, last updated at 12:33 a.m. on June 25, 2025.

Shapefiles for election districts and neighborhood tabulation areass (NTA) are from the city Department of City Planning.

# Data Dictionary
Each row corresponds with an election district. Columns are as follows:

- `ed`: Election District
- `ct_{name}`: Number of votes a candidate recieved in the first round. Column name is based on a candidate's last name.
- `ct_total_votes`: Number of total votes casted in an election district
- `pct_{name}`: Percent of total votes a candidate recieved in the first round. Column name is based on a candidate's last name.
- `tied`: `yes` or `no` category indicating whether an election district is tied.
- `num_top_candidate`: Number of top-scoring candidates. For example: `1` for election districts with one winner; `2` for election districts where two candidates are tied; `3` for election districts where three candidates are tied, etc.
-  `winner`: Last name of the winner for the election district. In cases in which an election distric is tied between two or more candidate, just one candidate's name is shown. Please refer to the columns `tied` and `num_top_candidate` to determine whether an election district is tied.
-  `winner_name_full`: Full name of the winner for an election district. In cases in which an election distric is tied between two or more candidate, just one candidate's name is shown. Please refer to the columns `tied` and `num_top_candidate` to determine whether an election district is tied.
- `NTAName`: The neighborhood tabulation area (NTA) which an election district falls under. To determine the NTA which an election district falls under, the 2025 election district shapefile was merged with the 2020 NTA shapefile. In cases where election districts fall within more than one NTA, it is counted as being part of the NTA that included its largest area.
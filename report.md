# Netflix Actor–Director Collaboration Network Analysis

## Project Overview
This project examines professional collaboration patterns in the Netflix Movies and TV Shows catalogue using an undirected network. Nodes represent actors or directors; an edge connects two people who worked on the same title. Edge weights count repeated shared titles.

## Motivation and Questions
- Which actors frequently work together?
- Which actors and directors have the strongest repeated partnerships?
- Who appears most often in the prepared dataset?
- How does the network vary across release decades?

## Data and Preparation
The original Netflix dataset contained 8,807 records. Rows missing cast or director information were removed, and the first four cast members were retained alongside all listed directors. The prepared analysis dataset contains 5,700 titles.

## Network Construction
Using Python, Pandas and NetworkX, each title's actors and directors were connected pairwise. Role-prefixed nodes distinguish an actor from a director with the same name. The complete graph contains **12,523 actor nodes, 4,529 director nodes, 17,052 nodes in total and 50,823 unique edges**.

## Actor–Director Partnerships
The analysis counted 21,523 unique actor–director pairs. The strongest reported pairs include:
| Actor | Director | Shared titles |
|---|---|---:|
| Rupa Bhimani | Rajiv Chilaka | 18 |
| Julie Tejwani | Rajiv Chilaka | 17 |
| Jigna Bhardwaj | Rajiv Chilaka | 17 |
| Vatsal Dubey | Rajiv Chilaka | 16 |
| Saurav Chakraborty | Suhas Kadav | 8 |

The plotted network focuses on the top 15 partnerships for readability.

## Actor–Actor Partnerships
The analysis found 28,185 unique actor pairs. Julie Tejwani and Rupa Bhimani were the strongest pair in the prepared data, sharing 26 titles. Several pairs involving Julie Tejwani, Jigna Bhardwaj, Rupa Bhimani and Vatsal Dubey shared 16 titles each, suggesting a recurring group in the catalogue.

## Frequent Actors
| Actor | Titles |
|---|---:|
| Shah Rukh Khan | 35 |
| Akshay Kumar | 28 |
| Rupa Bhimani | 27 |
| Julie Tejwani | 26 |
| Amitabh Bachchan | 25 |
| Anupam Kher | 22 |
| Kareena Kapoor | 22 |
| Naseeruddin Shah | 21 |
| Adam Sandler | 20 |
| Ajay Devgn | 20 |

## Frequent Directors
| Director | Titles |
|---|---:|
| Jan Suter | 21 |
| Rajiv Chilaka | 19 |
| Raúl Campos | 19 |
| Marcus Raboy | 16 |
| Jay Karas | 15 |
| Suhas Kadav | 13 |
| Cathy Garcia-Molina | 13 |
| Youssef Chahine | 12 |
| Martin Scorsese | 12 |
| Jay Chapman | 12 |

## Network by Release Decade
| Decade | Titles | Nodes | Unique edges | Collaboration occurrences | Occurrences/title |
|---|---:|---:|---:|---:|---:|
| 1940s | 5 | 16 | 31 | 31 | 6.20 |
| 1950s | 11 | 48 | 108 | 115 | 10.45 |
| 1960s | 23 | 107 | 233 | 235 | 10.22 |
| 1970s | 63 | 273 | 609 | 633 | 10.05 |
| 1980s | 121 | 488 | 1,119 | 1,210 | 10.00 |
| 1990s | 237 | 916 | 2,227 | 2,302 | 9.71 |
| 2000s | 673 | 2,317 | 6,551 | 6,893 | 10.24 |
| 2010s | 3,812 | 12,439 | 33,723 | 35,244 | 9.25 |
| 2020s | 755 | 3,217 | 6,926 | 7,149 | 9.47 |

The 2010s dominate the dataset by titles, nodes, unique edges and total collaboration occurrences. The 1950s show the highest occurrences per title (10.45), but this is based on only 11 titles and should be interpreted cautiously. The average is relatively stable across several decades, with a lower value in the 2010s.

## Conclusions
- The dataset reveals a sizeable professional network: 17,052 role-labelled nodes and 50,823 unique connections.
- Julie Tejwani and Rupa Bhimani were the strongest actor–actor partnership found, with 26 shared titles.
- Rupa Bhimani and Rajiv Chilaka were the strongest actor–director partnership found, with 18 shared titles.
- Shah Rukh Khan led the actor appearance ranking (35 titles); Jan Suter led the director ranking (21 titles).
- The 2010s had the largest network in absolute terms, although volume alone does not imply more intensive collaboration.

## Limitations
- Only the first four cast names per title were included.
- Titles missing cast or director data were excluded, leaving 5,700 records from 8,807.
- Netflix catalogue representation is not a comprehensive record of the entire film industry.
- Appearance counts do not measure popularity, audience reach or commercial success.
- People acting and directing are represented as separate role-prefixed nodes.
- Decades have different sample sizes, and the 2020s are incomplete.
- A unique edge is distinct from weighted repeated collaborations; the two measures are not interchangeable.

## Tools
Python, Pandas, NumPy, NetworkX, Matplotlib, itertools and collections.

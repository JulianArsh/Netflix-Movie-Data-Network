# 🎬 Netflix Actor–Director Collaboration Network Analysis

## 📌 Project Overview

This project explores professional relationships between actors and directors using the Netflix Movies and TV Shows dataset.

The goal is to build an undirected collaboration network where:
- **Nodes** represent actors and directors.
- **Edges** represent people who worked together on the same movie or TV show.
- **Edge weights** represent the number of titles shared by two people.

Using Python and NetworkX, this project identifies recurring collaborations, influential participants in the network, and changes in collaboration patterns across different release decades.

## 🎯 Project Objectives

- Build an actor–director collaboration network.
- Identify actors who frequently work together.
- Discover the strongest actor–director partnerships.
- Identify the most frequently appearing actors and directors.
- Compare collaboration networks across release decades.
- Communicate findings through network graphs and visualizations.

## 📂 Project Structure

```text
netflix-actor-director-network/
│
├── Netflix_Movie_Data.ipynb
├── netflix_dataset.csv
├── README.md
│
└── reports/
    ├── report.md
    ├── actor_director_network.png
    ├── actor_actor_collaborations.png
    ├── top_actors.png
    ├── top_directors.png
    ├── titles_by_decade.png
    └── collaboration_per_title.png
```

## 📊 Dataset

The project uses the Netflix Movies and TV Shows dataset.

- Original records: 8,807
- Original columns: 11
- Records retained after removing missing cast and director information: 5,700
- Actors considered per title: First four cast members
- Directors considered per title: All listed directors

Important variables include:

| Variable | Description |
|---|---|
| `title` | Movie or TV show name |
| `cast` | Actors associated with a title |
| `director` | Director or directors |
| `release_year` | Original release year |
| `type` | Movie or TV show |

## 🛠️ Technologies Used

- **Python** – Programming language
- **Pandas** – Data cleaning and manipulation
- **NumPy** – Numerical operations
- **NetworkX** – Network construction and analysis
- **Matplotlib** – Data visualization
- **itertools** – Generating actor and director pairs
- **Collections** – Counting appearances

## 🔍 Analysis and Methodology

### 1. Data Preparation

- Loaded the Netflix dataset.
- Removed records with missing cast or director information.
- Extracted the first four actors from each title.
- Extracted all available directors.
- Prepared the data for network construction.

### 2. Network Construction

Created an undirected graph using NetworkX.

Each title connects all its included actors and directors. The resulting network includes actor–actor, actor–director and director–director relationships.

### 3. Actor–Director Collaboration Analysis

Counted shared titles between actors and directors.

The strongest partnership identified was:

| Actor | Director | Shared Titles |
|---|---|---:|
| Rupa Bhimani | Rajiv Chilaka | 18 |
| Julie Tejwani | Rajiv Chilaka | 17 |
| Jigna Bhardwaj | Rajiv Chilaka | 17 |
| Vatsal Dubey | Rajiv Chilaka | 16 |

### 4. Actor–Actor Collaboration Analysis

Identified recurring actor partnerships.

The strongest partnership was:

**Julie Tejwani and Rupa Bhimani – 26 shared titles.**

### 5. Most Frequently Appearing Actors

| Actor | Number of Titles |
|---|---:|
| Shah Rukh Khan | 35 |
| Akshay Kumar | 28 |
| Rupa Bhimani | 27 |
| Julie Tejwani | 26 |
| Amitabh Bachchan | 25 |

### 6. Most Frequently Appearing Directors

| Director | Number of Titles |
|---|---:|
| Jan Suter | 21 |
| Rajiv Chilaka | 19 |
| Raúl Campos | 19 |
| Marcus Raboy | 16 |
| Jay Karas | 15 |

### 7. Network Analysis Across Decades

The network was divided into release decades to investigate changes in professional collaboration patterns.

The 2010s contained the largest network, with:

- 3,812 titles
- 12,439 people (nodes)
- 33,723 unique connections (edges)
- 35,244 total collaboration occurrences

The 1950s recorded the highest average collaboration occurrences per title, at 10.45, although this result was based on only 11 titles.

## 📈 Key Results

| Metric | Result |
|---|---:|
| Prepared titles | 5,700 |
| Actor nodes | 12,523 |
| Director nodes | 4,529 |
| Total nodes | 17,052 |
| Unique network edges | 50,823 |
| Unique actor–director partnerships | 21,523 |
| Unique actor–actor partnerships | 28,185 |

## 💡 Key Insights

1. Julie Tejwani and Rupa Bhimani formed the strongest actor–actor partnership, sharing 26 titles.
2. Rupa Bhimani and Rajiv Chilaka formed the strongest actor–director partnership, sharing 18 titles.
3. Shah Rukh Khan had the highest actor appearance count, with 35 titles.
4. Jan Suter had the highest director appearance count, with 21 titles.
5. The 2010s had the largest collaboration network by title count, nodes and unique edges.
6. Collaboration occurrences per title remained relatively stable across several decades.

## 📉 Limitations

- Only the first four cast members listed per title were included.
- Titles missing cast or director information were excluded.
- The dataset represents Netflix's catalogue rather than the entire entertainment industry.
- Frequent appearances do not necessarily indicate popularity or commercial success.
- People who acted and directed are represented as separate role-labelled nodes.
- The 2020s are an incomplete decade.
- Network size and collaboration frequency measure different aspects of professional relationships.

## 🚀 How to Run the Project

1. Clone or download this repository.
2. Install the required Python libraries:

```bash
pip install pandas numpy matplotlib networkx
```

3. Ensure `netflix_dataset.csv` is available in the expected location.
4. Open `Netflix_Movie_Data.ipynb` in Jupyter Notebook or JupyterLab.
5. Run the notebook cells sequentially.

## 📁 Project Deliverables

- Jupyter Notebook containing the complete analysis.
- Actor–director collaboration network visualization.
- Actor–actor collaboration chart.
- Most frequently appearing actor and director charts.
- Decade-based network analysis.
- Detailed project report.

## 🏁 Conclusion

This project demonstrates how network analysis can uncover professional collaboration patterns in the entertainment industry.

By transforming Netflix catalogue data into a graph, it becomes possible to identify recurring partnerships, frequently appearing industry participants and changes in collaboration patterns over time.

The project highlights the practical application of Python, data analysis and network visualization in extracting meaningful insights from real-world datasets.

---

**Author:** Julian Wanjiru  
**Project:** Netflix Actor–Director Collaboration Network Analysis  
**Tools:** Python, Pandas, NetworkX, Matplotlib  
**Category:** Data Analysis | Network Science | Data Visualization

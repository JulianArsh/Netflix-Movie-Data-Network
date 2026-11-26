# 🎬 Netflix Actor–Director Collaboration Network Analysis

Explore how actors and directors collaborate across Netflix titles using Python and network analysis.

## 📌 Project Overview

This project explores professional collaboration relationships between actors and directors using the Netflix Movies and TV Shows dataset.

Using Python and NetworkX, I transformed Netflix catalogue data into an undirected collaboration network to identify recurring partnerships, frequently appearing industry participants, and changes in collaboration patterns across release decades.

The network represents:
- **Nodes:** Actors and directors.
- **Edges:** Connections between people who worked on the same title.
- **Edge weights:** Number of titles shared by two people.

## 🎯 Project Objectives

- Build an actor–director collaboration network.
- Identify actors who frequently work together.
- Discover the strongest actor–director partnerships.
- Identify frequently appearing actors and directors.
- Compare collaboration networks across release decades.
- Communicate findings through charts and network visualizations.

## 🛠️ Technologies Used

| Technology | Purpose |
|---|---|
| Python | Programming and analysis |
| Pandas | Data cleaning and manipulation |
| NumPy | Numerical operations |
| NetworkX | Network construction and analysis |
| Matplotlib | Data visualization |
| itertools | Generating collaboration pairs |
| Collections | Counting collaborations |

## 📂 Project Structure

```text
Netflix-Movie-Data-Network/
│
├── notebook.ipynb
├── netflix_dataset.csv
├── README.md
├── netflix_network_portfolio.zip




## 📊 Dataset

The project uses the Netflix Movies and TV Shows dataset.

| Dataset information | Result |
|---|---:|
| Original records | 8,807 |
| Original columns | 11 |
| Records retained after cleaning | 5,700 |
| Actors considered per title | First four cast members |
| Directors considered per title | All listed directors |

Important variables include:

| Variable | Description |
|---|---|
| `title` | Movie or TV show name |
| `cast` | Actors associated with a title |
| `director` | Director or directors |
| `release_year` | Original release year |
| `type` | Movie or TV show |

## 🔍 Analysis and Methodology

### 1. Data Preparation
- Loaded the Netflix dataset.
- Removed records with missing cast or director information.
- Extracted the first four actors from each title.
- Extracted all available directors.
- Prepared the data for network construction.

### 2. Network Construction

Created an undirected graph using NetworkX.

Each title connects its included actors and directors. The resulting network includes:
- Actor–actor relationships.
- Actor–director relationships.
- Director–director relationships.

People who acted and directed are represented as separate role-labelled nodes.

### 3. Actor–Director Collaboration Analysis

Counted shared titles between actors and directors.

The strongest partnerships identified were:

| Actor | Director | Shared titles |
|---|---|---:|
| Rupa Bhimani | Rajiv Chilaka | 18 |
| Julie Tejwani | Rajiv Chilaka | 17 |
| Jigna Bhardwaj | Rajiv Chilaka | 17 |
| Vatsal Dubey | Rajiv Chilaka | 16 |

### 4. Actor–Actor Collaboration Analysis

Identified recurring actor partnerships.

**Strongest partnership: Julie Tejwani and Rupa Bhimani — 26 shared titles.**

### 5. Most Frequently Appearing Actors

| Actor | Number of titles |
|---|---:|
| Shah Rukh Khan | 35 |
| Akshay Kumar | 28 |
| Rupa Bhimani | 27 |
| Julie Tejwani | 26 |
| Amitabh Bachchan | 25 |

### 6. Most Frequently Appearing Directors

| Director | Number of titles |
|---|---:|
| Jan Suter | 21 |
| Rajiv Chilaka | 19 |
| Raúl Campos | 19 |
| Marcus Raboy | 16 |
| Jay Karas | 15 |

### 7. Network Analysis Across Decades

The network was divided into release decades to investigate changes in professional collaboration patterns.

The 2010s contained the largest network:

- 3,812 titles.
- 12,439 nodes.
- 33,723 unique edges.
- 35,244 total collaboration occurrences.

The 1950s recorded the highest average collaboration occurrences per title, at 10.45, based on only 11 titles.

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

## 📊 Visualizations

The project includes visualizations illustrating the collaboration network and key findings.

If you have uploaded the images into the `reports/` folder, you can display them directly in this README:

### Actor–Director Collaboration Network

![Actor–Director Network](reports/actor_director_network.png)

### Actor–Actor Collaborations

![Actor–Actor Collaborations](reports/actor_actor_collaborations.png)

### Top Actors

![Top Actors](reports/top_actors.png)

### Top Directors

![Top Directors](reports/top_directors.png)

### Netflix Titles by Decade

![Titles by Decade](reports/titles_by_decade.png)

### Collaboration Occurrences per Title

![Collaboration Occurrences per Title](reports/collaboration_per_title.png)

## 📉 Limitations

- Only the first four cast members listed per title were included.
- Titles missing cast or director information were excluded.
- The dataset represents Netflix's catalogue rather than the entire entertainment industry.
- Frequent appearances do not necessarily indicate popularity or commercial success.
- People who acted and directed are represented as separate role-labelled nodes.
- The 2020s are an incomplete decade.
- Network size and collaboration frequency measure different aspects of professional relationships.

## 🚀 How to Run the Project

### 1. Clone the repository

```bash
git clone https://github.com/JulianArsh/Netflix-Movie-Data-Network.git
cd Netflix-Movie-Data-Network
```

### 2. Install the required libraries

```bash
pip install pandas numpy matplotlib networkx
```

### 3. Open the notebook

Open `notebook.ipynb` using Jupyter Notebook or JupyterLab.

### 4. Run the notebook

Ensure `netflix_dataset.csv` is in the expected location, then execute the notebook cells sequentially.

## 🏁 Conclusion

This project demonstrates how network analysis can uncover professional collaboration patterns in the entertainment industry.

By transforming Netflix catalogue data into a graph, it becomes possible to identify recurring partnerships, frequently appearing industry participants and changes in collaboration patterns over time.

The project showcases practical applications of Python, data cleaning, exploratory data analysis, NetworkX and data visualization.

## 👨‍💻 Author

**Julian Wanjiru**

- **Project:** Netflix Actor–Director Collaboration Network Analysis
- **Tools:** Python, Pandas, NetworkX, Matplotlib
- **Category:** Data Analysis | Network Science | Data Visualization

---

⭐ If you find this project interesting, feel free to explore the repository and share your feedback.

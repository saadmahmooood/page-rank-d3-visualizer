# Simple Python Search Spider, Page Ranker, and Visualizer

This project is a simplified implementation of a search engine. It includes tools for crawling websites, calculating page ranks, and visualizing web structures. Data is stored in an `SQLite` database named `spider.sqlite`.

---

## **Features**
1. **Web Crawling**
   - Crawl and store pages with `spider.py`.
   - Records links between pages.
   - Supports incremental crawling (does not re-crawl already visited pages).
2. **Page Rank Calculation**
   - Use `sprank.py` to calculate and refine page ranks using iterative methods.
3. **Data Visualization**
   - Generate JSON data with `spjson.py` and visualize web structures using `force.html`.

---

## **Requirements**
- **Python 3.x**
- **SQLite Browser**: [Install here](http://sqlitebrowser.org/) to view or modify the database.
- Additional Tools:
  - **D3.js** for visualization.

---

## **Usage**

### 1. **Setup**
   - For Windows, run the following in the command prompt for proper UTF-8 encoding:
     ```cmd
     chcp 65001
     ```

### 2. **Crawling Websites**
   - Start crawling with `spider.py`:
     ```bash
     python3 spider.py
     ```
   - Example Input:
     ```
     Enter web URL or enter: http://www.dr-chuck.com/
     How many pages: 2
     ```
   - This will crawl and store two pages, recording their links.

### 3. **Viewing Database**
   - Use `spdump.py` to display the contents of `spider.sqlite`:
     ```bash
     python3 spdump.py
     ```

### 4. **Calculating Page Ranks**
   - Calculate page ranks with `sprank.py`:
     ```bash
     python3 sprank.py
     ```
   - Specify the number of iterations for refinement:
     ```
     How many iterations: 50
     ```

### 5. **Resetting Page Ranks**
   - Reset page ranks using `spreset.py`:
     ```bash
     python3 spreset.py
     ```

### 6. **Visualizing Data**
   - Generate visualization JSON with `spjson.py`:
     ```bash
     python3 spjson.py
     ```
   - Example:
     ```
     How many nodes? 30
     ```
   - Open `force.html` in a browser to view an interactive web structure.

---

## **Sample Outputs**

### **Database Dump (`spdump.py`):**
```
(5, None, 1.0, 3, 'http://www.dr-chuck.com/csev-blog')
(3, None, 1.0, 4, 'http://www.dr-chuck.com/dr-chuck/resume/speaking.htm')
```

### **Page Ranks (`sprank.py`):**
```
How many iterations: 50
[(1, 12.79), (2, 28.93), (3, 6.81), (4, 13.47)]
```

---

## **Visualization**
- Open `force.html` to view a D3.js-powered interactive graph of nodes and links.
- Drag and double-click nodes to explore the structure.

---

## **Acknowledgements**
- Data visualization powered by [D3.js](http://mbostock.github.io/d3/).
- Based on materials from Dr. Chuck’s courses.

---

Happy Crawling and Analyzing! 🚀
```

---

### **Summary of What This README.md Covers:**

1. **Project Overview**: Explains the purpose of the project.
2. **Features**: Highlights the main functionalities like crawling, ranking, and visualization.
3. **Requirements**: Lists necessary tools and installations.
4. **Usage Instructions**: Detailed steps for crawling, ranking, and visualization.
5. **Sample Outputs**: Example outputs from running the scripts.
6. **Visualization Details**: Instructions for using `force.html` for interactive visualization.
7. **Acknowledgements**: Credits to resources and inspirations.

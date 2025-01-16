# Web Crawler and Page Ranking System

This project implements a simple web crawler and page ranking system using Python and SQLite. It emulates basic functions of a search engine by crawling web pages, recording links between them, calculating page ranks, and visualizing the link structure.

## Overview

The system comprises three main components:

1. **Web Crawler**: Fetches web pages and stores their content and links in a SQLite database.
2. **Page Rank Calculator**: Computes the rank of each page based on the links using an iterative algorithm.
3. **Visualizer**: Generates a visual representation of the web pages and their links, illustrating the structure of the crawled web.

## Repository Structure

- **Python Scripts**:
  - `spider.py`: Crawls web pages and stores data in `spider.sqlite`.
  - `sprank.py`: Calculates page ranks iteratively.
  - `spjson.py`: Prepares data for visualization by creating `spider.js`.
  - `spreset.py`: Resets page ranks to their initial values.
  - `spdump.py`: Displays the contents of the database for inspection.

- **Visualization Files**:
  - `force.html`: Displays the visual representation of the web structure.
  - `force.js`: Contains JavaScript code for the visualization.
  - `d3.v2.js`: D3.js library for creating dynamic visualizations.
  - `force.css`: CSS styling for the visualization.

- **Database**:
  - `spider.sqlite`: SQLite database storing crawled web data and page ranks.

## Setup and Usage

**Crawl Web Pages**:

   Run `spider.py` to start crawling:

   ```bash
   python spider.py
   ```

   Follow the prompts to enter a starting URL and the number of pages to crawl.

**Calculate Page Ranks**:

   After crawling, compute page ranks using `sprank.py`:

   ```bash
   python sprank.py
   ```

   Specify the number of iterations for the algorithm when prompted.

**Generate Visualization Data**:

   Prepare the data for visualization by running `spjson.py`:

   ```bash
   python spjson.py
   ```

   This creates `spider.js`, which is used by `force.html`.

**View the Visualization**:

   Open `force.html` in a web browser to see the visual representation of the crawled web structure.

## Notes

- To reset the page ranks without re-crawling, use `spreset.py`:

  ```bash
  python spreset.py
  ```

- To inspect the database contents, run `spdump.py`:

  ```bash
  python spdump.py
  ```

- The `spider.sqlite` file can be deleted at any time to restart the process with a fresh database.

---

By following this guide, you can set up and run a basic web crawler and page ranking system, gaining insights into web structures and the fundamentals of search engine operations. 

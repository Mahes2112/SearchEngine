# 🔍 Java Search Engine (Web Crawler + Lucene)

A **mini search engine built entirely in Java**, implementing the core ideas behind real-world search systems like Google — from **web crawling** to **indexing** and **ranked keyword search** using **Apache Lucene**.

This project focuses on **information retrieval fundamentals**, not AI hype.

---

## 🚀 Features

- 🌐 **Web Crawler**
  - Crawls web pages starting from seed URLs
  - Downloads raw HTML
  - Avoids duplicate URLs
  - Depth-limited crawling

- 🧹 **HTML Parsing & Cleaning**
  - Removes scripts, styles, and navigation noise
  - Extracts page title and clean body text
  - Stores extracted data in JSONL format

- 📚 **Lucene Indexing**
  - Indexes cleaned web pages using Apache Lucene
  - Each web page = one Lucene `Document`
  - Indexed fields:
    - `url` (stored)
    - `title` (stored + boosted)
    - `body` (indexed)

- 🔎 **Keyword Search**
  - Searches across title and body text
  - Uses boosted relevance (title > body)
  - Displays title, URL, and relevance score

- 🖥️ **Command-Line Interface**
  - Interactive search from terminal
  - Supports multi-word queries

---

## 🛠️ Tech Stack

- **Language:** Java  
- **Search Library:** Apache Lucene (v10+)  
- **I/O:** Core Java (HttpURLConnection, BufferedReader, File I/O)  
- **Parsing:** Custom HTML cleaning logic  
- **Build Tool:** Manual JAR setup (no frameworks)

---

## 📂 Project Structure

```
search-engine/
├── src/
│   ├── Webcrawling.java
│   ├── ContentExtractor.java
│   ├── LuceneIndexing.java
│   └── LuceneSearching.java
├── data/
│   └── extractedcontent.jsonl
├── index/
├── lib/
└── README.md
```

---

## ⚙️ How It Works

1. **Crawling** – Downloads HTML pages from seed URLs  
2. **Extraction** – Cleans HTML and extracts useful text  
3. **Indexing** – Builds Lucene inverted index  
4. **Searching** – Performs ranked keyword search  

---

## ▶️ How to Run

1. Run `Webcrawling.java` and `ContentExtractor.java`
2. Run `LuceneIndexing.java`
3. Run `LuceneSearching.java` and search from CLI

---

## 📈 Future Improvements

- Snippet generation
- Parallel crawling
- Custom analyzers (n-grams)
- REST API / Web UI

---

## 📜 License

Educational / learning project.

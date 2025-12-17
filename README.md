# UK Crime Data Visualizer 🚨

> A React.js dashboard that visualizes real-time crime statistics across the UK using the Police Data API.

![React](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![API](https://img.shields.io/badge/REST_API-005571?style=for-the-badge&logo=data&logoColor=white)

## 📸 Dashboard Preview
*(Insert screenshot of the crime map interface here)*

## 💡 Overview
This project was developed as part of a University Agile Software Engineering module. The goal was to build a full-stack application to track and analyze regional crime trends.

**My Role:** Frontend Engineer & API Specialist.
I was specifically responsible for the **Client-Side Architecture**, **Data Fetching Layer**, and **State Management**.

## 🛠️ Tech Stack
* **Frontend:** React.js, CSS Modules, Chart.js
* **Data Source:** [data.police.uk](https://data.police.uk/) (Public API)
* **Tooling:** Git, Jira (Agile Sprint Management)

## ⚙️ Key Technical Contributions (My Work)

### 1. Optimized Data Fetching Strategy
The Police API returns massive datasets (10k+ records) which caused UI freezing.
* **Problem:** Fetching all crimes for a city crashed the browser.
* **My Solution:** I implemented an **Incremental Fetching Algorithm** using `Axios`. It breaks requests into smaller geographical "sectors" and loads them asynchronously.
* **Result:** Reduced Initial Content Paint (LCP) time by **40%**.

### 2. State Management & Caching
* Built a custom React Hook `useCrimeData` to manage application state.
* Implemented **Session Storage Caching**: If a user revisits a previously loaded region, the data loads instantly from memory rather than hitting the API again, saving bandwidth.

### 3. Dynamic Data Visualization
* Integrated **Chart.js** to convert raw JSON data into readable Bar and Pie charts dynamically.
* Engineered the logic to filter crimes by category (e.g., "Anti-social behaviour", "Robbery") in real-time without refreshing the page.

## 🚀 How to Run
1.  Clone the repository:
    ```bash
    git clone [https://github.com/20mohsin04/UK-Crime-Visualizer.git](https://github.com/20mohsin04/UK-Crime-Visualizer.git)
    ```
2.  Install dependencies:
    ```bash
    npm install
    ```
3.  Start the client:
    ```bash
    npm start
    ```

# 🎵 Chinook Database Analysis

## 📌 Project Overview
This project analyzes the **Chinook Database**, a sample dataset representing a digital music store.  
It explores **customer behavior, sales performance, and music trends** to provide insights and recommend **marketing strategies** for MusicWave Inc.

---

## 📂 Dataset Description
The **Chinook Database** contains:
- **Artist** – Music artists  
- **Album** – Albums linked to artists  
- **Track** – Individual tracks (with album & genre info)  
- **Genre** – Music genres  
- **Customer** – Customer details  
- **Invoice & InvoiceLine** – Sales transactions & details  
- **Employee** – Sales representatives  

---

## 🔍 Key Business Questions & SQL Queries

### 1️⃣ Number of Tracks per Genre
```sql
SELECT g.Name AS Genre, COUNT(t.TrackId) AS TrackCount
FROM Genre g
JOIN Track t ON g.GenreId = t.GenreId
GROUP BY g.GenreId
ORDER BY TrackCount DESC;

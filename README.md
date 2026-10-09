# Orbit Nexus 🪐
> City-First Social Networking Platform  
> *Connecting communities locally while maintaining absolute location privacy.*

---

## 📌 Project Overview
Orbit Nexus is a specialized social networking web application designed to bridge the gap in modern social media platforms, which often prioritize global content over local community connections. 

Built using ASP.NET Core (C#), SQL Server, and HTML/CSS, Orbit Nexus introduces the Orbit Engine—a city-centric content and user recommendation system. By leveraging custom Data Structures and Algorithms (DSA), the platform prioritizes posts and members from a user's specific city without ever requesting or exposing exact GPS location coordinates.

---

## 👥 Project Information
* Course: Data Structures & Algorithms (DSA)
* Degree: BS Software Engineering (Session 2025–2029)
* Supervised by: Mr. Muhammad Nazir
* Department: Institute of Data Science (Software Engineering)
* Institution: University of Engineering and Technology (UET), Lahore, Pakistan

### 👨‍💻 Team Members
* Muhammad Jown Raza (`2025-SE-40`)
* Ali Hassan (`2025-SE-49`)
* Abdullah Saeed (`2025-SE-25`)
* Umar Nadeem (`2025-SE-18`)

---

## 🎯 Key Features

* 🌆 City-Centric Home Feed: Automatically prioritizes posts from users residing in the same city using custom scoring algorithms.
* 🪐 Dedicated Orbit Directory: Fast lookup of all members in your city via hash-based indexing.
* 🛡️ Privacy & Safety First:
  * Ghost Mode: Reveals only the registered city, never precise GPS data.
  * Safety Tools: Comprehensive user blocking, reporting, and moderation controls.
* 💬 Real-Time Direct Messaging: Private messaging, media sharing, and instant notification buffering.
* ⚡ Algorithmic Search & Discovery: Multi-layered search with fuzzy string matching ("Did you mean?"), auto-complete, and graph-based "Friends of Friends" recommendations.

---

## 🛠️ Data Structures & Algorithms (DSA) Implementation

| DSA Concept | Platform Feature & Implementation | Time / Space Complexity |
| :--- | :--- | :--- |
| Hash Tables (`Dictionary<K,V>`) | Instant city-based user grouping and direct user profile retrievals without full database scans. | $O(1)$ average |
| Graph (Adjacency List) | Represents users as nodes and direct follow relationships as directed edges. | $O(V + E)$ space |
| Breadth-First Search (BFS) | Level-by-level traversal over follow graphs to generate local "Friends of Friends" connection suggestions. | $O(V + E)$ |
| Priority Queue / Max-Heap | Extracts top-trending posts dynamically without performing costly full-dataset sorts. | $O(\log N)$ extraction |
| Trie (Prefix Tree) | Powers real-time auto-complete for usernames, hashtags, and city searches. | $O(L)$ where $L$ = query length |
| Recursion & DFS | Models multi-level nested comment replies and renders hierarchical comment threads. | $O(N)$ tree depth |
| Custom Sorting Algorithms | Custom QuickSort / MergeSort implementation to rank home feeds by time-decay post scores. | $O(N \log N)$ |
| HashSet (`HashSet<T>`) | Instant $O(1)$ membership lookup to filter out blocked accounts and already-followed users. | $O(1)$ average |
| FIFO Queue | Buffers incoming real-time notifications and direct messages for accurate chronological processing. | $O(1)$ push/pop |
| Doubly Linked List | Bidirectional navigation for photo carousels and message history pagination. | $O(1)$ pointer shift |
| KMP Pattern Matching | Fast string normalization and hashtag/keyword extraction from post captions. | $O(N + M)$ |
| Levenshtein Distance | Calculates edit distance between string queries to power typo-tolerant "Did you mean?" search queries. | $O(M \times N)$ |
| Time Decay Function | Mathematical post score reduction over time: $\text{Score} = \frac{\text{Interactions}}{(Age + 2)^\gamma}$ | $O(1)$ evaluation |


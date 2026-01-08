# System Design Course Curriculum

A comprehensive index of the System Design course content. This curriculum covers basics, core distributed system concepts, deep dives into real-world high-level architectures, and a library of additional design scenarios.

## 📖 Table of Contents

- [1. Basics: Building an Ecommerce App](#1-basics-building-an-ecommerce-app-1-to-1m)
- [2. Concepts](#2-concepts)
- [3. High Level Design](#3-high-level-design)
    - [3.1 Gmail (Emailing Service)](#31-design-an-emailing-service-like-gmail-link)
    - [3.2 Tinder](#32-tinder-system-design-link)
    - [3.3 WhatsApp](#33-whatsapp-system-design-link)
    - [3.4 Chess (Turn-Based Gaming)](#34-chess-design-building-a-highly-scalable-turn-based-gaming-website-link)
    - [3.5 Hotstar (Live Streaming)](#35-hotstar-live-video-streaming-design-link)
    - [3.6 Google Docs (Collaborative Editor)](#36-google-docs-collaborative-editor-design-link)
    - [3.7 Uber (Cab Aggregator)](#37-design-a-cab-aggregator-app-like-uber-link)
    - [3.8 Google Maps (Location Services)](#38-design-a-location-based-service-like-google-maps-link)
    - [3.9 WhatsApp Calling (VoIP)](#39-whatsapp-calling-app-link)
    - [3.10 Recommendation Engine](#310-recommendation-engine-design-link)
    - [Additional System Design Scenarios](#additional-system-design-scenarios)
- [4. Research Paper Analysis](#4-research-paper-analysis)

---

## 1. Basics: Building an Ecommerce App (1 to 1M)
**Overview:** Introduction to system design through the evolution of a startup.

- **Intro:** How do I use this course?
- **#1:** What is System Design?
- **#2:** A star-tup is born!
- **#3:** Where are the pages?
- **#4:** Debugging in the trenches
- **#4.1:** Hard questions, harder answers
- **#5:** Serverless or Server-More?
- **#6:** Database-like Memory, Cache-like Recall
- **#7:** The case of the Expensive Cache
- **#8:** Sale Day Jitters
- **#9:** A new CTO is born!
- **#10:** Concluding the series!

---

## 2. Concepts

### 2.1 Databases Deep Dive
- What are Databases?
- Storage and Retrieval
- What is a NoSQL database?
- Types of Databases: Graph, TimeSeries and Object
- What database should you choose?

### 2.2 Consistency in Distributed Systems
- What is Data Consistency?
- Linearizable Consistency
- Eventual Consistency
- Causal Consistency
- Quorum
- Data Consistency Levels Tradeoffs
- **Quiz 1:** 5 questions
- Transaction Isolation Levels - Read Uncommitted Data
- Read Committed
- Repeatable Reads
- Serializable Isolation Level
- Transaction Level Implementations
- **Quiz 2:** 6 questions
- Conclusion - Transaction Isolation
- **PDF summary**

### 2.3 Caches Deep Dive
- Caching: Basics
- **Quiz 1:** 3 questions
- Write Policies: Write Back Policy
- Write Through Policy
- Write Around Policy
- Replacement Policies: LRU, LFU and Segmented LRU
- **Quiz 2:** 6 questions
- **PDF Summary**

### 2.4 Networks Deep Dive
- Breakdown: The physical layer
- Breakdown: The Routing Layer
- Breakdown: The behavioral layer
- **Quiz 1:** 3 questions
- Connecting to the internet: ISPs, DNS and everything in between
- Internal routing: MAC addresses and NAT
- **Quiz 2:** 4 questions
- HTTP, WebSockets, TCP and UDP
- Communication Standards: REST, GraphQL and GRPC
- Head of line blocking
- **Quiz 3:** 4 questions
- **Design Question:** Netflix Content Distribution Network
- Video transmission: WebRTC and HTTP-DASH
- **Quiz 4:** 3 questions
- **Summary PDF Networks**

### 2.5 Database Replication and Migration
- Primary Replica Architectures
- WAL and Change Data Capture
- Write Amplification and Split Brain
- Database Migrations
- Migrating the Database
- Migration Across Regions
- **Database Migration Summary**

### 2.6 Security in Distributed Systems
- Security aspects in distributed systems
- Token Based Auth
- SSO and OAuth
- Access Control Lists and Rule Engines
- Attack Vectors - Hackers, Developers and Code
- How videos are protected inside CDNs
- **Quiz:** Security Best Practices (5 questions)

### 2.7 Observability in Distributed Systems
- Introduction to Observability
- Logging - Best Practices
- Monitoring Metrics
- Anomaly Detection: Holt-Winters Algorithm
- Root Cause Analysis
- Conclusion to Observability

### 2.8 Distributed Consensus with Paxos
- The Problem of Distributed Consensus
- Basic Algorithm
- Improving the algorithm
- Termination Conditions
- Practical Considerations
- **Design Question:** Design a Payment Gateway

### 2.9 Distributed Rate Limiting
- The Oracle and the Timer Wheel
- **Quiz 1:** 3 questions
- Partitioning and Real-life Optimisations
- Architecture Diagram
- Capacity Estimations
- **Quiz 2:** 3 questions
- Summary PDF - Rate Limiting
- API Contracts
- FAQs

### 2.10 System Design Tradeoffs
- Introduction to design tradeoffs
- Pull vs. Push Architectures
- Memory vs. Latency
- Throughput vs. Latency
- Consistency vs. Availability
- Latency vs. Accuracy
- SQL vs. NoSQL databases
- Relations Between Tradeoffs
- **Quiz:** Design Tradeoffs (5 questions)

### InterviewReady Fundamentals Test
- **The Big Exam:** 17 questions

---

## 3. High Level Design

### 3.1 Design an Emailing service like Gmail [Link]
- Scope and Requirement setting
- Requirements List
- Chapter #1: Service Registration and Proxies
- Architecture Diagram 1
- **Quiz 1:** 5 questions
- Chapter #2: Authentication & Global Caching
- Architecture Diagram 2
- **Quiz 2:** 3 questions
- Chapter #3: API contracts & Versioning
- Architecture Diagram 3
- **Quiz 3:** 3 questions
- Chapter #4: Sending, Tagging & Searching Emails
- Architecture Diagram 4
- Chapter #5: Contacts & Groups
- Architecture Diagram 5
- **Quiz 4:** 4 questions
- Capacity Estimations
- FAQs
- API Contracts
- **Quiz 5:** 3 questions
- Summary - PDF
- **Design Question:** Gmail Service

### 3.2 Tinder System Design [Link]
- Requirements
- Image Storage: Files vs. Database BLOB
- **Quiz 1:** 3 questions
- Profile Creation and Authentication
- One to One chat messaging
- **Quiz 2:** 3 questions
- Matching right-swiped users
- Serving recommendations to users
- **Quiz 3:** 3 questions
- Architecture Diagram
- **Design Question:** Tinder Recommendations
- Summary - PDF

### 3.3 WhatsApp System Design [Link]
- System Requirements
- One to one messaging
- Last Seen Timestamps
- Group Messaging
- Architecture Diagram
- **Design Question:** WhatsApp Group Chat
- Summary - PDF

### 3.4 Chess Design: Building a highly scalable turn-based gaming website [Link]
- Requirements of a chess website
- Handling connections at scale
- **Quiz 1:** 3 questions
- Consistent Hashing vs. Sharding
- **Quiz 2:** 3 questions
- Connection related thundering herds
- **Quiz 3:** 3 questions
- Request Batching and Conclusion
- Architecture Diagram
- Capacity Planning
- API Contracts
- Summary - PDF
- **Design Question:** Chess Website

### 3.5 Hotstar: Live Video Streaming Design [Link]
- Live Streaming Requirement Breakdown
- Video Ingestion and Transformation
- **Quiz 1:** 3 questions
- Transferring processed videos to end users
- FAQs
- Capacity Planning
- Architecture Diagram
- **Quiz 2:** 3 questions
- Virtual Advertising for live sports events
- **Design Question:** Live Streaming App

### 3.6 Google Docs: Collaborative editor design [Link]
- Google Docs Requirements
- Document Schema
- Storing Documents
- Version History
- Avoiding Thundering Herds in Crons
- Compression and Caching
- Concurrent Writes with Locks
- Operational Transform Overview
- Permission Management
- **Quiz:** 5 questions
- **Design Question:** Google Docs

### 3.7 Design a Cab Aggregator App like Uber [Link]
- Requirements of a cab aggregator
- Static Pricing of Rides
- Ride Matching
- Calculating Estimated Time of Arrival
- Matching Drivers with Live Rides
- **Quiz:** 5 questions
- **Design Question:** Cab Aggregator

### 3.8 Design a Location Based Service like Google Maps [Link]
- Requirements of a Map application
- Routing Challenges in Maps
- Partitioning Algorithm: Splitting the graph into regions
- Finding the shortest path - A* search
- GeoHash and other proximity filters
- Detecting traffic jams and broadcasting updates
- Calculating an accurate and efficient estimated time of arrival
- **Quiz:** 6 questions
- **Design Question:** Google Maps

### 3.9 WhatsApp Calling App [Link]
- Requirements List
- Calling App Design
- Concept #1: Breaking calls into dialogs
- Concept #2: The state machine
- **Quiz 1:** 5 questions
- Concept #3: Charging Users
- Concept #4: Consistent Hashing for caching call state
- Calling App Architecture
- API Contracts
- **Quiz 2:** 4 questions
- FAQs
- Capacity Estimation
- FAQs 2
- **Design Question:** Calling App
- Summary - PDF

### 3.10 Recommendation Engine Design [Link]
- Converting data sources to a lake
- Querying on top of Views over the DB
- Data Lake Interactions
- The Map Reduce Architecture
- Map Reduce Architecture
- Fault tolerance and engineering optimizations
- **Quiz 1:** 3 questions
- Job Scheduler
- Real time analytics
- **Quiz 2:** 3 questions
- Ranking restaurants in real time and batch
- Example: Ranking Restaurants
- **Quiz 3:** 3 questions
- Final Architecture Diagram
- Summary - PDF
- **Design Question:** Recommendation Engine

### Additional System Design Scenarios
*(Detailed design questions and architectures)*

- Design a Reliable Webhook Dispatcher (powered by Kafka) [Link]
- Design a Concurrent History Tracking System (track changes for registered entities) [Link]
- Design a Cache Service (distributed, eviction policies, fault tolerance) [Link]
- Design an Authentication/Authorization Service (OTP, OAuth, etc.) [Link]
- Design an In-Memory Pub-Sub Model (producers, consumers, offsets) [Link]
- Design a Config Manager Service (serve configs to internal/external services) [Link]
- Design a Job Scheduler (accept job + cron expression) [Link]
- Design an API Rate Limiter [Link]
- System that ingests millions of transactions and serves millions of users [Link]
- Design a URL Shortener [Link]
- Design a Notification System (scalability, reliability, availability) [Link]
- Design a Notification Service (multi-channel traffic like SMS/email/push) [Link]
- Design a Leaderboard System (LeetCode-style rankings) [Link]
- Design a Car Parking Application [Link]
- Design a scalable Chat Application (WhatsApp/Slack) [Link]
- Design a News Aggregator [Link]
- Design an Auction Service (Seller lists products, Bidders search via Elasticsearch, Concurrency handling, Notifications) [Link]
- Design a Subscription Model (recurring monthly/yearly payments) [Link]
- Razorpay Subscription Flow (CureFit recurring billing with retries + confirmations) [Link]
- Design a Payment System (like Razorpay/Stripe) [Link]
- Design an E-commerce Checkout System [Link]
- Design a Cab Booking App (like Ola/Uber) [Link]
- Design a Ride-Hailing app (Uber/Ola) [Link]
- Database design for ride-sharing [Link]
- Design a Trending Topic Service (real-time trending content) [Link]
- How would you scale a Video Streaming platform? [Link]
- Data warehouse for an online retailer [Link]
- Fraud detection model for transactions [Link]
- Explain the design of one of your recent projects [Link]

### High Level Design Exam
- **The Big Exam:** 13 questions

---

## 4. Research Paper Analysis

### 4.1 Scaling Memcached at Facebook
- 1. Caching for Social Media
- 1-1. Caching for Social Media - Revision
- 2. Cascading Failures and Code Caches
- 3. Managing consistency across regions
- Lecture Notes PDF

### 4.2 Google's Authorization Service (Zanzibar)
- 1. Motivation and Data Model
- 2. APIs and Google Spanner
- 3. Overall Architecture and Optimizations
- 4. Rate Limiting and Request Collapsing
- Lectures Notes - Zanzibar

### 4.3 Timeseries Databases: Gorilla and Monarch
- 1. What is a time series database?
- 2. Requirements
- 3. Data Schema
- 4. Compression Algorithms
- 5. Persistence
- 6. Tradeoffs - Choosing a time window
- 7. Load Balancing
- 8. Replication and Fault tolerance
- 9. Monarch's architecture
- 10. System features
- 11. Query Optimization
- Livestream: GorillaDB Timeseries database
- Livestream: GorillaDB Timeseries database II
- Lecture Notes Facebook GorillaDB

### 4.4 TAO - An in-memory graph database by Meta
- 1. Usecases and Data Schema
- 2. Data Consistency and evictions
- 3. Cache Features for the graph
- TAO Lecture Notes

### 4.5 Google Dremel - Interactive Analytics
- Google Dremel
- Google Dremel Notes

### 4.6 Apache Kafka
- Kafka Paper Reading - Combined

### 4.7 Apache Spark
- Apache Spark - Combined

### 4.8 Milvus DB
- What are Vectors?
- Vector Indexes - HNSW

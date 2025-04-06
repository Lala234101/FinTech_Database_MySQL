# FinTechLytics - Financial Analytics Database System

# Project Overview

FinTechLytics is a comprehensive financial analytics database system designed to track user portfolios, stock prices, and trading transactions. This project provides a robust backend infrastructure for fintech applications that need to manage user investments, analyze market data, and track trading activity.

# Database Schema Features
* User Management: Track registered users and their account details

* Stock Information: Maintain comprehensive stock metadata including symbols, company names, and sectors

* Market Data: Historical stock price tracking for analysis and reporting

* Transaction System: Record all buy/sell transactions with timestamps

* Portfolio Tracking: Monitor user holdings with average cost calculations

# Database Tables

1. Users Table
* Stores user account information

* Primary Key: user_id

* Includes personal details and account creation timestamp

2. Stocks Table
* Contains stock metadata

* Primary Key: stock_id

* Tracks symbols, company names, sectors, and listing dates

3. StockPrices Table
*Records historical price data

*Primary Key: price_id

* Foreign Key: stock_id (references Stocks table)

* Stores price points with timestamps

4. Transactions Table
* Logs all user trades

* Primary Key: transaction_id

* Foreign Keys: user_id and stock_id

* Trades types (BUY/SELL), quantities, prices, and timestamps

5. Portfolios Table
* Tracks user holdings

* Primary Key: portfolio_id

* Foreign Keys: user_id and stock_id

Maintains current quantities and average purchase prices

# Entity Relationships
Database Schema Diagram

The database features these key relationships:

* Users have many Transactions (One-to-Many)

* Users have many Portfolio entries (One-to-Many)

* Stocks have many StockPrices (One-to-Many)

* Stocks have many Transactions (One-to-Many)

* Stocks have many Portfolio entries (One-to-Many)

# Technical Implementation
* Database System: PostgreSQL

* Schema: flt_schema

* SQL Scripts:

Complete database creation scripts

Table definitions with constraints

Foreign key relationships

Repository Contents
FinTechLyticsDB MySQL.sql: Complete SQL script for database creation

FinTechLytics_Schema_Docs.txt: Detailed documentation of schema structure

FinTechLyticsDB SQL Scripts.txt: Individual table creation scripts

FinTechLyticsDB.drawio.png: Visual database schema diagram

# Setup Instructions
Clone this repository

Execute the SQL scripts in your PostgreSQL environment:

sql
Copy
-- First create the schema
CREATE SCHEMA flt_schema;

-- Then run the table creation scripts
\i FinTechLyticsDB.sql
Potential Applications
Personal finance tracking apps

Investment portfolio management systems

Stock market analysis platforms

Trading journal applications

Financial research databases

License
This project is open-source and available under the MIT License.



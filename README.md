# Amana-Market-Price-Data-
Google- Kaggle Generative AI Learnings and project 2025.
# Amana Market Insights Tool

## Overview
Welcome to the **Amana Market Insights Tool**, a project built in **Google Colab** to empower traders in African markets like Nairobi’s Gikomba. Using **function calling** with the **Gemini API** (inspired by [Kaggle’s Day 3 notebook](https://www.kaggle.com/code/susanngatia/day-3-function-calling-with-the-gemini-api)), this tool helps vendors access **crop pricing data** and **credit insurance** insights for farm produce like maize and tomatoes. It leverages a **synthetic dataset** to simulate market transactions, answering queries like “What’s the price of maize?” or “Is cassava in stock?”

Initially, we aimed to integrate with **Zoho Inventory** for real-time data (April 12, 2025), but shifted to synthetic data for flexibility and testing (April 13, 2025). This repo showcases how AI can guide vendors in setting competitive prices and managing buyer credit risks, aligning with **Co Amana**’s mission to digitize African markets.

## Purpose
The **Amana Market** project supports traders by:
- **Pricing Guidance**: Delivering crop prices (e.g., “Tomatoes at 80.25 Ksh/kg”) to stay competitive.
- **Credit Insurance**: Assessing buyer risks (e.g., “Wholesalers score 75/100, safer”) to reduce losses.
- **Market Insights**: Highlighting trends (e.g., “Onions sell most in Gikomba”) to optimize stock.

This tool is a prototype for Amana’s **Marketplace Insights Tool**, designed for markets in Nigeria and Kenya (per our April 2 pilot focus). It uses AI to make markets smarter, tackling issues like unreliable pricing and unpaid debts (March 26 concerns).

## Dataset
The synthetic dataset, `amana_market_data.csv`, mimics 15 transactions in markets like Gikomba, Kisumu, and Mombasa. It includes:

- **crop_name**: Crop sold (e.g., Maize, Yams).
- **sku**: Unique ID (e.g., MAIZE001).
- **category**: Crop type (Grains, Vegetables, Tubers).
- **price_per_kg**: Price in Ksh (e.g., 120.50).
- **stock_quantity_kg**: Available stock (e.g., 200 kg).
- **units_sold_kg**: Sales volume (e.g., 10 kg).
- **vendor_id**, **vendor_name**: Vendor info (e.g., VEND001, Mama Jane’s Farm).
- **date**, **time**: Transaction timing (e.g., 2025-04-12, 14:30:00).
- **market_location**: Market name (e.g., Kisumu).
- **credit_risk_score**: Buyer risk (0=high, 100=low, e.g., 75).
- **buyer_type**: Buyer category (Wholesaler, Retailer, Local Buyer).

### Why Synthetic Data?
We created this data to reflect African market dynamics (e.g., maize price swings, per March 23 data issues) without needing live systems like Zoho Inventory. It’s safe, flexible, and lets us test Amana’s vision—80% price accuracy and risk management (April 2 goals)—before scaling to real data.

### Data Storage
The CSV is generated in Colab and saved to **Google Drive** for easy access and sharing with Amana’s team or vendors.

## How It Works
The Colab notebook:
1. **Generates `amana_market_data.csv`**: Creates synthetic market data.
2. **Connects to Google Drive**: Saves/loads the CSV.
3. **Uses Gemini API**: Enables function calling to query data.
4. **Defines Functions**:
   - `check_crop_price`: Gets the latest price (e.g., “Maize at 120.50 Ksh/kg”).
   - `check_crop_stock`: Checks stock (e.g., “150 kg of Tomatoes”).
5. **Answers Queries**: Responds to prompts like “What’s the price of onions?” via Gemini.

### Example Outputs
- **Prompt**: “What’s the price of Maize?”
- **Response**: “The latest price for Maize is 120.50 Ksh/kg, recorded on 2025-04-12 at 14:30:00 by Mama Jane’s Farm in Gikomba.”
- **Prompt**: “Is Tomatoes in stock?”
- **Response**: “Yes, Tomatoes are in stock with 150 kg, supplied by Okoth’s Produce in Gikomba.”

## Why We’re Doing This
African markets face challenges (per March 26 initiative):
- **Pricing Confusion**: Vendors lack reliable crop prices, risking losses.
- **Credit Risks**: Unpaid debts hurt small traders (April 11 loan concerns).
- **Tech Gaps**: Low digital tools limit efficiency (April 2 pilot).

This project shows AI’s potential to:
- Offer **real-time prices** (e.g., “Set yams at 200 Ksh/kg”).
- Flag **risky buyers** (e.g., “Retailers score 55, limit credit”).
- Share **insights** (e.g., “Cassava sells less, focus on maize”).

It’s a step toward Amana’s goal of empowering traders with data-driven decisions.

## Getting Started
### Prerequisites
- **Google Colab**: Run the notebook in Colab.
- **Gemini API Key**: Get one from [Google AI Studio](https://aistudio.google.com).
- **Google Drive**: For storing the CSV.
- **GitHub**: Clone this repo to contribute or modify.

### Setup
1. **Clone the Repo**:
   ```bash
   git clone https://github.com/YOUR_USERNAME/amana-market-insights.git
   cd amana-market-insights

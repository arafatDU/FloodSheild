# 🌊 AI-Powered Flood Prediction for Bangladesh
An AI-driven system to provide 15-day advance flood forecasts for 122 river monitoring stations across Bangladesh. This project is developed under the "AI for Bangladesh 2.0" theme, aiming to leverage technology to build a more resilient and secure nation


### Problem Statement
Bangladesh is one of the world's most vulnerable countries to climate change, with recurrent, devastating floods displacing millions, causing over $1 billion in annual economic damages, and resulting in tragic loss of life. Traditional flood warning systems often lack the lead time and geographical precision needed for effective disaster preparedness. This project directly addresses this critical challenge to national security and economic stability.

### Our Solution: An AI-Powered Early Warning System
We have developed a system that uses a sophisticated AI model to predict river water levels 15 days in advance. By training a specialized model for each of the 122 water monitoring stations, our solution provides highly localized and accurate forecasts.

The goal is to provide actionable intelligence to disaster management agencies, local authorities, and the public, enabling them to take proactive measures, save lives, and mitigate economic losses.

System Architecture
Our system follows a modular, multi-stage pipeline:

Data Ingestion: A Python script automatically fetches real-time and historical water level data from the Bangladesh Water Development Board (BWDB) public API endpoint https://api.ffwc.gov.bd/data_load/observed-waterlevel-by-station-and-date/{station_id}/{yyyy-mm-dd}.

Data Preprocessing: The raw 3-hourly data is cleaned, processed, and aggregated into daily average water levels. We enrich this data by engineering features like time-based variables (day of year, month) and lag features to provide historical context for the model.

AI Core (LSTM Models): The heart of our system. We use Long Short-Term Memory (LSTM), a specialized type of neural network perfect for time-series forecasting. A unique LSTM model is trained for each of the 122 stations to learn its specific hydrological patterns.

Prediction & Visualization: The trained models take the last 30 days of data as input to forecast the next 15 days. The output is then visualized on a web-based dashboard, showing a map of Bangladesh with each station color-coded by its predicted flood risk.

## Getting Started

First, run the development server:

```bash
npm run dev
# or
yarn dev
# or
pnpm dev
# or
bun dev
```
AI MODEL For Flood Prediction



You can start editing the page by modifying `app/page.js`. The page auto-updates as you edit the file.

This project uses [`next/font`](https://nextjs.org/docs/basic-features/font-optimization) to automatically optimize and load Inter, a custom Google Font.

## Learn More about the project

To learn more about Next.js, take a look at the following resources:

- [Next.js Documentation](https://nextjs.org/docs) - learn about Next.js features and API.
- [Learn Next.js](https://nextjs.org/learn) - an interactive Next.js tutorial.

You can check out [the Next.js GitHub repository](https://github.com/vercel/next.js/) - your feedback and contributions are welcome!

## Deploy on Vercel

The easiest way to deploy your Next.js app is to use the [Vercel Platform](https://vercel.com/new?utm_medium=default-template&filter=next.js&utm_source=create-next-app&utm_campaign=create-next-app-readme) from the creators of Next.js.

Check out our [Next.js deployment documentation](https://nextjs.org/docs/deployment) for more details.

## flood detection

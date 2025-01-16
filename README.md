# Rumi Chat
## Overview
The Rumi Chat visualization system allows users to interact with various data visualizations through natural language queries. The system supports multiple visualization types including line charts, pie charts, bar charts, tables, and rich text content.

# Installation

To install the project dependencies, follow these steps:

```
cd Rumi_Chat
npm install
npm run dev
```


Open your browser and navigate to http://localhost:5173. You should see the app running. Any changes you make to the source files will automatically be reflected in the browser.

## Available Visualizations

### 1. Sales Trends
**Query Examples:**
- "Show me sales trends"
- "Display sales over time"
- "What are the sales trends for the last 6 months?"

**Returns:** A line chart showing monthly sales data from January to June.

### 2. Revenue Distribution
**Query Examples:**
- "Show revenue distribution"
- "Display revenue distribution across products"

**Returns:** A pie chart showing revenue distribution across Products A-D and Others.

### 3. Customer Demographics
**Query Examples:**
- "Show customer demographics"
- "Display customer age groups"
- "What are our customer demographics?"

**Returns:** A table showing customer distribution across age groups with counts and percentages.

### 4. Performance Comparison
**Query Examples:**
- "Show performance vs target"
- "Display quarterly performance"
- "How are we performing against targets?"

**Returns:** A bar chart comparing actual performance against targets for each quarter.

### 5. Key Metrics
**Query Examples:**
- "Show key metrics"
- "Display KPIs"
- "What are our key performance indicators?"

**Returns:** A formatted text display showing key metrics including revenue, growth, and satisfaction scores.

### 6. Media Gallery
**Query Examples:**
- "Show company events"
- "Display media gallery"
- "Show me recent company events"
- "Display images"

**Returns:** An image gallery showing recent company events with captions.

### 7. Quarterly Report
**Query Examples:**
- "Show quarterly report"
- "Display Q2 summary"
- "Show me the latest report"

**Returns:** A rich text document containing the quarterly report with formatting and embedded media.



## Error Handling
- If no matching visualization is found for a query, the system returns `null`
- All queries are case-insensitive for better user experience



## Supported Visualization Types
- `line-chart`: Temporal data visualization
- `pie-chart`: Proportional data visualization
- `bar-chart`: Comparative data visualization
- `table`: Structured data presentation
- `text`: Formatted text content
- `images`: Media gallery

## Project Structure
```
├─ src/
│   ├─ components/     # Contains reusable UI components
│   │   ├─ visualizations/  # Contains visualization components
│   │   │   ├─ Charts.jsx
│   │   │   ├─ DataTable.jsx
│   │   │   ├─ MediaDisplay.jsx
│   │   │   ├─ RichTextRenderer.jsx
│   │   │   └─ VisualizationRenderer.jsx
│   ├─ data/           # Contains mock data and data-related utilities
│   │   ├─ mockVisualizations.js
│   ├─ pages/          # Contains individual page components
│   ├─ layouts/        # Contains layout components for structuring pages
│   ├─ app.jsx         # Main app component that wraps routes and layout
│   ├─ routes.jsx      # Defines application routes and their corresponding components
│   └─ main.jsx        # Entry point of the application, where the app is rendered
├─ public/             # Contains public assets like index.html and favicon
├─ tests/              # Contains test files for the application
├─ .gitignore          # Specifies files and folders to be ignored by Git
├─ LICENSE             # License information for the project
├─ package.json        # Project dependencies and scripts
├─ README.md           # Project documentation
├─ vercel.json         # Vercel config for production
└─ vite.config.js      # Configuration for Vite build and dev server

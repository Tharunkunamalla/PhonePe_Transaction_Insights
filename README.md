# PhonePe Transaction Insights 📊

A comprehensive data analytics and visualization project that extracts, processes, and visualizes PhonePe Pulse transaction data using Python, MySQL, and Streamlit.

## 📝 Project Overview

This project provides interactive insights into PhonePe's digital payment ecosystem across India. It processes large-scale transaction data, stores it in a MySQL database, and presents it through an intuitive Streamlit dashboard with various analytics views and geographical visualizations.

## ✨ Features

- **Data Extraction**: Automated extraction of PhonePe Pulse data from JSON files
- **Database Management**: MySQL database integration for efficient data storage and retrieval
- **Interactive Dashboard**: Multi-page Streamlit application with the following views:
  - Overview: High-level metrics and trends
  - State-wise Analysis: Regional transaction patterns
  - Aggregated Insurance: Insurance transaction insights
  - Top Users: User engagement metrics
  - KPIs & Metrics: Key performance indicators
  - Geo Visualization: Interactive geographical maps
  - Download CSVs: Export data for further analysis
- **Data Visualization**: Interactive charts and graphs using Plotly
- **Real-time Queries**: Dynamic SQL queries for on-demand analytics

## 🔧 Prerequisites

- Python 3.7 or higher
- MySQL Server
- Git

## 📦 Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/Tharunkunamalla/PhonePe_Transaction_Insights.git
   cd PhonePe_Transaction_Insights
   ```

2. **Install required packages**
   ```bash
   pip install -r requirements.txt
   ```

3. **Set up MySQL database**
   - Ensure MySQL server is running
   - Update database credentials in `Phone_pe/Sql_scripts/db_connect.py`

4. **Extract and load data**
   ```bash
   # Extract data from PhonePe Pulse
   cd Phone_pe/Scripts
   python extract_data.py
   
   # Create database tables
   cd ../Sql_scripts
   python create_tables.py
   
   # Load data into MySQL
   python insert_data.py
   ```

## 🚀 Usage

1. **Launch the Streamlit dashboard**
   ```bash
   cd Phone_pe/streamlit_app
   streamlit run app.py
   ```

2. **Access the dashboard**
   - Open your web browser and navigate to `http://localhost:8501`
   - Use the sidebar to navigate between different views
   - Interact with charts and filters to explore the data

## 📁 Project Structure

```
PhonePe_Transaction_Insights/
├── Phone_pe/
│   ├── Data/
│   │   └── phonepe_extracted.csv
│   ├── Scripts/
│   │   └── extract_data.py
│   ├── Sql_scripts/
│   │   ├── db_connect.py
│   │   ├── create_tables.py
│   │   ├── insert_data.py
│   │   ├── load_dataframes.py
│   │   └── all_sql.py
│   ├── streamlit_app/
│   │   ├── app.py
│   │   ├── utils.py
│   │   ├── india_states.geojson
│   │   ├── phonepe.png
│   │   └── transac.png
│   ├── phonepe_extracted_csv/
│   ├── pulse/
│   └── phonepe_Transactions_Insights.ipynb
├── requirements.txt
└── README.md
```

## 🛠️ Technologies Used

- **Python**: Core programming language
- **Streamlit**: Web application framework for the dashboard
- **MySQL**: Database management system
- **Pandas**: Data manipulation and analysis
- **NumPy**: Numerical computing
- **Plotly**: Interactive data visualization
- **Matplotlib & Seaborn**: Statistical visualization
- **Scikit-learn**: Machine learning utilities
- **SciPy**: Scientific computing

## 📊 Data Sources

This project uses data from [PhonePe Pulse](https://github.com/PhonePe/pulse), which provides aggregated transaction and user data across India.

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## 📄 License

This project is open source and available for educational and research purposes.

## 👨‍💻 Author

Tharun Kunamalla

## 🙏 Acknowledgments

- PhonePe for providing the Pulse data
- Streamlit community for excellent documentation and support

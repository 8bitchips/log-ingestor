# Log Ingestor and Query Interface

This application serves as a log ingestor and provides a user-friendly query interface for log retrieval.


## Overview

This Flask application provides a web-based log ingestor and a query interface to efficiently handle log data. Logs are stored in a PostgreSQL database, and the application supports features such as log ingestion over HTTP and log querying with various filters.

<img src="1.JPG">

<img src="2.JPG">


## Getting Started

### Prerequisites

- [Python](https://www.python.org/) (version 3.x)
- [PostgreSQL](https://www.postgresql.org/) database
- [PIP](https://pypi.org/project/pip/)

### Installation

1. Clone the repository:
2. git clone https://github.com/yourusername/log-ingestor.git
3. Install the required dependencies:
4. cd log-ingestor
5. pip install -r requirements.txt
6. Set up the PostgreSQL database and configure the connection string in app.py:
7. app.config['SQLALCHEMY_DATABASE_URI'] = 'postgresql://your_username:your_password@your_host/your_database?sslmode=require'
8. Run the application:
9. python app.py

### Usage
Log Ingestion
Logs can be ingested by sending a POST request to the /ingest endpoint. Use the following JSON format for log data:

- Log Querying
Query logs using a GET request to the /query endpoint. Various filters and pagination are supported. See the Sample Queries section for examples.

- User Interface
Access the user interface by visiting the /query_ui endpoint. This provides a simple HTML-based interface for querying logs.

- Configuration
Adjust the configuration settings in app.py to suit your requirements. Ensure that the PostgreSQL database connection string is correctly set.

- Advanced Features
The application supports advanced features such as search within specific date ranges, regular expressions for search, combining multiple filters, real-time log ingestion, and role-based access to the query interface.

- Database Schema
The PostgreSQL database schema is defined in the Log model in app.py. Ensure that the database is created with the required tables before running the application.

- Contributing
Contributions are welcome! Feel free to open issues or pull requests.

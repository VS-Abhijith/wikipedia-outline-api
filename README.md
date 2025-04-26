
---

# **FastAPI Country Outline Scraper**

This project is a simple **FastAPI** web application that scrapes Wikipedia pages to extract the outline (headings) of a country’s page. It uses **BeautifulSoup** for HTML parsing and **httpx** for asynchronous HTTP requests. The application provides an API endpoint to fetch the outline of a given country.

## 🛠️ **Technologies Used**
- **FastAPI**: Modern web framework for building APIs with Python.
- **BeautifulSoup**: Python library for parsing HTML and extracting data.
- **httpx**: Asynchronous HTTP client for Python.
- **CORS**: Cross-Origin Resource Sharing middleware to enable safe cross-origin requests.

## 🚀 **Features**
- Fetches the outline of a country's Wikipedia page.
- Displays a structured list of headings (h1, h2, h3, etc.) from the page.
- Supports **asynchronous** requests for better performance.
- Allows cross-origin requests (CORS enabled).

## 📡 **API Endpoint**

### `/api/outline`

**Method**: `GET`

**Query Parameters**:
- `country` (str): The name of the country whose outline you want to fetch.

**Response**:  
Returns the outline of the country's Wikipedia page in Markdown format.

**Example Request**:  
```
GET http://localhost:8000/api/outline?country=India
```

**Example Response**:  
```json
{
  "outline": "## Contents\n\n# India\n\n### History\n\n### Geography\n\n### Economy\n\n"
}
```

## 🚀 **Installation**

### Prerequisites
- Python 3.7+
- Pip (Python package manager)

### Steps
1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/fastapi-country-outline.git
   cd fastapi-country-outline
   ```

2. Create and activate a virtual environment (optional but recommended):
   ```bash
   python -m venv venv
   source venv/bin/activate  # For Linux/macOS
   venv\Scripts\activate  # For Windows
   ```

3. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```

4. Run the FastAPI app:
   ```bash
   uvicorn main:app --reload
   ```

   The app will run at `http://localhost:8000`.

## 📄 **Project Structure**
```plaintext
/fastapi-country-outline
│
├── main.py           # FastAPI application code
├── requirements.txt  # List of required dependencies
└── README.md         # Project documentation
```

## 📝 **Requirements**
- `fastapi`: Web framework for building APIs.
- `httpx`: For making asynchronous HTTP requests.
- `beautifulsoup4`: For scraping and parsing HTML.
- `uvicorn`: ASGI server to run the FastAPI app.

### Install requirements:
```bash
pip install fastapi httpx beautifulsoup4 uvicorn
```

## ⚙️ **Running the App**

To run the app locally, use:

```bash
uvicorn main:app --reload
```

Then, you can access the API endpoint by visiting:
```
http://localhost:8000/api/outline?country=CountryName
```

Example:  
```bash
GET http://localhost:8000/api/outline?country=France
```

## 🧑‍💻 **Contributing**
Feel free to fork this repository and open a pull request with any improvements or bug fixes!

## 📑 **License**
This project is licensed under the MIT License.

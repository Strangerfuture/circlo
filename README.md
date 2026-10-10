# circlo

A lightweight social networking application built with **FastAPI, Streamlit, and Python**, featuring a separate backend API and interactive web frontend.

## Tech Stack

- **Python** — Core programming language
- **FastAPI** — Asynchronous backend API
- **Streamlit** — Interactive web frontend
- **SQLAlchemy** — Database operations and ORM
- **ImageKit** — Image handling and hosting integration

## Architecture

The application separates the frontend from the backend:

- **Frontend:** Streamlit provides the user interface and communicates with the API using HTTP requests.
- **Backend:** FastAPI handles API endpoints, request validation, authentication, file uploads, and application logic.
- **Database:** SQLAlchemy manages database access and asynchronous database sessions.
- **Image handling:** ImageKit integration supports image-related functionality.

## Project Structure

```text
circlo/
├── app/
│   ├── db.py
│   ├── images.py
│   ├── schemas.py
│   └── users.py
├── frontend.py
├── main.py
├── pyproject.toml
├── requirements.txt
└── uv.lock
```

## Getting Started

### Prerequisites

- Python
- pip or [uv](https://docs.astral.sh/uv/)
- Required database and ImageKit configuration

### 1. Clone the Repository

```bash
git clone https://github.com/Strangerfuture/mini_social.git
cd circlo
```

### 2. Install Dependencies

Using pip:

```bash
pip install -r requirements.txt
```

Or using uv:

```bash
uv sync
```

### 3. Configure Environment Variables

Configure the database connection, authentication settings, and ImageKit credentials required by the application. Keep secret keys and credentials out of version control.

### 4. Start the Backend

If `main.py` defines the FastAPI application as `app`:

```bash
uvicorn main:app --reload
```

The API will typically be available at `http://127.0.0.1:8000`.

Interactive API documentation is usually available at `http://127.0.0.1:8000/docs`.

### 5. Start the Frontend

In a separate terminal, run:

```bash
streamlit run frontend.py
```

Streamlit will display the local frontend URL, usually `http://localhost:8501`.

## Development

The backend uses asynchronous database sessions and Pydantic schemas to support structured request validation and database operations. The Streamlit frontend communicates with the API to provide the web interface.


Developed by [Strangerfuture](https://github.com/Strangerfuture).

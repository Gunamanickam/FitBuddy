# FitBuddy – AI Fitness Plan Generator

FitBuddy is an AI-powered fitness planning web application built with:

- FastAPI
- Jinja2
- SQLite
- SQLAlchemy
- Google Gemini
- HTML
- CSS
- Pydantic

## Features

- Personalized 7-day workout plans
- Nutrition and recovery tips
- Feedback-based workout plan updates
- SQLite database
- Admin dashboard
- REST API
- FastAPI Swagger documentation
- Gemini AI integration
- Demo fallback if Gemini API key is not configured

## Installation

Create virtual environment:

Windows:

python -m venv venv

Activate:

venv\Scripts\activate

Install packages:

pip install -r requirements.txt

## Environment

Create `.env`:

GEMINI_API_KEY=YOUR_GEMINI_API_KEY

GEMINI_WORKOUT_MODEL=gemini-3.8-flash

GEMINI_FAST_MODEL=gemini-3.5-flash-lite

DATABASE_URL=sqlite:///./fitbuddy.db

APP_NAME=FitBuddy

DEBUG=true

## Run

uvicorn app.main:app --reload

## Open

Website:

http://127.0.0.1:8000

API documentation:

http://127.0.0.1:8000/docs

Admin:

http://127.0.0.1:8000/view-all-users

Health:

http://127.0.0.1:8000/api/health

## Workflow

1. Open the website.
2. Enter user information.
3. Select a fitness goal.
4. Select workout intensity.
5. Click Generate My 7-Day Plan.
6. Review the workout plan.
7. Review the nutrition/recovery tip.
8. Submit feedback.
9. FitBuddy generates an updated plan.
10. Open Admin View to see stored users.

## API

POST /api/generate-workout

POST /api/submit-feedback

GET /api/users

GET /api/users/{user_id}

GET /api/health
# FastAPI Playwright Screenshot API

FastAPI service using Playwright and Chromium.

## Endpoints

### Health

GET /health

Example:

/health

Response:

{
    "status": "healthy"
}

### Screenshot

GET /screenshot

Parameters:

- pfp_url
- change_

Example:

/screenshot?pfp_url=https://leetcode.com/u/example&change_=1

The endpoint streams newline-delimited JSON containing progress
updates and the final base64-encoded screenshot.

## Local development

Install dependencies:

pip install -r requirements.txt

Install Playwright browsers:

playwright install chromium

Run:

uvicorn main:app --reload

## Docker

Build:

docker build -t playwright-api .

Run:

docker run -p 10000:10000 playwright-api

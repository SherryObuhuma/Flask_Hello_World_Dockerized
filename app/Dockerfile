# Official Python image
FROM python:3.11-slim 

# Set working directory
WORKDIR /app

#Copy requirements
COPY requirements.txt .

#Install dependencies
RUN pip install --no-cache-dir -r requirements.txt

# Copy the app code 
COPY . .

# Run with gunicorn

EXPOSE 5000
CMD ["gunicorn", "-b", "0.0.0.0:5000", "blog:app"]
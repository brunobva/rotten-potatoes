FROM python:3.8-slim-buster
WORKDIR /bva
COPY requirements.txt /bva
RUN python -m pip install -r requirements.txt
COPY . /bva
EXPOSE 7700
CMD ["gunicorn", "--workers=3", "--bind", "0.0.0.0:7700", "app:app" ]
# FLASK-PG-REDIS (Hands on live class)

## Create Virtual Environment for Linux

```bash
python3 -m venv my_env
```

## Activate Virtual Environment

```bash
source my_env/bin/activate
```

## Install Dependecies

```bash
pip3 install -r requirements.txt
```


## Database Technologies

- <i>PostgreSQL: A powerful relational database management system that provides robust data storage and querying capabilities.</i>

<p>Install postgres and in order to access postgress locally required connection string is given below :</p>

```bash
postgresql://postgres:admin@localhost:5432/poridhi
```
<p>Postgres shell access:</p>

```bash
psql -h localhost -p 5432 -U postgres
```

## Create Database

```sql
create database poridhi
```

## Databse Query

```sql
select * from tablename
```

- <i>Redis: An in-memory data structure store that can be used as a database, cache, and message broker.</i>

<p>In order to start a redis server, we used an image of redis and used docker. Build a redis image and run at port 6379</p>

<code>docker run -p 6379:6379 --name my-redis-container -d redis</code>

## Database Initialize
```python
flask db init
```

## Database Migration

```python
flask db stamp head  # To set the revision in the database to the head.
flask db migrate -m "<migration message (optional)>"  # To detect automatically all the changes.
flask db upgrade  # To apply all the changes.
```

## Run Application

<code>python3 run.py</code>

## Test
<p>Visit [http://127.0.0.1:5000](http://127.0.0.1:5000) to check if things are okay or not.</p>


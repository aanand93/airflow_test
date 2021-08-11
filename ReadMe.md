## Apache Airflow 2.0 set up.

1. Check local python3 version:

```
$ python3 --version
```

2. Create a python3 environment and launch it:

```
$ pipenv shell
```

3. install airflow locally (change the python dependecy to match your local python3 version (mine is 3.9))

```
$ pip install 'apache-airflow==2.1.2' \
 --constraint "https://raw.githubusercontent.com/apache/airflow/constraints-2.1.2/constraints-3.9.txt"
```

4. Indicate the path of aiflow home:

```
$ export AIRFLOW_HOME=.
```

5. Initialise the databse for airflow:

```
$ airflow db init
```

6. Create an Admin user for airflow webserver:

```
$ airflow users create --username admin --firstname firstname --lastname lastname --role Admin --email admin@domain.com
```

7. start the airflow webserver:

```
$ airflow webserver -port 8080
```

8. open another terminal and start airflow scheduler:

```
$ airflow scheduler
```

9. Open broweser and type '0.0.0.0:8080' to see airflow UI.

## Airflow Documentation

- https://airflow.apache.org/docs/apache-airflow/stable/index.html

## Apache Airflow 2.0 GitHub

- https://github.com/apache/airflow

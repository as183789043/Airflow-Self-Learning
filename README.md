## Quick Start 
```bash
git clone https://github.com/as183789043/Airflow-Self-Learning.git
cd Airflow-Self-Learning
docker compose up -d  #port 8080  user:airflow password:airflow
``` 


## IF you Want Check Monitor 
```bash
docker compose --profile flower up -d  #port 5555
```

## DAGs Overview

| Python File    | Description                                      | Notes                                                                |
| -------------- | ------------------------------------------------ | -------------------------------------------------------------------- |
| `parallel_dag` | A simple DAG that runs tasks in parallel         |                                                                      |
| `user_process` | Demonstrates an HTTP sensor to retrieve and process data | Includes a database connection configured via the Airflow UI         |
| `producer`     | Demonstrates dataset changes                     | Works in conjunction with the `consumer` DAG                         |
| `consumer`     | Processes data when a dataset change is detected | Pairs with the `producer` DAG                                        |
| `group_dag`    | Aggregates multiple tasks into a single group for easier management | Custom functions are located in the `group` directory               |
| `xcom_dag`     | Demonstrates data passing between tasks via XComs | Uses custom functions with parameters `ti` and returns task IDs to trigger the next task |
| `elastic_dag`  | Demonstrates the use of a custom plugin in a DAG | Requires a connection setup in the Airflow UI; custom plugin functions are located in the `plugins` directory |

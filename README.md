# RDD Creation and Transformation using PySpark

## Overview
This repository demonstrates how to create and transform Resilient Distributed Datasets (RDDs) using **Apache PySpark**. RDDs are fundamental data structures in Spark, allowing distributed data processing at scale.

## Features
- Different ways to create RDDs in PySpark
- Various transformation operations such as **map**, **filter**, **flatMap**, **reduceByKey**, and more
- Real-world examples showcasing the power of RDDs
- Sample dataset for hands-on learning

## Prerequisites
To run the code in this repository, ensure you have the following installed:

- Python (>= 3.7)
- Apache Spark (>= 3.0)
- PySpark library

### Installation
You can install PySpark using pip:
```sh
pip install pyspark
```

## Getting Started
Clone this repository and navigate into the project directory:
```sh
git clone https://github.com/yourusername/RDD-Creation-and-Transformation-using-PySpark.git
cd RDD-Creation-and-Transformation-using-PySpark
```

### Running the Examples
To run the PySpark scripts:
```sh
spark-submit rdd_example.py
```
Alternatively, if using Jupyter Notebook, start the notebook:
```sh
jupyter notebook
```
Then open `RDD_Creation_and_Transformation.ipynb` and run the cells.

## Example RDD Operations
### Creating an RDD
```python
from pyspark.sql import SparkSession

spark = SparkSession.builder.appName("RDD Example").getOrCreate()
data = ["apple", "banana", "cherry", "date"]
rdd = spark.sparkContext.parallelize(data)
print(rdd.collect())
```

### Applying a Transformation
```python
upper_rdd = rdd.map(lambda x: x.upper())
print(upper_rdd.collect())
```

## Project Structure
```
.
├── data/                     # Sample dataset (if any)
├── notebooks/                # Jupyter Notebooks for step-by-step execution
├── scripts/                  # Python scripts for RDD operations
├── README.md                 # Project documentation
└── requirements.txt          # List of dependencies
```

## Contributing
Contributions are welcome! Please follow these steps:
1. Fork the repository
2. Create a new branch (`feature-branch`)
3. Commit your changes (`git commit -m "Added new RDD example"`)
4. Push to the branch (`git push origin feature-branch`)
5. Create a Pull Request

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Contact
For any questions or suggestions, feel free to open an issue or reach out on [LinkedIn](https://www.linkedin.com/in/your-profile).


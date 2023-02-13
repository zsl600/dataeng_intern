# DSAID Data Engineering Technical Test

This test is split into 2 sections, **data pipelines**, **databases**

## Submission Guidelines
Please create a Github repository containing your submission and send us an email containing a link to the repository.

Dos:
- Frequent commits
- Descriptive commit messages
- Clear documentation
- Comments in your code

Donts:
- Only one commit containing all the files
- Submitting a zip file
- Sparse or absent documentation
- Code which is hard to read

## Section 1: Data Pipelines
The objective of this section is to design and implement a solution to process a data file. Assume that there are 2 data files `dataset1.csv` and `dataset2.csv`, design a solution to process these files. The expected output of the processing task is a CSV file including a header containing the field names.

Please provide documentation (a markdown file will help) to explain your solution.

Processing tasks:
- Split the `name` field into `first_name`, and `last_name`
- Remove any zeros prepended to the `price` field
- Delete any rows which do not have a `name`
- Create a new field named `above_100`, which is `true` if the price is strictly greater than 100

*Note: please submit the processed dataset too.*

## Section 2: Databases
You are appointed by a car dealership to create their database infrastructure. There is only one store. In each business day, cars are being sold by a team of salespersons. Each transaction would contain information on the date and time of transaction, customer transacted with, and the car that was sold. 

The following are known:
- Each car can only be sold by one salesperson.
- There are multiple manufacturers’ cars sold.
- Each car has the following characteristics:
- Manufacturer
- Model name
- Serial number
- Weight
- Price

Each sale transaction contains the following information:
- Customer Name
- Customer Phone
- Salesperson
- Characteristics of car sold

Set up a PostgreSQL database using the base `docker` image [here](https://hub.docker.com/_/postgres) given the above. We expect at least a `Dockerfile` which will stand up your database with the DDL statements to create the necessary tables. Produce entity-relationship diagrams as necessary to illustrate your design.

Your team also needs you to query some information from the database that you have designed. You are tasked to write a `sql` statement for each of the following task:

1) I want to know the list of our customers and their spending.

2) I want to find out the top 3 car manufacturers that customers bought by sales (quantity) and the sales number for it in the current month.

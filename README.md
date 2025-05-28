# 10a [Individual] Document A Database

**Type**: Individual

Use a **tool** to document any database.


# MySQL Dump Documentation

Dumping a database schema captures its structure and data, providing a clear reference for design, troubleshooting, and restoration.

## How to execute dumping

In the terminal use the command:

```sh
python dump_mysql.py
```

Or to do the same without the dump_mysql.py script, within a **GitBash** terminal:

```bash
$ mysqldump --user=<MYSQL_DB_USER> --password=<MYSQL_DB_PASSWORD> --host=localhost --port=3306 --no-tablespaces kea_cars_dev > mysql-dump/dump_$(date +%s).sql
```

How to dump my MongoDB database of kea_cars_customer_dev, within a **GitBash** terminal:

```bash
$ mongodump --uri="mongodb://adminUser:adminPassword@localhost:27017/kea_cars_customer_dev?authSource=admin" --out=backup_folder
```

To restore the MongoDB datase kea_cars_customer_dev, use this command:

```bash
$ mongorestore --uri="mongodb://adminUser:adminPassword@localhost:27017/kea_cars_customer_dev?authSource=admin" backup_folder/kea_cars_customer_dev
```

# EER Diagram Documentation

An Enhanced Entity-Relationship Diagram (EERD) visually represents a database's structure, showing entities, attributes, and relationships.

This can be seen in the [EERD_kea_cars_dev.png](EERD_kea_cars_dev.png)

<details>
  <summary>Click to view the EER Diagram</summary>

  ![EER Diagram](EERD_kea_cars_dev.png)

</details>

## How to generate an EER diagram using **MySQL Workbench**

Open MySQL Workbench > Database > Reverse Engineer > follow wizard 

File > Export > Export as PNG > Pick folder to save PNG of the EERD


# MRO Documentation (Model Relations to Objects) 

## Using MRO with `npx`

```bash
cd mro
npx mro generate
```

## How MRO Helps Document a Database


1. **HTML File**: [`mro/kea_cars_dev_mro_docs.html`](mro/kea_cars_dev_mro_docs.html)
   
2. **JSON File**: [`mro/kea_cars_dev.json`](mro/kea_cars_dev.json)

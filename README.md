# TiDB Example - Java JDBC

## Initial database and table

Use [dbinit.sql](src/main/resources/dbinit.sql) to create `bank` database and `accounts` table.

```sql
SET sql_safe_updates = FALSE;

USE mysql;
DROP DATABASE IF EXISTS bank;
CREATE DATABASE IF NOT EXISTS bank;

USE bank;

CREATE TABLE accounts (
    `id` VARCHAR(36),
    `balance` INTEGER,
	PRIMARY KEY (`id`)
);
```

## Install maven

If you have configured `Maven`, skip this part.

To install Maven on macOS, run the following command:

```brew install maven```

To install Maven on a Debian-based Linux distribution like Ubuntu:

```apt-get install maven```

To install Maven on a Red Hat-based Linux distribution like Fedora:

```dnf install maven```

For other ways to install Maven, see its official [documentation](https://maven.apache.org/install.html).

## Build 

Note: It will taken sooooo long when you first time run it, must be patience

```mvn clean package```

## Run

```java -jar target/tidb-example-java-jdbc-0.0.1-jar-with-dependencies.jar```
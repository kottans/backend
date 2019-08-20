[![MIT Licensed][icon-mit]][license]
[![Awesome][icon-awesome]][awesome]
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;

# Relational Databases Basics

## Theory

- [Introduction To DBMS](https://www.minigranth.com/dbms-tutorial/dbms-introduction/)
- [Intro to Relational Databases](https://www.udacity.com/course/intro-to-relational-databases--ud197)
- [How does a relational database work](http://coding-geek.com/how-databases-work/)
- [CodeCademy Learn SQL](https://www.codecademy.com/learn/learn-sql)
- [SQL Introduction](https://www.minigranth.com/sql-tutorial/sql-introduction/)
- [CodeCademy Table Transformation](https://www.codecademy.com/learn/sql-table-transformation)
- [CodeCademy SQL analyzing Business Metrocs](https://www.codecademy.com/learn/sql-analyzing-business-metrics)
- [Intro to SQL: Querying and managing data](https://www.khanacademy.org/computing/computer-programming/sql)

## Practical Task

1. Seed data is data that you populate the database with at the time it is created. Assume that the following script was used to create tables and produce seed data:

```sql
CREATE TABLE IF NOT EXISTS `person` (
    `id` INT AUTO_INCREMENT PRIMARY KEY,
    `first_name` VARCHAR(255) NOT NULL,
    `last_name` VARCHAR(255) NOT NULL,
    `created_at` DATETIME DEFAULT NOW(),
    `updated_at` DATETIME DEFAULT NOW()
)  ENGINE=INNODB;

CREATE TABLE IF NOT EXISTS `item` (
    `id` INT AUTO_INCREMENT PRIMARY KEY,
    `name` VARCHAR(255) NOT NULL,
    `price` DECIMAL(5,2) DEFAULT 0,
    `created_at` DATETIME DEFAULT NOW(),
    `updated_at` DATETIME DEFAULT NOW()
)  ENGINE=INNODB;

CREATE TABLE IF NOT EXISTS `order` (
    `id` INT AUTO_INCREMENT PRIMARY KEY,
    `person_id` INT NOT NULL REFERENCES `person`(`id`),
    `created_at` DATETIME DEFAULT NOW(),
    `updated_at` DATETIME DEFAULT NOW()
)  ENGINE=INNODB;

CREATE TABLE IF NOT EXISTS `order_item` (
    `id` INT AUTO_INCREMENT PRIMARY KEY,
    `order_id` INT NOT NULL REFERENCES `order`(`id`),
    `item_id` INT NOT NULL REFERENCES `item_id`(`id`),
    `quantity` INT DEFAULT 1,
    `discount` DECIMAL(5,2) DEFAULT 0,
    `created_at` DATETIME DEFAULT NOW(),
    `updated_at` DATETIME DEFAULT NOW()
)  ENGINE=INNODB;

INSERT INTO `person`(`first_name`, `last_name`) VALUES
    ('Ann', 'Peterson'),
    ('Josh', 'Harris'),
    ('Sarah', 'Connor'),
    ('James', 'Ball');

INSERT INTO `item`(`name`, `price`) VALUES
    ('TV', 299.99),
    ('Carrot', 1.25),
    ('Patrol', 1.41),
    ('Soap', 0.4),
    ('Football Tickets', 149),
    ('T-Shirt', 19.1),
    ('Playstation 4 Pro', 419.99);

INSERT INTO `order`(`person_id`) VALUES
    (1),
    (2),
    (4),
    (4);

INSERT INTO `order_item`(`order_id`, `item_id`, `quantity`, `discount`) VALUES
    (1, 3, 4, 0),
    (1, 6, 1, 0),
    (2, 1, 1, 11.2),
    (2, 7, 1, 15.99),
    (3, 4, 3, 0),
    (3, 2, 8, 0),
    (3, 6, 1, 0),
    (4, 5, 1, 1.49);
```

2. Create folder called `sql_basics` in
   your `kottans-backend` repo

3. In `sql_basics` folder create file called `select.sql` and write SQL SELECT statement to get following output:

| first_name | last_name | total_orders | total_items_bought | total_money_spent |
| ---------- | --------- | ------------ | ------------------ | ----------------- |
| Ann        | Peterson  | 1            | 5                  | 24.74             |
| Josh       | Harris    | 1            | 2                  | 692.79            |
| Sarah      | Connor    | 0            | null               | null              |
| James      | Ball      | 2            | 13                 | 177.81            |

4. Note that discount column value reduces order_item price **for each** item.
5. Use [DB Fiddle](https://www.db-fiddle.com/f/xceugd67tNjdx7PSHVr4qw/0) for practice.

## Done?

➡️ Go forward to [Language-specific Topics: Part II](language_basics_2.md)

⤴️ Back to [Contents](../contents.md)

[icon-chat]: https://img.shields.io/badge/chat-on%20telegram-blue.svg
[icon-mit]: https://img.shields.io/badge/license-MIT-blue.svg
[icon-awesome]: https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg
[license]: https://github.com/Kottans/web/blob/master/LICENSE.md
[awesome]: https://github.com/sindresorhus/awesome

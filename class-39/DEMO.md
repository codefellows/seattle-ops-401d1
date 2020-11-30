# Sample SQL Demo Code

Structured query language (SQL) is a domain-specific language used to design, manipulate, and view data in a relational database management system (RDBS). Reference these code samples below to help you with today's lab.

## SQL Fiddle Schema

Paste this schema code into [SQL Fiddle](sqlfiddle.com) for a free, quick, and disposable SQL reference lab similar to repl.it for other code languages.

```sql

-- Create a produce lines table
CREATE TABLE IF NOT EXISTS `product_lines` (
  `id` int(6) unsigned NOT NULL,
  `line` varchar(50) NOT NULL,
  `desc` varchar(200) NOT NULL,
  PRIMARY KEY (`id`)
) DEFAULT CHARSET=utf8;

-- Create a product details table
CREATE TABLE IF NOT EXISTS `products` (
  `id` int(6) unsigned NOT NULL,
  `price` float(4) unsigned NOT NULL,
  `desc` varchar(200) NOT NULL,
  PRIMARY KEY (`id`)
) DEFAULT CHARSET=utf8;

-- Populate the product lines table with records
INSERT INTO `product_lines` (`id`, `line`, `desc`) VALUES
  ('1', 'Tools', 'Every vulnerable web site is a hardware shop'),
  ('2', 'Deli', 'Can I get a fish sandwich?'),
  ('3', 'Produce', 'Healthy stuff you should probably be eating'),
  ('4', 'Apparel', 'Men\'s and women\'s clothing totally made in the US');

-- Populate the product details table with records
INSERT INTO `products` (`id`, `price`, `desc`) VALUES
  ('1001', '9.99', 'Hammer'),
  ('1002', '9.99', 'Saw'),
  ('1003', '9.99', 'Wrench'),
  ('1004', '9.99', 'Crowbar');

```

## SQL Commands

Here are the SQL syntax for basic commands. You'll need to get comfortable with these for today's lab, which involves SQL injection. Try crafting your own queries in SQL Fiddle.
 
View data with the SELECT command

```sql
SELECT
(column_name_1, column_name_2)
FROM
your-table-name
```

Add new data into a table with the INSERT command

```sql
INSERT INTO
"your-table-name"
(column_name_1, column_name_2)
VALUES
(value_for_column_name_1, value_for_column_name_2)

```

Revise existing data with the UPDATE command

```sql
UPDATE
Products
SET
column_name_2 = new_value
WHERE
Column_name_1 = some_value
```

Return results of two or more SELECT statements
- Each SELECT statement within UNION must have the same number of columns
- The columns must also have similar data types
- The columns in each SELECT statement must also be in the same order

```sql
SELECT column_name(s) FROM table1
UNION
SELECT column_name(s) FROM table2;
```
These are normal SQL commands used every day by DBAs all the way down to your junior dev/analyst. 


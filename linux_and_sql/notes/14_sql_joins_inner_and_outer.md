# SQL joins — inner and outer joins

## Inner joins

The first type of join you might use is an **inner join**. **`INNER JOIN`** returns rows that **match** on a specified column that exists in **more than one table**.

In a Venn diagram of two tables (left and right), the inner join corresponds to the **intersection** only.

It returns only rows where there is a match. Like other joins, it returns **all specified columns** from all joined tables. For example, if the query joins two tables with `SELECT *`, **all columns** from **both** tables are returned.

**Note:** If a column exists in **both** tables, it appears **twice** when `SELECT *` is used.

### Syntax of an inner join

```sql
SELECT *
FROM employees
INNER JOIN machines ON employees.device_id = machines.device_id;
```

- The **left** table is listed after `FROM`.
- The **right** table is listed after `INNER JOIN`.
- After the right table, use **`ON`** and **`=`** to specify the join column(s).
- Use **`table.column`** (period between table and column) so it is clear which table each column comes from.

You can select only certain columns. For example, to return **username**, **operating_system**, and **device_id**:

```sql
SELECT username, operating_system, employees.device_id
FROM employees
INNER JOIN machines ON employees.device_id = machines.device_id;
```

**Note:** If **username** and **operating_system** appear in only one table, you can use the column name alone. If **device_id** appears in **both** tables, qualify it (e.g., `employees.device_id`) so the query knows which table’s column to return.

---

## Outer joins

**Outer joins** expand what is returned from a join. Each type returns **all rows** from one table, or **both** tables, in addition to (or instead of) only matches—depending on the join type.

---

## Left joins

**`LEFT JOIN`** returns **all records** from the **first (left) table**, and only matching rows from the **second (right) table** on the specified column.

Venn diagram: the **left circle** and the **intersection** are highlighted.

### Syntax

```sql
SELECT *
FROM employees
LEFT JOIN machines ON employees.device_id = machines.device_id;
```

- **`employees`** is the **left** table (after `FROM`) — **all** of its rows are returned.
- **`machines`** is the **right** table — only rows that **match** on `device_id` are included from this table.

---

## Right joins

**`RIGHT JOIN`** returns **all records** from the **second (right) table**, and only matching rows from the **first (left) table** on the specified column.

Venn diagram: the **right circle** and the **intersection** are highlighted.

### Syntax

```sql
SELECT *
FROM employees
RIGHT JOIN machines ON employees.device_id = machines.device_id;
```

This returns **all** rows from **`machines`** (right table) and only **matching** rows from **`employees`** (left table).

**Note:** You can get the **same result** as a `LEFT JOIN` by swapping table order and using `RIGHT JOIN`. For example, this is equivalent to the earlier `LEFT JOIN` example with `employees` on the left:

```sql
SELECT *
FROM machines
RIGHT JOIN employees ON employees.device_id = machines.device_id;
```

Swap which table appears before and after the join keyword to swap **left** and **right**.

---

## Full outer joins

**`FULL OUTER JOIN`** returns **all records from both tables**. You can think of it as **fully merging** two tables.

Venn diagram: **both circles** are highlighted.

### Syntax

```sql
SELECT *
FROM employees
FULL OUTER JOIN machines ON employees.device_id = machines.device_id;
```

Like **`INNER JOIN`**, the **order of tables** does not change the logical result set for a full outer join (both tables are included in full).

---

## Key takeaways

- All joins match rows on a **specified column** (using `ON`).
- **`INNER JOIN`** returns **only** matching rows (intersection).
- **Outer joins** also return non-matching rows from one or both sides:
  - **`LEFT JOIN`** — all rows from the **left** table
  - **`RIGHT JOIN`** — all rows from the **right** table
  - **`FULL OUTER JOIN`** — all rows from **both** tables

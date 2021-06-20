# Spring-Boot-Transaction

## Toppics

### ACID Transaction
 
- <b>Atomicity</b> หมายถึงความสำเร็จทั้งหมดหรือความล้มเหลวทั้งหมด. All tasks of a transaction are performed or none of them are. There are no partial transactions. For example, if a transaction starts updating 100 rows, but the system fails after 20 updates, then the database rolls back the changes to these 20 rows.
- <b>Consistency</b>
- <b>Isolation</b>
- <b>Durability</b>

### Transaction Propagation
- REQUIRED
- SUPPORTS
- NOT_SUPPORTED
- REQUIRES_NEW
- NEVER
- MANDATORY
### Transaction Isolation

## การจัดการ JDBC Transaction แบบปกติ

พื้นฐานการจัดการ Transaction จะมีรูปแบบดังนี้

    import java.sql.Connection;

    Connection connection = dataSource.getConnection(); // (1)

    try (connection) {
        connection.setAutoCommit(false); // (2)
        // execute some SQL statements...
        connection.commit(); // (3)

    } catch (SQLException e) {
        connection.rollback(); // (4)
    }

- 1. เชื่อมต่อกับฐานข้อมูลเพื่อเริ่มต้น Transaction
- 2.
- 3.
- 4.

### Refference 

- https://dzone.com/articles/spring-boot-transactions-tutorial-understanding-tr

# Spring-Boot-Transaction

## Toppics

- Transaction Propagation
- Transaction Isolation

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

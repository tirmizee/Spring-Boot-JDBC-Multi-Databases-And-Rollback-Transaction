# Spring-Boot-Transaction

    import java.sql.Connection;

    Connection connection = dataSource.getConnection(); // (1)

    try (connection) {
        connection.setAutoCommit(false); // (2)
        // execute some SQL statements...
        connection.commit(); // (3)

    } catch (SQLException e) {
        connection.rollback(); // (4)
    }

En Java, cuando trabajas con la API JDBC (Java Database Connectivity) para comunicarte con una base de datos, utilizas varias métodos proporcionados por la interfaz java.sql.Statement y la interfaz java.sql.PreparedStatement para interactuar con la base de datos. Dos de los métodos clave son executeQuery y executeUpdate, pero hay otros métodos relacionados que se utilizan para tareas específicas.

Estos métodos se pueden categorizar de la siguiente manera:

+ Métodos para ejecutar consultas (SELECT):
executeQuery: Este método se utiliza para ejecutar una consulta SQL que devuelve un conjunto de resultados, generalmente utilizado para consultas SELECT. Retorna un objeto ResultSet que contiene los datos recuperados de la base de datos.

+ Métodos para ejecutar actualizaciones (INSERT, UPDATE, DELETE, etc.):
executeUpdate: Este método se utiliza para ejecutar consultas SQL que realizan actualizaciones en la base de datos, como INSERT, UPDATE, DELETE, etc. Retorna el número de filas afectadas por la operación.

+ Métodos para ejecutar cualquier tipo de sentencia SQL:
execute: Este método se utiliza para ejecutar cualquier tipo de sentencia SQL, ya sea una consulta o una actualización. Retorna un valor booleano (true si el primer resultado es un objeto ResultSet o false si es un recuento de filas o no hay resultados).

+ Métodos para trabajar con parámetros en consultas preparadas:
setXXX (por ejemplo, setString, setInt, setDate): Estos métodos se utilizan para establecer valores en consultas preparadas antes de ejecutarlas. La "XXX" en el nombre del método varía según el tipo de dato que se está configurando.

+ Métodos para recuperar metadatos de resultados:
getMetaData: Este método se utiliza para obtener información sobre los metadatos de los resultados de una consulta, como nombres de columnas, tipos de datos, etc.

+ Métodos para gestionar transacciones:
commit: Se utiliza para confirmar una transacción.
rollback: Se utiliza para deshacer una transacción.
setAutoCommit: Se utiliza para establecer si las transacciones se confirman automáticamente o no.

Estos son algunos de los métodos más comunes utilizados en la API JDBC para interactuar con bases de datos en Java. La elección del método dependerá de la tarea que desees realizar, ya sea una consulta de lectura, una actualización de datos, la configuración de parámetros en consultas preparadas o la gestión de transacciones.

### Otros metodos usados

| Propósito	| Métodos |
| --------- | ------- |
| Gestionar cursores y navegación de resultados | next, previous, first, last, absolute, relative|
| Obtener metadatos de columnas de resultados | getColumnName, getColumnType, getColumnLabel, getColumnCount |
| Gestionar conexiones en un DataSource | getConnection(String username, String password), closeConnectionPool |
| Gestionar conjuntos de resultados múltiples | getMoreResults, getMoreResults(int current) |
| Establecer tiempo de espera de consultas | setQueryTimeout, getQueryTimeout
| Establecer comportamiento de recuperación automática | setFetchSize, setFetchDirection, setFetchSize(int rows) |
| Configurar el manejo de excepciones | SQLException, SQLWarning, setWarnings |
| Trabajar con transacciones de nivel de aislamiento | setTransactionIsolation, getTransactionIsolation, TRANSACTION_READ_COMMITTED, TRANSACTION_SERIALIZABLE, etc. |
| Obtener resultados de procedimientos almacenados | executeCall, getResultSet, getUpdateCount, getMoreResults, getGeneratedKeys |
| Trabajar con bases de datos en clúster | getClusterMap, setClusterMap |
Obtener información sobre el controlador JDBC | getDriverName, getDriverVersion, getDriverMajorVersion, getDriverMinorVersion |
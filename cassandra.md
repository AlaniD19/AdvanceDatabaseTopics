# Apache Cassandra con Docker
Centro de Investigación en Computación / Instituto Politécnico Nacional

> _**Autor:** Alan Ignacio Delgado Alarcon_  
> *Junio 2025*  
> *Aspectos Avanzados de Bases de Datos*

# Guía rápida de Cassandra

Esta guía cubre los comandos básicos para comenzar con Apache Cassandra.

---

## 1. Conectarse a Cassandra

Usa `cqlsh` para conectarte al servidor local:

```bash
cqlsh
```

## 2. Crear un Keyspace
Un Keyspace es como una base de datos en Cassandra:

```sql
CREATE KEYSPACE ejemplo
WITH replication = {
  'class': 'SimpleStrategy',
  'replication_factor': 1
};
```

## 3. Crear una tabla
```sql
CREATE TABLE ejemplo.usuarios (
  id UUID PRIMARY KEY,
  nombre TEXT,
  correo TEXT
);
```

## 4. Insertar datos
```sql
INSERT INTO ejemplo.usuarios (id, nombre, correo)
VALUES (uuid(), 'Juan Pérez', 'juan@example.com');
```

## 5. Consultar datos
```sql
SELECT * FROM ejemplo.usuarios;
```

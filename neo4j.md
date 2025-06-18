# Bases de Datos de Grafos - Neo4j
Centro de Investigación en Computación / Instituto Politécnico Nacional

> _**Autor:** Alan Ignacio Delgado Alarcon_  
> *Junio 2025*  
> *Aspectos Avanzados de Bases de Datos*

## Instalación
Para versiones para Windows y macOS visite el sitio y descargue el archivo de instalación:

[Instalador - neo4j.com](https://neo4j.com/deployment-center/?gdb-selfmanaged)

### Linux - Ubuntu 24.04
Para instalación en sistemas basados en debian, como el caso de Ubuntu version `24.04 LTS` para neo4j `2025.05.0`, siga los siguinetes pasos:

> **NOTA**  
> las versiones de neo4j 2025 requieren de `java 21`. Para comprobar las versiones disponibles de java en su sistema use:  
> ```bash
> update-java-alternatives --list
>```
> La salida del comando podria ser similar a esta:
> ```bash
> java-1.21.0-openjdk-amd64 2111 /usr/lib/jvm/java-1.21.0-openjdk-amd64
> java-1.17.0-openjdk-amd64 1711 /usr/lib/jvm/java-1.17.0-openjdk-amd64
> ...
> ```
> Asigne la versón 21 de java por defecto con el siguinete comando:
> ```bash
> sudo update-java-alternatives --jre --set java-1.21.0-openjdk-amd64
> ```
> valide que la actualización se realizo correctamente con:
> ```bash
> java -version
> ```

1. Agregar los repositorios oficiales, las llaves de verificación y actualizamos la lista de paquetes disponibles para instralación.
```bash
wget -O - https://debian.neo4j.com/neotechnology.gpg.key | sudo gpg --dearmor -o /etc/apt/keyrings/neotechnology.gpg
echo 'deb [signed-by=/etc/apt/keyrings/neotechnology.gpg] https://debian.neo4j.com stable latest' | sudo tee -a /etc/apt/sources.list.d/neo4j.list
sudo apt-get update
```

2. Verificamos que el paquete y versiones de neo4j estan disponibles.
```bash
apt list -a neo4j
```

3. Instalamos neo4j en su version `Community` que nos permite hacer uso del gestor sin necesidad de licencia. Instalamos la ultima versión estable: `2025.05.0`.
```bash
sudo apt-get install neo4j=1:2025.05.0
```

4. Ejecutamos el siguiente comando para asegurarnos que neo4j se inicie automaticamente al iniciar el sistema.
```bash
sudo systemctl enable neo4j
```

### Ubicación de archivos
Los directorios y sus ubicaciones por defecto para configuraciones adicionales se pueden consultar diractamente de la documentación oficial.

[Default file locations - neo4j.com](https://neo4j.com/docs/operations-manual/current/configuration/file-locations/)

Para fines de los ejercicios en este documento no es necesario realizar ajustes adicionales a la instalación previa.

### Neo4j Desktop
Este software habilita una interfaz grafica para la gestion de las bases de datos locales, incluye una licencia de neo4j `Enterprice Edition Developer`, limitada para ser usada unicamente en una máquina.

Para los ejercicios permitira ver de forma visual los resultados de las consultas y comprender mejor el modelo de este tipo de baes de datos. Neo4j recomienda no ejecutar la aplicación Desktop en entornos de producción debido a los problemas de seguridad derivados por el tipo de ejecuciones.

#### Ejecución
1. En la pagina del centro de desarrollo de neo4j, en el apartado de neo4j Desktop deje seleccionada la ultima versión disponible y seleccione el sistema operativo `Linux (x86 AppImage)`.

[Deployment Center - neo4j.com](https://neo4j.com/deployment-center/?desktop-gdb)

2. Llene el formulario que muestra a continuación y el archivo comenzará su descarga automaticamente.

3. Abra una terminal en el sistema y vaya al directorio donde se ha descargado el archivo de neo4j desktop.

4. Asignamos permisos de ejecución con el usuario que inicio sesión en el sistema:
```bash
sudo chmod +x neo4j-desktop-2.0.1-x86_64.AppImage
```

5. Instalamos el paquete `fuse` necesario para el funcionamiento del aplicativo
```bash
sudo apt install fuse
```

6. Iniciamos la aplicación con el siguiente comando para ejecutarla sin el entorno seguro. Esta opción se utiliza únicamente con fines prácticos en este documento. 
```bash
./neo4j-desktop-2.0.1-x86_64.AppImage --no-sandbox
```

> **NOTA**  
> `.AppImage` es un formato portable de aplicaciones Linux que no requiere instalación, solo permisos de ejcucición.

## CRUD
### Create - Crear


### Read - Leer



### Update - Actualizar


### Delete 


## Carga de datos



## Lenguajes de programación

```bash

```

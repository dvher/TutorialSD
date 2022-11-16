# Instalación

## Pre-requisitos

1. Instalar Java
    ```bash
    sudo apt-get install openjdk-11-jdk
    ```
1. Instalar Hadoop
    1. Crear usuario
        ```bash
        sudo addgroup -m hadoop
        sudo passwd hadoop
        ```
    1. Descargar Hadoop
        ```bash
        wget https://dlcdn.apache.org/hadoop/common/hadoop-3.3.4/hadoop-3.3.4.tar.gz
        ```
1. Descomprimir Hadoop
    ```bash
    sudo tar -C /usr/local -xzf hadoop-3.3.4.tar.gz
    ```

## Instalar

1. Descargar HBase mediante el enlace de descarga de la página oficial de [HBase](https://hbase.apache.org/downloads.html).
    ```bash
    wget https://dlcdn.apache.org/hbase/2.4.15/hbase-2.4.15-bin.tar.gz
    ```
1. Descomprimir el archivo descargado.
    ```bash
    sudo tar -C /usr/local -xzf hbase-2.4.15-bin.tar.gz
    ```
1. Agregar la variable de entorno 'JAVA_HOME' al archivo hbase-env.sh.
    ```bash
    sudo nano /usr/local/hbase-2.4.15/conf/hbase-env.sh
    ```
    ```bash
    export JAVA_HOME=/usr/lib/jvm/java-11-openjdk-amd64
    ```
1. Para ejecutar HBase, se debe ejecutar el script 'start-hbase.sh' que se encuentra en la carpeta 'bin' del directorio de instalación.
    ```bash
    sudo /usr/local/hbase-2.4.15/bin/start-hbase.sh
    ```
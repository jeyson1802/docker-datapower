Pasos para iniciar contenedor:
 1. eliminar carpeta config local
 2. crear carpeta config local
 3. chmod 777 config local
 4. iniciar contenedor de forma manual

docker run -it \
  -v $PWD/config:/drouter/config \
  -v $PWD/local:/drouter/local \
  -e DATAPOWER_ACCEPT_LICENSE=true \
  -e DATAPOWER_INTERACTIVE=true \
  -e DATAPOWER_WORKER_THREADS=4 \
  -p 9090:9090 \
  ibmcom/datapower

 5. configurar app web del datapower
    configure; web-mgmt 0 9090 9090;
 6. guardar cambios 
    write mem
 7. salir -> exit
 8. luego se puede iniciar con docker-compose 




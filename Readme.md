# Proyecto de aplicación
## Servicio Web

## Demo

https://bsginstitutelaboratory.innovandoperu.com/

## Contenido 

- deploy: Archivos de configuración para despliegue
- webapp: Aplicación Django Web Server 

### Deploy
#### Pasos de despliegue Django



    mkdir /app
    cd /app
    python -m venv webapp
    cd webapp 
    git clone https://github.com/pacifi/awsec2test proyecto
    mkdir -p /app/webapp/proyecto/logs
    source /app/webapp/bin/activate
    pip install -r /app/webapp/proyecto/requirements.txt

#### Despliegue Supervisor

    sudo apt install supervisor
    cp /app/webapp/proyecto/deploy/webapp.conf /etc/supervisrd/conf.d
    sudo supervisorctl reread
    sudo supervisorctl update
    sudo supervisorctl restartall
    sudo systemctl enable supervisor.service
    sudo systemctl restart supervisor.service
    


# Documentazione per lab gitlab con Docker

## Creazione ambiente

### Step 1:

#### Step 1.1:

Modificare nella cartella 

C:\Windows\System32\drivers\etc

il file hosts

aggiungendo la riga

127.0.0.1 gitlab.corso.local

#### Step 1.2:

Accertarsi di avere nella folder ove risiede il docker-compose.yaml, le seguenti folder (se non esistono crearle):
- config
- data
- logs

### Step 2
lanciare il seguente batch

```powershell
./01-start.bat

# Nota: se si desidera seguire i log di gitlab, lanciare il comando:
# docker logs -f gitlab

```

### step 3

Aprire con il browser l'endpoint

http://gitlab.corso.local:8929


### step 4

Una volta accertato che gitlab è pronto all'uso, aprire un prompt dei comandi 
e lanciare il seguente comando docker per recuperare la password dell'utenza root

```powershell
docker exec -it gitlab grep 'Password:' /etc/gitlab/initial_root_password
```

### step 5
Tornare al browser sull'endpoint

http://gitlab.corso.local:8929

e loggarsi usando le credenziali

USR: root
PWD: [quella recuperata dal comando docker]

ENJOY !!!
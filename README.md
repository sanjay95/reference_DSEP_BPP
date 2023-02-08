# reference_DSEP_BPP Installation and usage

## PreRequisites: 

Docker run time, docker compose, postman(or similar ) 

## Components :

BPP APIs, SearchAPI,Opensearch for storing job and application catalog

SearchAPI to handle catalog search requests from BPP and to post and manage the job catalog.

                                  # BG→BPP→searchAPI→Opensearch 



#Configure the environment variable for your BPP ( subscriber-id, private key,, BPP Urls etc)  in docker compose file:https://github.com/sanjay95/reference_DSEP_BPP/blob/main/docker-compose.yml


## Steps: 

### start the containers using 	      docker-compose up -d 
### Check status using 	## docker-compose ps 
### For Logs:  ## docker-compose logs -f 
### Post a sample job to searchAPI at http://localhost:8080/opensearch
With payload: https://github.com/sanjay95/reference_DSEP_BPP/blob/main/Sample_Job.json
### Note: ID will be generated and saved in catalog
 
### Perform search/select/confirm/status api calls at : 
http://localhost:8088/search

http://localhost:8088/select

http://localhost:8088/confirm

http://localhost:8088/status



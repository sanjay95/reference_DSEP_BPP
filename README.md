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
![image](https://user-images.githubusercontent.com/1314582/217458674-26c0de3e-e178-4c72-abca-d9fb841dbc5d.png)


### Check status using 	## docker-compose ps 
<img width="1130" alt="image" src="https://user-images.githubusercontent.com/1314582/217458204-b2ad8f6c-c602-410c-b39d-2cdbc092eca8.png">


### For Logs:  ## docker-compose logs -f 


### Post a sample job to searchAPI at http://localhost:8080/opensearch
With payload: https://github.com/sanjay95/reference_DSEP_BPP/blob/main/Sample_Job.json
### Note: ID will be generated and saved in catalog
 
### Perform search/select/confirm/status api calls at : 
http://localhost:8088/search

http://localhost:8088/select

http://localhost:8088/confirm

http://localhost:8088/status



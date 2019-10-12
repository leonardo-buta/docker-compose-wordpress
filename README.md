## Docker Compose with MySql, PhpMyAdmin and WordPress

This is an example of a docker compose file which starts the following docker containers:
* `MySql` - 8.0
* `PhpMyAdmin` - latest
* `WordPress` - latest

# How to start
Put the docker-compose.yaml into a folder and run the following in terminal:
```
docker-compose up -d
```

It will download the images if you dont have it. After the download is complete, you can acess in your browser:  
### WordPress - http://localhost:8000

The installation will start and you need to provide the required information.

### PhpMyAdmin - http://localhost:8080

In PhpMyAdmin, enter the following:  
`Server`: db  
`Username`: wordpresswithdocker  
`Password`: wordpresswithdocker

That's it!

# How to stop
If you wish to stop the containers but keep your MySql data, run:
```
docker-compose down
```

If you wish to stop the containers and delete your MySql data (volumes), run:
```
docker-compose down --volumes
```
## References
[Docker Documentation](https://docs.docker.com/compose/wordpress)  
[bradtraversy](https://gist.github.com/bradtraversy/faa8de544c62eef3f31de406982f1d42)

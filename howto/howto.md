## The Gcloud assignment

### Docker setup

1. 
1. at top right click on create and then "Create automated Build"
1. select github (on the left)
1. select your forked project yourgithubid/gcloud
1. click on create

Now every time you push a commit to the github repo, the new container is created on DockerHub.

You can access them from any machine via
`docker pull yourDockerId/gcloud`

#### > fork coscs340/gcloud

![image0001](image0001.png)

![image0002](image0002.png)

![image0003](image0003.png)

![image0004](image0004.png)

![image0005](image0005.png)

![image0006](image0006.png)

![image0007](image0007.png)

![image0008](image0008.png)

![image0009](image0009.png)

#### > create dockerhub account [hub.docker.com](http://hub.docker.com)

![image0010](image0010.png)

![image0012](image0012.png)

`Create automated build`

![image0013](image0013.png)

Select the forked gcloud repo

![image0014](image0014.png)

![image0015](image0015.png)

![image0016](image0016.png)

Done with the docker stuff for now.

## Now to Google Cloud

Get dat URL from the lectures repo.

![image0017](image0017.png)

Set up yer account

![image0018](image0018.png)

![image0019](image0019.png)

Nah let's do this the easy way...

![image0020](image0020.png)

![image0021](image0021.png)

To the web interface!

Select a new cs340 project

![image0022](image0022.png)

![image0023](image0023.png)

![image0024](image0024.png)

K done now make a compute instance using that button earlier.

![image0025](image0025.png)

![image0026](image0026.png)

Hmm this seems to be taking awhile...

Ok done.

![image0027](image0027.png)

![image0028](image0028.png)

![image0029](image0029.png)

"Create"

![image0030](image0030.png)

Check the "Deploy a container image" so that we can use our docker container.

Remember this?

![image0054](image0054.png)

Put that title into this:

![image0055](image0055.png)

Add HTTP for the firewall:

![image0033](image0033.png)

Click that more config stuff dropdown:

![image0056](image0056.png)

Now add this into the boot script: (modify it first)

```
#!/bin/bash
docker rm ws
docker run -d --name ws -p80:80 YOURGITHUBUSER/webserver
```

![image0057](image0057.png)

Done here.

![image0034](image0034.png)

Being created:

![image0035](image0035.png)

Done:

![image0036](image0036.png)

Click on that IP: WEBSITE!

E.x. [http://35.196.184.168/](http://35.196.184.168/)

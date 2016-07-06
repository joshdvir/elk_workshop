
# ELK Workshop

![](http://384uqqh5pka2ma24ild282mv.wpengine.netdna-cdn.com/wp-content/uploads/2014/12/ELK1.jpg)

## Prerequisites

#### Docker

Install Docker using the *getting started* guide on Docker website, set it up for your distribution [Mac](https://docs.docker.com/docker-for-mac/), [Linux](https://docs.docker.com/engine/installation/) and [Windows](https://docs.docker.com/docker-for-windows/).

* docker-machine
* docker-compose

## Very Quick Start

Run these commands and you are done

```
git clone https://github.com/joshdvir/elk_workshop.git
cd elk_workshop
docker-machine start dev
eval "$(docker-machine env dev)"
docker-compose up
```

Everything should be running now

Get the IP of the VM

```
docker-machine ip dev
```

Go to http://[```docker-machine ip dev```]:5601/


# Lets go over the files and see how it's done!!!
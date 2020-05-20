# bioc-release
A More Complete Bioconductor Release Container

How I build the container:

```
docker build -t schifferl/bioc-release:latest - < Dockerfile
```

How I start the container:

```
read -s 'REPLY?bioc-passwd:'; echo; docker run -d --name bioc-release --restart unless-stopped -p 7000:8787 -e PASSWORD=$REPLY -e USER=bioc -v /Users/$USER/.ssh:/home/bioc/.ssh schifferl/bioc-release:latest; unset REPLY
```

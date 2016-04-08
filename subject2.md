# Subject2

You want to deploy some web services for your company. Including : 

 - Redmine : a ticketting system
 - Owncloud for sharing files
 - The web site of your company : Mashibuya

Your goal is to design a docker file to aggregate all these docker files behind a docker-compose

## Question 1 

Using https://hub.docker.com/_/redmine/ start a redmine:latest container (2 point)

## Question 2

Using https://hub.docker.com/_/owncloud/ start  owncloud:latest container (2 point)

## Qestion 3

Add these DNS entry pointing to 127.0.0.1 in your **/etc/hosts** file : redmine.mashibuya.com, owncloud.mashibuya.com (2 point)

## Question 4

Create a NGinx container rederecting redmine.mashibuya.com to host name redmine, and owncloud.mashibuya.com to name owncloud. Your service will listen in HTTP, port 80. (3 points)

## Question 5

Create a docker compose file with both redmine and owncloud behind a NGinx container (3 points)

## Question 6

Following the links given earlier, configure both containers to rely on the same mysql database (3 points)

## Question 7

Add a volume to the owncloud container (/var/www/html) (3 points)
Same thing for redmine (/usr/src/redmine/files)

## Question 8

Configure NGinx to use SSL with a self signed certificate (4 points)

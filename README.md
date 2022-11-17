# freekvanlier-personal-website
 
docker build -t image/freekvanlier-personal-website . && docker run -d -p 80:80 --name freekvanlier-website --restart unless-stopped image/freekvanlier-personal-website 

# Docker-1T-Data-training

## Starting a single database
1. Move to db folder - `cd db`
2. Build image by using command `docker build -t test_image:latest .`
3. Run container - `docker run -d -p 5432:5432 --name test_container test_image:latest`
4. Check the container by using `docker ps`
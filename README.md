# Restaurant Environment

### Prerequisites
1. docker: [https://docs.docker.com/engine/install/ubuntu/](https://docs.docker.com/engine/install/ubuntu/)
2. docker-compose: [https://www.digitalocean.com/community/tutorials/how-to-install-and-use-docker-compose-on-ubuntu-20-04](https://www.digitalocean.com/community/tutorials/how-to-install-and-use-docker-compose-on-ubuntu-20-04)

### Installation steps
1. Create and enter the directory where you want to download the repositories
   `mkdir restaurant && cd restaurant`
2. Clone the repositories with
   ```
   git clone git@github.com:Cristi2807/Restaurant.git
   git clone git@github.com:Cristi2807/DinningHall.git
   git clone git@github.com:Cristi2807/Kitchen.git
   ```
3. Build the docker images
   ```
   docker build -t dinninghall DinningHall/
   docker build -t kitchen Kitchen/
   ```
4. Enter the `Restaurant` directory with `cd Restaurant`
5. Use `docker-compose up -d` to start the containers for the simulation
6. Download the dependencies with
   ```
   docker exec DinningHall go mod vendor && docker exec Kitchen go mod vendor
   ```

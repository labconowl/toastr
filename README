# toaSTR
toaSTR is a browser-based application for the analysis of short tandem repeats from massively parallel sequencing data.

## Installation
This dockerized, standalone distribution of toaSTR is a multi-container application that depends on multiple services, including a MySQL database and a job queue system which processes the analysis tasks. The application’s services are configured in a Docker Compose file (`docker-compose.yml`) and automatically handled by the Docker platform. When toaSTR is started for the first time, it reads the `init.sql` file to initialize the toaSTR database.

1. Install Docker for your platform (macOS, Windows or Linux): https://docs.docker.com/get-docker/
2. Only Linux users: Install Docker Compose https://docs.docker.com/compose/install/
3. Clone or download this repository
4. Configure the number of CPU cores used by toaSTR. Open the file `docker-compose.yml` in a text editor and search for the key `theschwartz` -> `environment` -> `PARALLEL_WORKERS`. Set the value to an appropriate number of CPU cores (default: 4).
5. On the command line, navigate to the `toastr` directory and run `docker-compose pull` to pull the toaSTR service images from Docker Hub.

## Usage
1. Start toaSTR: `docker-compose up -d`. On first start, please wait one minute to complete database initialization before proceeding to the next step.
2. Open `localhost:3000` in your browser and login with username `admin` and password `toastrdocker`. Please refer to the manual inside the app for usage instructions.
3. Stop toaSTR: `docker-compose down`

In case you want to reset the application, run `docker-compose down -v`. Warning: This deletes all app data and configuration.

## Contact
Sebastian Ganschow <sganschow@lacon-owl.de>
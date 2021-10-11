# toaSTR
toaSTR is a browser-based application for the analysis of short tandem repeats from massively parallel sequencing data. It runs on macOS, Windows, and Linux.

## Installation
This dockerized, standalone distribution of toaSTR is a multi-container application that depends on multiple services, including a MySQL database and a job queue system which processes the analysis tasks. The application’s services are configured in a Docker Compose file (`docker-compose.yml`) and automatically handled by the Docker platform. When toaSTR is started for the first time, it reads the `init.sql` file to initialize the toaSTR database.

1. Install Docker (macOS, Windows or Linux): https://docs.docker.com/get-docker/
2. Install Docker Compose (Linux users only): https://docs.docker.com/compose/install/
3. Clone or download this repository
4. Optionally configure the number of CPU cores used by toaSTR. Open the file `docker-compose.yml` in a text editor and search for the key `theschwartz` -> `environment` -> `PARALLEL_WORKERS`. Set the value to an appropriate number of CPU cores for your machine (default: 4).
5. Open a command prompt (terminal), navigate to the `toastr` directory and run `docker-compose pull` (Linux: `sudo docker-compose pull`) to pull the toaSTR service images from [Docker Hub](https://hub.docker.com/repository/docker/labconowl/toastr).

## Usage
1. Start toaSTR: `docker-compose up -d` (Linux: `sudo docker-compose up -d`). On first start, please wait one minute to complete database initialization before proceeding to the next step.
2. Open `localhost:3000` in your browser and login with username `admin` and password `toastrdocker`. Please refer to the manual inside the app for usage instructions.
3. Stop toaSTR: `docker-compose down` (Linux: `sudo docker-compose down`)

In case you want to reset the application, run `docker-compose down -v` (Linux: `sudo docker-compose down -v`). Warning: This deletes all app data and configuration.

## Support
Sebastian Ganschow <sganschow@labcon-owl.de>
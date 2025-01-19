# SecFit

SecFit (Secure Fitness) is an application for fitness logging with a focus on privacy and security.

## Prerequisites

Before you start, make sure the following tools are installed on your system:

- **Git:** Version control system to clone the project repository [Download Git](https://git-scm.com/downloads)
- **Docker:** To containerize the application and ensure it runs consistently across different environments [Download Docker](https://www.docker.com/products/docker-desktop)
- **VPN** - Connection to NTNU servers [VPN Guide](https://i.ntnu.no/wiki/-/wiki/English/Install+VPN)

## Usage

To run the project, execute the following command in the root folder:

```bash
docker compose up --build -d
```

This will build the Docker images (if necessary) and run the containers in the background. You can access the application at [http://localhost](http://localhost) and the Django backend at [http://localhost/api](http://localhost/api).
The Admin interface for the Django backend is available at [http://localhost/admin](http://localhost/admin).

To stop the containers, you can use the following command:

```bash
docker compose down
```

## GitHub Runner (CODE DELIVERY)

The repository is configured such that changes pushed to the **production** branch will automatically be deployed on [http://tdt4237-XXX.idi.ntnu.no/](http://tdt4237-XXX.idi.ntnu.no/) (XXX = group number). This can be used for testing the deployed application and should be used for pushing code after fixing vulnerabilities. Typical workflow after finishing development on the main branch would be:

- `git checkout production`
- `git merge main`
- `git push origin production`
- Go to the "Actions" tab within this GitHub repository to monitor deployment.

## Documentation

For more information on how the application is structured, and how to run it without Docker for **development**, see the [Developer Guide](/docs/developer-guide.md).

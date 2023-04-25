# Prometheus Grafana Stack with Docker Compose

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

This repository contains the Docker Compose configuration files for setting up a monitoring and alerting stack using Prometheus, Grafana, Alertmanager, and other related components.

## Table of Contents

- [Introduction](#introduction)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Configuration](#configuration)
- [Usage](#usage)
- [Alerting](#alerting)
- [Contributing](#contributing)
- [License](#license)

## Introduction

This Prometheus Grafana stack provides a comprehensive monitoring and alerting solution for containerized environments. It can be used to monitor various kinds of infrastructure. The stack includes:

- Prometheus: For collecting metrics and monitoring your systems.
- Grafana: For visualizing collected metrics data using customizable dashboards.
- Alertmanager: For managing alerts and sending notifications to different channels like email, Slack, or PagerDuty.

## Prerequisites

To deploy this Prometheus Grafana stack using Docker Compose, make sure you have the following installed on your system:

- Docker
- Docker Compose

## Installation

1. Clone this repository to your local machine.

    ```
    git clone https://github.com/clonewriter/pga-stack-docker.git
    ```

2. Change into the repository directory and deploy the stack using Docker Compose.
    
    ```
    cd pga-stack-docker 
    
    # run docker compose
    docker-compose up -d
    ```
 
3. Access the Grafana web interface via `http://localhost:3000` (default port) with the default username and password (admin/admin) to start customizing your dashboards.

## Configuration

To customize Prometheus, Grafana, or Alertmanager configurations, you can:

- Modify the configuration files located in the `./config` directory.
- Restart the relevant Docker containers for the changes to take effect.

```
docker-compose down 
docker-compose up -d
```

## Usage

Use your browser to access the following services and explore your infrastructure's metrics:

- Access Grafana at: `http://localhost:3000`
- Access Prometheus at: `http://localhost:9090`
- Access Alertmanager at: `http://localhost:9093`

## Alerting

To set up alerts based on the collected metrics, you can modify the `./config/alertmanager/config.yml` file and create custom alert rules for your infrastructure. Restart the Alertmanager container for the changes to take effect.

## Contributing

To contribute to this project, please create a fork and submit pull requests with your proposed changes. We welcome any improvements, bug fixes, and other contributions.

## License

This project is licensed under the [MIT License](https://opensource.org/licenses/MIT).

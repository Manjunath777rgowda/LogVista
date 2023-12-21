# LogVista

LogVista is a project designed to streamline the processing and analysis of log files using Filebeat. It provides a robust and organized approach to handling log data within your system.

## Features

- Docker Compose configuration for easy deployment.
- Efficient loading of log files using Filebeat.
- Seamless processing and forwarding of logs to your desired destination.
- Clear and concise organization of log data for easy analysis.
- Integration with Graylog for centralized log management.

## Getting Started

These instructions will help you set up and run LogVista on your system.

### Prerequisites

- [Docker](https://www.docker.com/get-started) installed on your machine.
- [Graylog](https://www.graylog.org/) for centralized log management.



### Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/Manjunath777rgowda/LogVista.git
   ```

## Configuration

### Configure Filebeat:

Edit the *filebeat.yml* configuration file to match your log file paths and destination settings.

### Configure Docker Compose:

Adjust the docker-compose.yml file to suit your specific needs, including volumes, environment variables, and service configurations.

### Configure Graylog:

- Create Input configuration 'System> Inputs> Select Input as Beats' to accept the filebeat request.
- Import [extractor.json](./extractor.json) to get the extractor. Or create your own extractor

## Usage
Start the Docker Compose services:

```bash
docker-compose up -d
```

Log file which are present under /logs will automatically loaded to the graylog. Check the log folder which is mounted for the file beats in the [docker-compose.yml](./docker-compose.yml) file

## Acknowledgments
- [Filebeat Documentation](https://www.elastic.co/guide/en/beats/filebeat/current/running-on-docker.html)
- [Docker Documentation]()
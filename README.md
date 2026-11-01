# hardened-opencode-docker

> _Disclaimer: The docker-compose.yml file was assisted by AI. It was tasked to generate a hardened docker-compose.yml to run the Docker version of OpenCode in, while the creator of this repository verified and tweaked the contents. Every other file in the repo was not assisted by AI._

An isolated container for OpenCode.

## Installation

Prerequisites: [Install Docker Compose](https://docs.docker.com/compose/install)

### Linux

#### 1. Clone the repository

#### 2. Go to directory

```bash
$ cd hardened-opencode-docker/
```

#### 3. Run the docker-compose.yml

```bash
$ sudo docker compose run --rm opencode
```

## Reasoning

OpenCode installed normally via curl, npm, yay, or other methods such as through
Ollama CLI can access the entire working directory of the user that installed
the application, which compromises the privacy and security of the system. This
allows AI models to see contents of the user's home directory, and potentially
conduct destructive work on the environoment. A more secure option is
downloading OpenCode through a Docker container. This project then hardens the
Docker install further.

## Limitations

This Compose build is designed for cloud-based AI usage only; it does not mount
the proper volumes to detect local AI. Additionally, it does not update to the
latest version, and must be manually changed.

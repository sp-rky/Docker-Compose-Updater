# Docker Compose Updater
A very simple script that:

- Is given a directory containing docker-compose files.
- Searches recursively for files with names containing "docker-compose"
- Runs `docker compose pull` on each file.
- If `docker compose pull` completes successfully, it then runs `docker compose up` on those files.
- Provides basic diagnostic output. 

## Usage
```bash
python3 docker-compose-updater.py /path/to/docker/compose
``` 

## Disclaimer
This code is not intended for use in production environments. It does not have robust error handling, and *might* break some containers if you're not careful. While I am happy to fix any bugs that are reported, I am not responsible for any issues caused by running this script.


# full-stack-containerized-development
All the required assets to develop and run a complete PHP/MySQL/JavaScript/CSS/HTML, including VS Code

## Running The First Time
* Make sure [docker](https://www.docker.com/) is installed.
* Set the following environment variables:
  * `SRC_DIR`
* Run this command
  * `docker-compose up`
* Open a browser to:
  * http://localhost:10080

## Stopping
When `docker-compose stop` is invoked, the environment will be stopped, but not removed. Subsequent to stopping, `docker-compose start` will start the environment.

If the intent is to remove the environment (and all data not mapped into containers), issue the command `docker-compose down`.

## Persisting Data
Data can be persisted within the MySQL and VS Code containers.
  * MySQL
    * Set the `DB_DATA_DIR` environment variable to point to a fully qualified directory where the database will store data
    * Uncomment the following line in `docker-compose.yml`
      * ` - "${DB_DATA_DIR}:/var/lib/mysql"`
  * VS Code
    * Set the `VSCODE_SETTINGS_DIR` environment variable to point to a fully qualified directory where settings will be stored
    * Uncomment the following line in `docker-compose.yml`
      * `- "${VSCODE_SETTINGS_DIR}:/home/coder/.local"`

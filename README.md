# full-stack-containerized-development

All the required assets to develop and run a complete PHP/MySQL/JavaScript/CSS/HTML, including VS Code

## Running The First Time

* Make sure that [docker](https://www.docker.com/) is installed.
* Start the environment
  * Run `docker-compose up`
* Open a browser to:
  * [http://localhost:10080](http://localhost:10080)

## Stopping

When `docker-compose stop` is invoked, the environment will be stopped, but not removed. Subsequent to stopping, `docker-compose start` will
re-start the environment.

To fully remove the environment (and all data not mapped into containers), issue the command `docker-compose down`. Persisted data will remain locally until manually removed.

## Editing HTML/PHP

Use the IDE to edit `index.php`. Add, update or create more pages as necessary.

## Managing The Database

Open the database management page (`Adminer`) from the [main page](http://localhost:10080) and log into the database. The default password for `root` is `p@ssw0rd` (this can be changed within
the `docker-compose.yml` file).

## Persisting Data

All data is persisted into three volumes:

* MySQL
* HTML Source
* VS Code Settings

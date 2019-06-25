FROM codercom/code-server:1.621

RUN mkdir -p /home/coder/project && touch /home/coder/project/index.php && mkdir -p /home/coder/.local
RUN chmod a+w /home/coder/project/
COPY index.php /home/coder/project/index.php

## Need to make this dir so perms are correct when the directory is mounted in
VOLUME [ "/home/coder/project" ]
VOLUME [ "/home/coder/.local" ]

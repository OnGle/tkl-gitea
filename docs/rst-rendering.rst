RST Rendering
=============

Enabling RST rendering in Gitea is relatively simple however
potentially presents security concerns so be warned.

1. update apt and install either `python-docutils` or `python3-docutils`

    .. code-block:: bash

        apt update && apt install python-docutils

2. open /home/git/custom/conf/app.ini and add the following lines

    .. code-block:: ini

        [markup.restructuredtext]
        ENABLED = true
        FILE_EXTENSION = .rst
        RENDER_COMMAND = rst2html
        IS_INPUT_FILE = false

3. restart gitea

    .. code-block:: bash

        service gitea restart

        

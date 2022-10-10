1. install WSL2 Ubuntu   [Windows Subsystem for Linux](https://learn.microsoft.com/en-us/windows/wsl/install)

2. ```shell
    mkdir /tmp/missing
    ```

3. ```shell
    man touch
    ```

4. ```shell
    cd /tmp/missing
    touch semester
    ```

5. ```shell
    echo '#!/bin/sh' >> semester
    echo 'curl --head --silent https://missing.csail.mit.edu' >> semester
    ```

6. Because lacking the execution permission to the semester file.

7. This work because it doesn't need execution permission.

8. ```shell
    man chmod
    ```

9. ```shell
    chmod u+x semester
    ```

    Because the first line(the shebang line) defines the sh to interpret the script.

10. ```shell
    /tmp/semester | grep --ignore-case 'last modified' | cut --delimiter=' ' -f2- > /home/fel/last-modified.txt
    ```

    
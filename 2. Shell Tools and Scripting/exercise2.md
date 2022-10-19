1. ```shell
    ls -alht --color
    ```

2. ```shell
     #!/usr/bin/env bash
     marco () {
        	path = $(pwd)
        	export path
     }
    ```

    ```shell
     #!/usr/bin/env bash
     polo () {
    	cd "$path" || exit
     }
    ```

3. ```shell
     #!/usr/bin/env bash
        
     code=0
     count=0
     path="/home/fel/exercise2"
        
     if [[ -f "$path/stdout.txt"]]
     then
        	 rm -f "$path/stdout.txt"
     fi
     touch "$path/stdout.txt"
        
     if [[ of "path/stderr.txt"]]
     then
      	 rm -f "$path/stderr.txt"
     fi
     touch "$path/stderr.txt"
        
     while [ $code -eq 0 ]; do
        	$path/problem3.sh >> $path/stdout.txt 2>> $path/stderr.txt
        	code=$?
        	((count++))
        	
        	if [[ $code -ne 0 ]]; then
        		echo "runs $count times"
        		cat $path/stdout.txt
        		cat $path/stderr.txt
        		exit 0
        	fi
     done    
        	
    ```

    ```shell
     #!/usr/bin/env bash
    
     n=$(( RANDOM % 100 ))
    
     if [[ n -eq 42 ]]; then
        echo "Something went wrong"
        >&2 echo "The error was using magic numbers"
        exit 1
     fi
    
     echo "Everything went according to plan"
    ```

4. ```shell
     find ./ -name '*.html' | xargs -d '\n' tar cf 
     ```

     
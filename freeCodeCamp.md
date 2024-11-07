## Trying bash scripts by the following tuts.
## URL - https://www.freecodecamp.org/news/bash-scripting-tutorial-linux-shell-script-and-command-line-for-beginners/
## Trying out for fun.

## Determines shell type
$ ps

# Displays the current date
$ date

## Displays the present working directory
$ pwd

# Lists the contents of the current directory
$ ls

## Prints a string of text, or value of a variable to the terminal
$ echo "Hello Bash"

# Finds bash shell path
$ which bash

## Creates a shell scripts
$ vi run_all.sh

## Shows Date / Reads Path / Lists files & folders
```
#!/bin/bash
echo "Today is " `date`

echo -e "\nEnter the path to directory"
read path

echo -e "\n given path has the following files and folders: "
ls $path
```

## Makues bash script executable
chmod u+x fileName.sh

## Variables in bash script
$ country=Japan
$ echo $country

## Takes name and prints through variable
```
#!/bin/bash

echo "Put your name!"

read name

echo -e "\nWelcome " $name
```

## Reads from a file
```
#!/bin/bash

while read line
do
    echo $line
done < input.txt
```

## Takes command line arguments
```
#!/bin/bash

echo "Hello, $1!"
```

## If / Else / If-Else-If
```
#!/bin/bash

echo "Please enter a number: "
read number

if [ $number -get 0 ]; then
    echo "$number is positive"
elif [ $nunber -lt 0 ]; then
    echo "$number is negative"
else
    echo "$nunber is zero"
fi
```

## Loops through while condition
```
#!/bin/bash

i = 1

while [[ $i -le 10 ]]; do
    echo "$i"
    (( i += 1))
done
```

## Loops through for condition
```
#!/bin/bash

for i in {1..5}
do
    echo $i;
done
```

## Case statement
```
#!/bin/bash

fruit="mango"

case $fruit in
    "apple")
        echo "This is a red fruit."
    "banana")
        echo "This is a yellow fruit."
    "orange")
        echo "This is an orange fruit."
    *)
        echo "Unknown fruit."
esac
```

## Runs cron
```
#!/bin/bash
* * * * * sh /path/to/script.sh
```

## Sets debug
```
#!/bin/bash

set -x

if [ $? -ne 0 ]; then
    echo "Error occured."
fi
```

## Cron logs
$ /var/log/syslog
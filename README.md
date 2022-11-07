# FursaHW-BashScripts
In this assignment we were asked to write three bash scripts using AWS 

Question 1: Write a bash script that collects two numbers from the user and then prints a message if these two numbers are smaller or greater than 100.

    #! /usr/bin/bash
    echo "please enter first number: "
    read  num1
    echo "please enter second number: "
    read  num2
    sum=$((num1 + num2))
    if [ $sum -lt 100 ]
    then
           echo "Sum is Less than 100"
    elif [ $sum -gt 100 ]
    then
           echo "Sum is more than 100"
    else
           echo "Sum Equals 100"
    fi
Question 2:Write a bash script that reads a temperature in Fahrenheit and converts it to Celcius.

    #! /usr/bin/bash
    echo "please enter the temperature in Fahrenheit: "
    read temf
    temc=$((($temf-32)*5/9))
    echo "$temf = $temc"

Question 3:Using the find, du, and sort commands, please write a script that finds the largest 10 files in a directory.

    echo -n "please enter directoy path: "
    read path 
    if [[ -z $path ]]
    then
        echo "input is incorrect!"
    else
        echo "The largest 10 files in this path are: "
        find $path -type f | du -a | sort -rh | head -10
    fi

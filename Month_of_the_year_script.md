### Conditional Loop 
Develop a shell script /home/bob/print-month-name.sh that accepts the number of a month as input and prints the name of the respective month.eg ./print-month-name.sh 1 should print January and ./print-month-name.sh 5 should print May. Also keep these in mind.

1. The script must accept a month number as a command line argument.
2. If a month number is not provided as command line argument, the script must exit with the message No month number given.
3. The script must not accept a value other than 1 to 12. If not the script must exit with the error Invalid month number given.

### Create file using vim

vi print-month-name.sh

### Press i to insert text

A=$1   #Alternatively, use interactive input  read -p "Kindly enter month number (1-12):" A

if [ -z $A ]

then echo "No month number given. Kindly input any number from 1 - 12"

elif [ $A -eq 1 ]

then echo "January"

elif [ $A -eq 2 ]

then echo "February"

elif [ $A -eq 3 ]

then echo "March"

elif [ $A -eq 4 ]

then echo "April"

elif [ $A -eq 5 ]

then echo "May"

elif [ $A -eq 6]

then echo "June"

elif [ $A -eq 7 ]

then echo "July"

elif [ $A -eq 8 ]

then echo "August"

elif [ $A -eq 9 ]

then echo "September"

elif [ $A -eq 10 ]

then echo "October"

if [ $A -eq 11 ]

then echo "November"

if [ $A -eq 12 ]

then echo "December"

else

echo "Invalid month number given. Kindly input any number from 1 - 12"

fi

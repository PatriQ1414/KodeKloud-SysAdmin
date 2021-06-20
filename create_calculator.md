#### Build a menu driven calculator program. 
#### Develop a script calculator.sh that when run shows a menu driven program with the following options:

#### 1. Add
#### 2. Subtract
#### 3. Multiply
#### 4. Divide
#### 5. Quit

#### Depending on the input the program must ask for 2 numbers - Number1 and Number2 and then print the result in the form Answer=6.The program must then show the menu again until user selects option 5 to quit.

while true

do

echo "1. Add"

echo "2. Subtract"

echo "3. Multiply"

echo "4. Divide"

echo "5. Quit"

echo "Kindly select the appropriate number option for the operation you want to perform"

read -p "Please, enter a number selection:" selection

if [ $selection -eq 1 ]

then 

read -p "Please enter first number:" number1

read -p "Please enter second number:" number2

echo "Answer=$(($number1+$number2))

elif [ $selection -eq 2 ]

then 

read -p "Please enter first number:" number1

read -p "Please enter second number:" number2

echo "Answer=$(($number1-$number2))

elif [ $selection -eq 3 ]

then 

read -p "Please enter first number:" number1

read -p "Please enter second number:" number2

echo "Answer=$(($number1*$number2))

elif [ $selection -eq 4 ]

then 

read -p "Please enter first number:" number1

read -p "Please enter second number:" number2

echo "Answer=$(($number1/$number2))

elif [ $selection -eq 5 ]

then 

break

else

echo "Invalid input. Kindly enter a seletion from 1 - 5."

fi

done



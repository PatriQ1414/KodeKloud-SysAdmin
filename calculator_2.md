### Calculator using the CASE statement

while true

do

echo "1. Add"

echo "2. Subtract"

echo "3. Multiply"

echo "4. Divide"

echo "5. Quit"

echo "Kindly select the appropriate number option for the operation you want to perform"

read -p "Please, enter a number selection:" selection

case $selection in

      1) read -p "Please enter first number:" number1

         read -p "Please enter second number:" number2
   
        echo "Answer=$(($number1+$number2))
   ;;

      2) read -p "Please enter first number:" number1

        read -p "Please enter second number:" number2

        echo "Answer=$(($number1-$number2))
   ;;

      3) read -p "Please enter first number:" number1

         read -p "Please enter second number:" number2

         echo "Answer=$(($number1*$number2))
   ;;

     4) read -p "Please enter first number:" number1

        read -p "Please enter second number:" number2

        echo "Answer=$(($number1/$number2))
   ;;

     5) break

;;

    *) echo "Invalid input. Kindly enter a seletion from 1 - 5."

;;

esac

done

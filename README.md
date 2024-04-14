# bene
Function_based_math_table

This function ask the user to input an interger then it will generate a math table for the input integer.
The program will ask the user if he/she wanna try again.


def math_table():
    while True:
        number = input('Please enter an integer number: ')
        if number.isdigit(): # isdigit() tjekker om inputtet er nummerisk og returner False hvis der er kommatal
            number = int(number) # Konveter til et heltal
            print('Time table for the input number: ')
            for i in range(1, number+1):
                print(f'\n{number} * {i} = {number * i}')
            
            while True:
                again = input('Wanna try again? [y] or [n]') 
                if again == 'y ':
                    print('You chose to try again')
                    break # Hvis brugeren indtaster 'y' breaker den fra den indre løkke og går op til den ydre
                elif again == 'n ':
                    print('You stopped the program')
                    return 
                
                else:
                    print('Please enter [y] or [n] wether you wanna try again or not')
        
        else:
            print('ERROR! Integers only. Please Try again')
            continue
          
        

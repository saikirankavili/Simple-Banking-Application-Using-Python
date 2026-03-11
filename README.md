# Simple-Banking-Application-Using-Python
A console‑based mini banking application that simulates PIN verification, balance inquiry, deposits, and withdrawals with receipt options.
U&I Bank – Console-Based Banking System
A Python-based mini banking application that simulates core ATM functionalities including secure PIN verification, balance inquiry, deposits, and withdrawals. 
The project emphasizes user input validation, transaction handling, and receipt generation, making it a practical demonstration of control structures, loops, and conditional logic in Python.


###### Code ######
### 1st Type of code

print("😇Welcome To U&I Bank😇")
pin=35968
attempts = 0
max_attempts = 3
while attempts < max_attempts:
    a=int(input("Please Cover The Keypad and Enter Your Pin:"))
    if pin==a:
        print("✅ Login Successful")
        print("Account Holder Name: Sai Kiran.ps \nAccount No: 35689 \nAccount type: Savings")
        print("1.Check Balance \n2.Money Deposite \n3.Cash Withdrawl")
        Balance = 98653 
        choice=int(input("Please Choose an Option to Continue:"))
        if choice==1:
            print("Your Current Balance:",Balance)
            b=input("Do You Want Reciept (yes/no):")
            if b=="yes":
                print("Reciept Printed Sucessfully. Please Collect the Reciept")
            else:
                print("Thank You for Banking With U&i Bank")
        elif choice==2:
            c=int(input("Enter The Amount to be Deposite:"))
            if c>0:
                Balance+=c
                print("Money is Deposited Successfully \nYour Current Balance:",Balance)
                c1=input("Do You Want Reciept (yes/no):")
                if c1=="yes":
                    print("Reciept Printed Successfully. Please Collect Your Reciept")
                else:
                 print("Thank You for Banking With U&I Bank")
            else:
                print("Enter a Valid Amount to be deposite")
        elif choice==3:
            d=int(input("Enter Amount to withdrawl:"))
            if d<=Balance:
                print("Withdrawl is Sucessful. Please Collect Your Cash")
                print("Thank You for Banking With U&I Bank")
                d1=input("Do You Want Reciept (yes/no):")
                if d1=="yes":
                    print("Reciept Printed Successfully. Please Collect Your Reciept")
                else:
                    print("Thank You for Banking With U&I Bank")
            else:
                print("Enter a Valid Amount")
        break
    else:
        attempts += 1
        if attempts < max_attempts:
            print("You Have Entered Wrong Pin❌ \nPlease Try Again")
        else:
            print("You Have Enterd the Wrong Pin for 3 Times❌\n🚫Your Account is Blocked🚫 \nContact the Bank🏦")


### 2nd Type Code

print("😇 Welcome To U&I Bank 😇")
pin = 35968
attempts = 0
max_attempts = 3
Balance = 98653

while attempts < max_attempts:
    a = int(input("Please Enter Your Pin: ")) 
    if pin == a:
        print("✅ Login Successful")
        print("Account Holder Name: Sai Kiran.ps \nAccount No: 35689 \nAccount type: Savings")
        while True:
            print("\n🏦 Menu:")
            print("1. Check Balance")
            print("2. Money Deposit")
            print("3. Cash Withdrawal")
            print("4. Exit")            
            choice = int(input("Please Choose an Option: "))       
            if choice == 1:
                print("Your Current Balance:", Balance)
                b = input("Do You Want Receipt (yes/no): ")
                if b.lower() == "yes":
                    print("Receipt Printed Successfully. Please Collect the Receipt")
                else:
                    print("Thank You for Banking With U&I Bank")          
            elif choice == 2:
                c = int(input("Enter The Amount to Deposit: "))
                if c > 0:
                    Balance += c
                    print("Money Deposited Successfully \nYour Current Balance:", Balance)
                    c1 = input("Do You Want Receipt (yes/no): ")
                    if c1.lower() == "yes":
                        print("Receipt Printed Successfully. Please Collect Your Receipt")
                    else:
                        print("Thank You for Banking With U&I Bank")
                else:
                    print("Enter a Valid Amount to Deposit")          
            elif choice == 3:
                d = int(input("Enter Amount to Withdraw: "))
                if 0 < d <= Balance:
                    Balance -= d
                    print("Withdrawal Successful. Please Collect Your Cash")
                    d1 = input("Do You Want Receipt (yes/no): ")
                    if d1.lower() == "yes":
                        print("Receipt Printed Successfully. Please Collect Your Receipt")
                    else:
                        print("Thank You for Banking With U&I Bank")
                else:
                    print("Invalid Withdrawal Amount")            
            elif choice == 4:
                print("🚪 Exiting... Thank You for Banking With U&I Bank!🚪")
                break            
            else:
                print("Invalid Choice. Please Try Again.")        
        break  # Exit PIN loop after successful login    
    else:
        attempts += 1
        if attempts < max_attempts:
            print("❌ Wrong Pin. Please Try Again")
        else:
            print("❌ You Have Entered the Wrong Pin 3 Times \n🚫 Your Account is Blocked Please Contact the Bank.")
        

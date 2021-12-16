# Hello , Welcome to my yearly compound profit calculator
# Enjoy it

Money = float(input(f" How much Money do you have in your bank account? "))
Profit_rate = float(input(f" Yearly Profit rate?( exp: 0.05 for 5% )"))
years = int(input(f" After how many years ? "))
if Money <= 0:
    print('')
    print (" Go and find a job :\ ")
    
else: 
    
    if years>= 1 and 0 <= Profit_rate <= 1.00:
        
        for years in range(1,years+1):
            Acc_balance = Money * (Profit_rate + 1) ** years
            
            if years == 1 :
                print('')
                print( f'First year account balance = { round ( Acc_balance , 2 )}')
                
            else : 
                print( f'{years}th year account balance = { round ( Acc_balance , 2 )}')
                
        profit = round ( Acc_balance - Money , 2 )
        print('')
        print( f"** $$ Congratulation !! $$ ** All of your profit after {years} years is {profit} **")
        
    elif Profit_rate >= 1.00 :
        
        print('')
        print(" Your profit rate is over 100% and it's impossible.\n please pay more attention and try again :) ")
        
    elif Profit_rate < 0 :
        print('')
        print(" WTF! Give me your money , i need it more than f*ckin Banks :) ")
        
    else:   # YEARS <=0
        
        print('')
        print(f" Unfortunately you don't any profit before your first year ") 
    
# ©M.f4rahani    

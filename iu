#Trading account

import random

print("Your initial bank balance is 10000$")

#Defining Variables which need to be constant for the whole program
bankBalance = 10000
loanBalance = 0
z=0 #time period for loans
loanDict1={loanBalance:z}
loanDict2={loanBalance:z}
loanDict3={loanBalance:z}
loanDict4={loanBalance:z}
loanDict5={loanBalance:z}
StocksOwned = {1:0,2:0,3:0,4:0,5:0,6:0,7:0,8:0,9:0,10:0}
StocksList = {1:"Google", 2:"Bitcoin", 3:"Tata Motors", 4:"Reliance", 5:"Whirlpool", 6: "Tesla", 7: "Amazon", 8: "Apple Inc.", 9: "Gamestop", 10: "NASDAQ"}
StocksPrice = {1:300,2:1000,3:200,4:550,5:150,6:700,7:600,8:550,9:400,10:800}
InvestmentList = ["There are rumours that the government is going to ban bitcoin", "There was a reddit post urging people to buy Gamestop Shares as they increase in value",
                          "Sorry we have no tips at the current moment", "Tesla is releasing a new revolutionalry product soon", "Amazon stock is remoured to be very risky",
                          "Tata motors just lost a big deal with their manufacturers", "Whirlpool stock seems to be on a downward trend",  "Sorry we have no tips at the current moment",
                          "Apple recently changed CEOs. The stock price depends entirely on the performance of the new CEO!", "Sorry we have no tips at the current moment"]

#WhileLoop is created
whiloop = "y"
while whiloop != "n":
    print("\n\nWhat services would you like to use\n")

#This is the menu which contains all the options which the user will have.
    print("\na. Balance\nb. Trading stocks\nc. Loans\nd. Investment advice\ne. Deposits \n")
    choice = input("Enter your menu choice: ")

#Once the user chooses which menu, we have to use if blocks for each menu option


#INVESTMENT ADVICE
    elif choice == "d":
      print("This sub-menu gives tips on the market for a consultation fee of 300$")
      print()
      print("In order to get investment advice, you need to pay 300$ for consultation. However, there is no guarentee that it will help you.")
      wouldYou = input("Do you want to pay 300$ for the consultation?(y/n) ")
      if wouldYou == "y" and bankBalance >= 300:
        bankBalance = bankBalance - 300
        rando = (random.randint(0,9))
        print(InvestmentList[rando])
        InvestmentList[rando] = None
      print()
#LOANS
    elif choice == "c":
      #Here we need to print out a set of loan packages with simple and compound interest and different interest rates. Ask the user to choose.
      if bankBalance>=0 and loanBalance <= 4000:
        print()
        print("1.1200$ at 5% under Simple interest for 2 years")
        print("2.1700$ at 4% compounded for 3 years")
        print("3.3700$ at 6% under Simple interest for 3 years")
        print("4.2500 at 7% compounded for 1 year")
        print("5.Custom loan")
        print()
        choice=int(input("Which package would you like to choose: "))
        print()
        print()
        if choice==1:
          si=(60*2)
          print("The simple interest on this package is",si)
          print("Loan request has been accepted and you have been registered for this")
          loanBalance=(1200+si)
          z=(2*365)
          bankBalance+=1200
          loanDict1 = {loanBalance:z}
        if choice==2:
          ci=(1700*((1.04)**3))
          print("the compound interest on this package is:",ci)
          print("Loan request has been accepted and you have been registered for this")
          loanBalance=(1700+ci)
          z=(3*365)
          bankBalance+=1700
          loanDict2 = {loanBalance:z}
        if choice==3:
          si=(222*3)
          print("The simple interest on this package is",si)
          print("Loan request has been accepted and you have been registered for this")
          loanBalance=(3700+si)
          z=(3*365)
          bankBalance+=3700
          loanDict3 = {loanBalance:z}
        if choice==4:
          ci=(2500*(1.07**1))
          print("The compound interest on this package is:",ci)
          print("Loan request has been accepted and you have been registered for this")
          loanBalance=(2500+ci)
          z=(1*365)
          bankBalance+=2500
          loanDict4 = {loanBalance:z}
        if choice==5:
          P=float(input("Enter the amount required,amount requested:"))
          if P>=(0.3*bankBalance):
            print("Maximum limit is 30% of your balance")
          if P<1000:
            R=6
          if P>=1000:
            R=8
          compound=input("Would you like it to be compounded?:")
          simple=input("Would you like to be simple interest?:")
          if compound=='yes':
            ci=P*(((100+R)/100)**t)
            print("the compound interest on this package is:",ci)
            loanBalance=(P+ci)
            z=(t*365)
            bankBalance+=(P)
            print("Loan request has been accepted and you have been registered for this")
            loanDict5 = {loanBalance:z}
          if simple=='yes':
            si=(P*R*t)/100
            print("The simple interest on this package is",si)
            loanBalance=(P+si)
            z=(t*365)
            bankBalance+=(P)
            print("Loan request has been accepted and you have been registered for this")
            loanDict5 = {loanBalance:z}
      else:
        print("Bank balance below required limit,not eligible for a loan")
      loanDict= [['loan','days left'],[loanDict1],[loanDict2],[loanDict3],[loanDict4],[loanDict5]] #loan list for showing multiple loans taken at a time

#TRADING - BUY OR SELL
    elif choice == "b":
      print()
      buyOrSell = input("Would you like to buy or sell (b/s)? ")
     
      if buyOrSell == "b":
        print()
        print("The market currently offers 4 stocks:")
        l1 = random.sample(list(StocksList.keys()), 4)
        print("1.", StocksList[l1[0]], " - ", StocksPrice[l1[0]])
        print("2.", StocksList[l1[1]], " - ", StocksPrice[l1[1]])
        print("3.", StocksList[l1[2]], " - ", StocksPrice[l1[2]])
        print("4.", StocksList[l1[3]], " - ", StocksPrice[l1[3]])
        print()
              
        whichStock = int(input("Which stock do you want to buy?(1/2/3/4) "))
        numberOfStock = int(input("How many of that stock do you want to purchase? "))
        print()
        cost = StocksPrice[l1[whichStock-1]] * numberOfStock
        if bankBalance >= cost:
          StocksOwned[l1[whichStock-1]] += numberOfStock
          bankBalance -= cost
          print("Congratulations! You just purchased", numberOfStock, "stocks of", StocksList[l1[whichStock-1]])
          print("Your remaining bank balance is:", bankBalance)
          print()
        else:
          print("Insufficient Bank Balance")
          print()
      if buyOrSell == "s":
        for i in range(1,11,1):
          print(i, ". ", StocksList[i], " - ", StocksOwned[i], sep="")
          print()
        whichStock = int(input("Which stock of yours would you like to sell?(Enter menu number) "))
        numberOfStock = int(input("How many of that stock do you want to sell? "))
        print()
        if numberOfStock <= StocksOwned[whichStock]:
          StocksOwned[whichStock] -= numberOfStock
          if whichStock == 3 or whichStock == 5:
            #Stocks which will most probably lose money
            rando = random.randrange(80,170,10)
            print("Each stock of yours was sold for ", rando, "$", sep="")
            print("You earned a total of ", rando*numberOfStock, "$", sep="")
            bankBalance += rando*numberOfStock
          elif whichStock == 6 or whichStock == 7 or whichStock == 10:
            #Stocks which will definitely gain money
            rando = random.randrange(700,850,10)
            print("Each stock of yours was sold for ", rando, "$", sep="")
            print("You earned a total of ", rando*numberOfStock, "$", sep="")
            bankBalance += rando*numberOfStock
          elif whichStock == 4 or whichStock == 8:
            #Stocks which can go either way
            rando = random.randrange(450,660,10)
            print("Each stock of yours was sold for ", rando, "$", sep="")
            print("You earned a total of ", rando*numberOfStock, "$", sep="")
            bankBalance += rando*numberOfStock
          elif whichStock == 9:
            #Gamestop will rise massively
            rando = random.randrange(700,900,40)
            print("Each stock of yours was sold for ", rando, "$", sep="")
            print("You earned a total of ", rando*numberOfStock, "$", sep="")
            bankBalance += rando*numberOfStock
          elif whichStock == 1:
            #Stocks which can go either way
            rando = random.randrange(250,360,10)
            print("Each stock of yours was sold for ", rando, "$", sep="")
            print("You earned a total of ", rando*numberOfStock, "$", sep="")
            bankBalance += rando*numberOfStock
          elif whichStock == 2 :
            #Bitcoin will collapse
            rando = random.randrange(600,850,30)
            print("Each stock of yours was sold for ", rando, "$", sep="")
            print("You earned a total of ", rando*numberOfStock, "$", sep="")
            bankBalance += rando*numberOfStock
        else:
          print("You do not own enough stock")
      print()
      print()
#PORTFOLIO
    if choice == "a":
        print("\nYour bank balance is:", bankBalance)
        if loanBalance != 0:
          print("outgoing loans:",loanDict)
        for i in range(1,11):
          if StocksOwned[i] != 0:
            print("You own", StocksOwned[i], "stocks of", StocksList[i])




    if choice == "e":
      if bankBalance <2000.0:
        print("Insuffecient Bank Balance") 
        deposit_amount=int(input("How much money would you wish to deposit: ")) 
        while deposit_amount > 1600: 
          bankBalance-=deposit_amount
          print("Your bank balance is",bankBalance) 
          print("Your money is safe with us") 
        else: 
          print("It is suggested to deposit over $100 for account to remain open. ") 
          deposit_amount=int(input("How much money would you wish to deposit: ")) 
      else:
        deposit_amount=int(input("How much money would you wish to deposit: ")) 
        bankBalance-=deposit_amount 
        print("Your bank balance is",bankBalance) 
        print("Your money is safe with us")
    

    print()
    whiloop = input("Would you like to continue trading? (y/n) ")
    print()

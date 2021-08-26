# -*- coding: utf-8 -*-
"""
Created on Mon Aug 23 16:10:34 2021

@author: tp
"""
from time import ctime as t
import datetime
import pandas as pd
finv={'id':[], 'item':[ ], 'amount':[], 'unit price':[],'total price':[]}
new_products={}
invoice={'inv_id':[0], 'time':[], 'total':[]}
resturant={'notes':[]}
snacks={'salt': 0.75, 'potatos': 0.85, 'sause':0.25}
discounts={'3 persons meal': 5.5, '6 persons meal':9.5, '10 persons meal': 15}
basket={'item':[], 'amount':[], 'unit price':[], 'total price':[]}
beverages={'pepsi':0.30,'sprite':0.3,'fanta':0.3, 'pepsi dite':0.35}
sandwitches={'shawerma':0.6, 'burger':0.75, 'mexico':1.0, 'fajeta':1.25}
meals={'shawerma':1.50, 'italy':2, 'french':2, 'brousted':2.75}
departments={'meals':['shawerma', 'italy', 'french', 'brousted', 'burger'], 'sandwitches':['shawerma', 'burger', 'mexico', 'fajeta'], 'beverages':['pepsi', 'sprit', 'fanta', 'pepsi dite'], 'discounts':['3 persons meal', '6 persons meal', '10 persons meal'], 'snacks':['salt', 'potatos', 'sause']}
information={'email':[], 'username':[], 'passward':[], 'Phone Number':[], 'C/E':[], 'address':[]}
class Registeration:
    def __init__(self, username):
        self.username = username
    def register(self):
        
            user=input('please enter your email address or e / exit:')
            if user.lower()=='e':
                return 0
         
            for i in range (1,4):
                print('you have only 3 tries')
                pass1=input('enter you passward:')
                pass2=input('enter you passward again')
                if pass1==pass2:
                        print('welcome {}'.format(self.username))
                        number=input('enter your number')
                        address=input('enter your address')
                        information['passward'].append(pass1)
                        information['email'].append(user)
                        information['Phone Number'].append(number)
                        information['address'].append(address)
                        break
                else: 
                    print('wrong passward ,try again')
                    


    def log_in(self):
        email=input('enter your email address to LOGIN:')
        passward=input('enter your passward:')
        ind=information['email'].index(email)
        while True :
            if information['passward'][ind]==passward:
                print ('Welcome {}'.format(self.username))
                
            else:
                print('wrong enteration!!')
                print('try again later')
            break
      
        
class Customer:
    def __init__(self):
        self
    def meals(self):
        while True:
            pic=input('choose from the following meals/e for exit')
            if pic.lower() in meals.keys():
                size=str(input('enter size you want r/regular, m/medium, l/large'))
                if size.lower()=='m':
                    basket['unit price'].append(meals[pic]+0.35)
                    am=int(input('enter amount you want'))
                    basket['amount'].append(am)
                    total_amount=am*(meals[pic]+0.35)
                    basket['total price'].append(total_amount)
                elif size.lower()=='l':
                    basket['unit price'].append(meals[pic]+0.75)
                    am=int(input('enter amount you want'))
                    basket['amount'].append(am)
                    total_amount=am*(meals[pic]+0.75)
                    basket['total price'].append(total_amount)
                elif size.lower()=='r': 
                    basket['unit price'].append(meals[pic])
                    am=int(input('enter amount you want'))
                    basket['amount'].append(am)
                    total_amount=am*meals[pic]
                    basket['total price'].append(total_amount)
                
                else:
                    print('wrong enteration')
                    break
                basket['item'].append(pic)

            elif pic.lower()=='e':
                print('thx for join us')
                break
            else:
                print('wrong enteration')
                break
    def sandwitches(self):
        sandwitches.items()
        while True:
            pic=input('choose from the following sandwitches/e for exit')
            if pic.lower() in sandwitches.keys():
                size=str(input('enter size you want r/regular, m/medium, l/large'))
                if size.lower()=='m':
                    basket['unit price'].append(sandwitches[pic]+0.3)
                    am=int(input('enter amount you want'))
                    basket['amount'].append(am)
                    total_amount=am*(sandwitches[pic]+0.3)
                    basket['total price'].append(total_amount)
                elif size.lower()=='l':
                    basket['unit price'].append(sandwitches[pic]+0.6)
                    am=int(input('enter amount you want'))
                    basket['amount'].append(am)
                    total_amount=am*(sandwitches[pic]+0.6)
                    basket['total price'].append(total_amount)
                elif size.lower()=='r': 
                    basket['unit price'].append(sandwitches[pic])
                    am=int(input('enter amount you want'))
                    basket['amount'].append(am)
                    total_amount=am*sandwitches[pic]
                    basket['total price'].append(total_amount)
                else:
                    print('wrong enteration')
                    break
                basket['item'].append(pic)

            elif pic.lower()=='e':
                print('thx for join us')
                break
            else:
                print('wrong enteration')
                
                break
                
    def beverages(self):
        beverages.items()
        while True:
            pic=input('choose from the following beverages/e for exit')
            if pic.lower() in beverages.keys():
                size=str(input('enter size you want r/regular, m/medium, l/large'))
                if size.lower()=='m':
                    basket['unit price'].append(beverages[pic]+0.20)
                    am=int(input('enter amount you want'))
                    basket['amount'].append(am)
                    total_amount=am*(beverages[pic]+0.20)
                    basket['total price'].append(total_amount)
                elif size.lower()=='l':
                    basket['unit price'].append(beverages[pic]+0.35)
                    am=int(input('enter amount you want'))
                    basket['amount'].append(am)
                    total_amount=am*(beverages[pic]+0.35)
                    basket['total price'].append(total_amount)
                elif size.lower()=='r': 
                    basket['unit price'].append(beverages[pic])
                    am=int(input('enter amount you want'))
                    basket['amount'].append(am)
                    total_amount=am*beverages[pic]
                    basket['total price'].append(total_amount)
                else:
                    print('wrong enteration')
                    break
                basket['item'].append(pic)

            elif pic.lower()=='e':
                print('thx for join us')
                break
            else:
                print('wrong enteration')
                break
    
    def discounts(self):
        print('you will got 1 leter pepsi for each meal')
        discounts.items()
        while True:
            pic=input('choose from the following meals/e for exit')
            if pic.lower() in discounts.keys():
                basket['item'].append(pic)
                basket['unit price'].append(discounts[pic])
                am=int(input('enter amount you want'))
                basket['amount'].append(am)
                total_amount=am*discounts[pic]
                basket['total price'].append(total_amount)
            elif pic.lower()=='e':
                print('thx for join us')
                break
            else:
                print('wrong enteration')
                break
    def snacks(self):
        snacks.items()
        while True:
            pic=input('choose from the following snacks/e for exit')
            if pic.lower() in snacks.keys():
                size=str(input('enter size you want r/regular, m/medium, l/large'))
                if size.lower()=='m':
                    basket['unit price'].append(snacks[pic]+0.35)
                    am=int(input('enter amount you want'))
                    basket['amount'].append(am)
                    total_amount=am*(snacks[pic]+0.35)
                    basket['total price'].append(total_amount)
                elif size.lower()=='l':
                    basket['unit price'].append(snacks[pic]+0.65)
                    am=int(input('enter amount you want'))
                    basket['amount'].append(am)
                    total_amount=am*(snacks[pic]+0.65)
                    basket['total price'].append(total_amount)
                elif size.lower()=='r': 
                    basket['unit price'].append(snacks[pic])
                    am=int(input('enter amount you want'))
                    basket['amount'].append(am)
                    total_amount=am*snacks[pic]
                    basket['total price'].append(total_amount)
                else:
                    print('wrong enteration')
                    break
                basket['item'].append(pic)

            elif pic.lower()=='e':
                print('thx for join us')
                break
            else:
                print('wrong enteration')
                break         
    def newproducts(self):
        new_products.items()
        while True:
            pic=input('choose from the following items/e for exit')
            if pic.lower() in new_products.keys():
                size=str(input('enter size you want r/regular, m/medium, l/large'))
                if size.lower()=='m':
                    basket['unit price'].append(new_products[pic]+0.35)
                    am=int(input('enter amount you want'))
                    basket['amount'].append(am)
                    total_amount=am*(new_products[pic]+0.35)
                    basket['total price'].append(total_amount)
                elif size.lower()=='l':
                    basket['unit price'].append(new_products[pic]+0.65)
                    am=int(input('enter amount you want'))
                    basket['amount'].append(am)
                    total_amount=am*(new_products[pic]+0.65)
                    basket['total price'].append(total_amount)
                elif size.lower()=='r': 
                    basket['unit price'].append(new_products[pic])
                    am=int(input('enter amount you want'))
                    basket['amount'].append(am)
                    total_amount=am*new_products[pic]
                    basket['total price'].append(total_amount)
                else:
                    print('wrong enteration')
                    break
                basket['item'].append(pic)

            elif pic.lower()=='e':
                print('thx for join us')
                break
            else:
                print('wrong enteration')
                break         
    def notes(self):
        #if u have any note to become better market wrote it below
        notes=input('if you have any notes write it below: \n')
        with open('readme.txt', 'w') as f:
            f.write(notes)
            print('Thank you for join us')
            resturant['notes'].append(notes)

    def show_bill(self):
        import pandas as pd
        basket1=pd.DataFrame(basket)
        
        print(basket1)

    def remove_item(self):
        while True:
            ch=str(input('enter item name: '))
            if ch in basket['item']:
                basket['item'].remove(ch)
                basket['amount'].remove()
                basket['unit price'].remove()
                basket['total price'].remove()
                
                break
            else:
                print('item not found, rewrite again')

    def inv(self):
        inv_id=invoice['inv_id'][-1]+1
        for i in range(0,len(basket['amount'])):
            finv['id'].append(inv_id)
            finv['item'].append(basket['item'][i])
            finv['amount'].append(basket['amount'][i])
            finv['unit price'].append(basket['unit price'][i])
            finv['total price'].append(basket['amount'][i]*basket['unit price'][i])

        invoice['inv_id'].append(inv_id)
        time = t()
        invoice['time'].append([time])
        finv=pd.DataFrame({finv:[]})
        print(finv)  
        

  
class employee:
    def __init__(self):
        self
    def Creat_dep(self):
        while True:
            dep=input('enter department name to creat /e for exit')
            if dep in departments.keys():
                print('department already exist')
            elif dep.lower()=='e':
                break
                
            departments.update({dep:[]})
            
    def add_product(self):
         dep=input('For which department you want to add product')
         if dep in departments.keys():
             p_name=input('enter the product name you want to add: ')
             if p_name in departments.keys():#if the product name exsists in the department printe(exsist)
                 print ('product already exsist')
             p_price=float(input('enter product price Format{9.99} JD: '))
            
             departments[dep].append(p_name)
             new_products.update({p_name:p_price})
             print('product added succesfully')
    def edit():
        ch=input('enter p to edit product  E exit: ')
        while True:
            print(departments.keys())
            if ch.lower()=='p':
                meals.items()
                sandwitches.items()
                snacks.items()
                beverages.items()
                new_products.items()
                x=input('from which dep you want to edit m/meals, s/sandwitches, b/beverage, w/new_products, n/snacks, d/discounts')
                if x.lower()=='m':
                    p_name=input('enter product name: ')
                    if p_name in meals:
                        n_price=float(input('enter new price Format {9.99} JD or E'))
                        meals[p_name]=n_price
                        print('succesfully done')
                elif x.lower()=='s':
                     p_name=input('enter product name: ')
                     if p_name in sandwitches:
                        n_price=float(input('enter new price Format {9.99} JD or E'))
                        sandwitches[p_name]=n_price
                        print('succesfully done')
                elif x.lower()=='n':
                    p_name=input('enter product name: ')
                    if p_name in snacks:
                        n_price=float(input('enter new price Format {9.99} JD or E'))
                        snacks[p_name]=n_price
                        print('succesfully done')
                elif x.lower()=='w':
                    p_name=input('enter product name: ')
                    if p_name in new_products:
                        n_price=float(input('enter new price Format {9.99} JD or E'))
                        new_products[p_name]=n_price
                        print('succesfully done')
                elif x.lower()=='b':
                    p_name=input('enter product name: ')
                    if p_name in beverages:
                        n_price=float(input('enter new price Format {9.99} JD or E'))
                        beverages[p_name]=n_price
                        print('succesfully done')
                elif x.lower()=='d':
                    p_name=input('enter product name: ')
                    if p_name in discounts:
                        n_price=float(input('enter new price Format {9.99} JD or E'))
                        discounts[p_name]=n_price
                        print('succesfully done')               
                else:
                    print('wrong enteration')
                    break
            elif ch.lower()=='e':
                print('exit...')
                break
               
        
    
def main():
    kh=Registeration('khaled')
    r=input('''choose form the following numbers:
            1-SIGN UP
            2-LOGIN
            3-EXIT''')     
    while True:
        if r.lower()=='1':
            kh.register()
            kh.log_in()
            manage()
        elif r.lower()=='2':
            kh.log_in()
            manage()
            print(f'Welcome {email}')
        elif r.lower()=='3':
            break
        else:
            print('wrong enteration!!!, try again')
           
def manage():      
    while True:
        c=input('''Are you
                1-CUSTOMER
                2-EMPLOYEE''')
        if c.lower()=='1':
            al=Customer()
            information['C/E'].append('customer')
            while True:
                cho=input('''choose from the following numbers: 
                          1- meals: 
                          2- sandwitches:
                          3-snacks:
                          4-new_products:
                          5-discounts:
                          6-beverages:
                          7-show bill / remove items:
                          8-invoice
                          9-add notes
                          e- exit''')
                if cho=='1':
                    x=meals.items()
                    print(x)
                    print('''The mentioned price is for regular meal\n
                          for medium size you have to pay the regular meal price + 0.35 \n
                          for large size you have to pay the regular meal price + 0.75''')
                    
                    al.meals()
                elif cho=='2':
                    x=sandwitches.items()
                    print(x)
                    print(''' The mentioned price is for regular meal\n
                              for medium size you have to pay the regular meal price + 0.30 \n
                              for large size you have to pay the regular meal price + 0.60''')
                    al.sandwitches()
                elif cho=='3':
                    x=snacks.items()
                    print(x)
                    print('''The mentioned price is for regular meal\n
                          for medium size you have to pay the regular meal price + 0.35 \n
                          for large size you have to pay the regular meal price + 0.65''')                    
                    al.snacks()
                elif cho=='4':
                    x=new_products.items()
                    print(x)
                    print('''The mentioned price is for regular meal\n
                          for medium size you have to pay the regular meal price + 0.35 \n
                          for large size you have to pay the regular meal price + 0.65''')                    
                    al.newproducts()
                elif cho=='5':
                    x=discounts.items()
                    print(x)
                    
                    al.discounts()
                elif cho=='6':
                    x=beverages.items()
                    print(x)
                    al.beverages()
                elif cho=='7':
                    al.show_bill()
                    ch=input('Do you want to remove item? Y/N')
                    if ch.upper()=='Y':
                        al.remove_item()
                    else:
                        break
                elif cho=='8':
                    al.inv()
                elif cho=='9':
                    al.notes()
                elif cho.lower()=='e':
                    break
                
                else:
                    print('wrong enteration')
                    continue
                
        elif c.lower()=='2':
            for i in range (1,4):
                pa=input('enter employees passward, you have only 3 tries')
                if pa=='KST':
                    information['C/E'].append('employee')
                    print('WELCOME ')
                    j=employee
                    while True:
                        cho=input('''choose from the following numbers: 
                                  1- creat department: 
                                  2- add products:
                                  3-edit price:
                                  ''')
                        if cho=='1':
                            j.Creat_dep()
                        elif cho=='2':
                            j.add_product()
                        elif cho=='3':
                            j.edit()
                        else:
                            print('wrong enteration')
                            break 
                else:
                    print('wrong passward')
                    
        else:
            print('wrong enteration')
            kh=Registeration('khaled')
            kh.log_in()
        

    
        
while True:
    main()         

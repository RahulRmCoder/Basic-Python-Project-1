import pandas as pd

print("Store name: PYMART")
print('Address: JP Nagar Bengaluru')
print("Timing: 9:00am - 9:00pm")

dict1 = {'Items': ['Apples', 'Oranges', 'Guava', 'Stawberry', 'Mangoes'],
         'Prize per fruit in $': [5, 3, 3, 2, 5],
         'Quantity': [10, 10, 10, 10, 10]}

list_items = pd.DataFrame(dict1)
print()
print('ITEM LIST')
print()
print(list_items)

num = int(input("How many items you want to buy:"))
print()
tprice=0
for i in range(num):
    fruits = input("Enter the name of the item you want to buy: ").capitalize()
    print()
    quantity = int(input("Enter the quantity of item: "))
    print()
    if fruits in list_items['Items'].tolist():
        item_index = list_items.index[list_items['Items'] == fruits].tolist()[0]
        if quantity <= list_items.loc[item_index, 'Quantity']:
            list_items.loc[item_index, 'Quantity'] -= quantity
            p= list_items.loc[item_index,'Prize per fruit in $']
            price=p*quantity
            print("You've purchased",quantity,fruits,".")
        else:
            print("Sorry, we don't have enough quantity available.")
        tprice+=price
    else:
        print("Item not found in the store.")
print()
print()
print()
print("TOTAL AMOUNT TO BE PAID:",tprice,"$")
print()
print()
print("THANK YOU FOR SHOPPING!")
        
print()
print('UPDATED ITEM LIST')
print()
print(list_items)

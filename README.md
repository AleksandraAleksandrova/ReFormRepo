# PreFormRepo
1. choosing a file 
2. deleting the needless columns 
3. saperating the registration 
4. calculating the quantity 
5. putting this number in a column 
6. putting the initials of the country, in which the transaction was made, in a new column
7. calculating and printing the net value of the customer's currency in a new column
8. calculating and printing the unit price in the last column 

Steps v2 by Vesko

1. Choose an input file

2. Keep columns with descriptions:
    Държава, в която е направена трансакцията
    Регистрационен номер на превозно средство
    Код на продукт
    Количество
    Нетна стойност във валута на клиента
Delete the rest columns

3. Keep only groups 30,32,33 and 36 from "Код на продукт". Delete the rest rows

4. Check for thousands separator issues in the columns  "Нетна стойност във валута на клиента" and "Количество"

5. Calculate and save new column"Еденична цена" - divide "Нетна стойност във валута на клиента" / "Количество", round the amount to the second digit (e.g. xx,yy лв.)

6. Move inside separate sheet every entry by using the "Регистрационен номер на превозно средство" as key and name for the page. 
All entries without "Регистрационен номер на превозно средство" should go to "missing data" sheet.

7. Save the resulting file, display end message.

Proposal for Java library to parse xls files (Java 8 compatible):
   
http://poi.apache.org/

  
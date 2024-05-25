# SI_2024_lab2_222006
Ime:Anastasija  
Prezime: Maksimovska
Indeks:222006
Control Flow Graph
![CFG222006](https://github.com/stejsi123/SI_2024_lab2_222006/assets/139148203/8b44cdc7-d372-45d6-b0d9-b50f05efb466)
ЦИКЛОМАТСКА СЛОЖЕНОСТ
1
2
3
4.1
4.2
4.3
5
6
7
8
9
10
11.1
11.2
11.3
12
13
14
15
16
17
18
19
20
21
22
23
24
NUMBER OF NODES:28
NUMBER OF EDGES:36
Пресметуванје на цикломатската сложеност:
Цикломатска сложеност=36(number of edges)-28(number of nodes)+2*1(вообичаено P=1 за една програма)
Цикломатска сложеност=10
Објаснување:
Значи, цикломатската сложеност на функцијата checkCart е 10. Ова покажува дека има 10 независни патеки низ функцијата, што е мерка за нејзината сложеност.
Тест случаи според критериумот EVERY BRANCH
![image](https://github.com/stejsi123/SI_2024_lab2_222006/assets/139148203/612c1aed-ae00-4f5b-8e8a-f332ff9a1bf9)
MULTIPLE CONDITION
За да го задоволиме Multiple Condition критериумот треба да ги земеме во предвид сите можни boolean под-комбинации.
1.A: item.getPrice() > 300
2.B: item.getDiscount() > 0
3.C: item.getBarcode().charAt(0) == '0'
Имаме 8 можни комбинации бидејќи 2^3=8, тие можат да бидат или true или false

Test Case	A: item.getPrice() > 300	B: item.getDiscount() > 0	C:item.getBarcode().charAt(0) == '0'	Expected Result
1			true				true					true				true
2			true				true					false				false
3			true				false					true				false
4			true				false					false				false
5			false				true					true				false
6			false				true					false				false
7			false				false					true				false
8			false				false					false				false

Тест случај 1: Сите услови се точни
Влез: Item=["item1", "012345", 350, 0,1], payment = 400
Очекуван излез: Точно (бидејќи цената е намалена за 30)
Објаснување: Ова го опфаќа случајот кога A е true, Б е true, а C е true.

Тест случај 2: Цената и discount е true, barcode false
Влез: Item=["item1", "112345", 350, 0,1], payment = 400
Очекуван излез: Неточно
Објаснување: Ова го опфаќа случајот кога А е treu, Б е true, а C е false.

Тест случај 3: Точна цена, попуст неточно, точно баркод точно
Влез: Item=["item1", "112345", 350, 0], payment = 400
Очекуван излез: неточно
Објаснување: Ова го опфаќа случајот кога А е true, Б е false, а C е true.

Тест случај 4: Точна цена, попуст неточно, баркод неточно
Влез: Item=["item1", "112345", 350, 0], payment = 400
Очекуван излез: неточно
Објаснување: Ова го опфаќа случајот кога А е true, Б е false, а C е false.

Тест случај 5: Цена неточна, попуст точно, точно баркод
Влез: Item=["item1", "012345", 250, 0,1], payment = 400
Очекуван излез: Точно
Објаснување: Ова го опфаќа случајот кога А е false, Б е true, а C е true.

Тест случај 6: Цената неточна, попуст вистина, баркод неточно
Влез: Item=["item1", "112345", 350, 0,1], payment = 400
Очекуван излез: неточно
Објаснување: Ова го опфаќа случајот кога А е false, Б е true, а C е false.

Тест случај 7: Цена неточна, попуст неточна, точно баркод точно
Влез: Item=["item1", "012345", 250, 0], payment = 400
Очекуван излез: неточно
Објаснување: Ова го опфаќа случајот кога А е false, Б е false, а C е true.

Тест случај 8: Сите услови се неточни

Влез: Item=["item1", "112345", 250, 0], payment = 400
Очекуван излез: неточно
Објаснување: Ова го опфаќа случајот кога А е false, Б е false, а Ц е false.




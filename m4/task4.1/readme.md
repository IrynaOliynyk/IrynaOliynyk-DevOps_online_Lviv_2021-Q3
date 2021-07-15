
TASK 4.1

1. Зібратинаступнийпроект(рис1), якийміститьвсобі: 4 ПКтипуPC-PT, Концентратор(Hub-PT). Кожен  комп'ютер  повинен  бути  з'єднаний  з концентратором за допомогою крученоїпари(CopperStraight-through).

![image](https://user-images.githubusercontent.com/58170246/125827815-4ce1fbe9-94fc-481d-9138-32e9de9b1279.png)

![image](https://user-images.githubusercontent.com/58170246/125828462-8d7f6928-1f33-4625-b0d9-ff45a4476fa8.png)

![image](https://user-images.githubusercontent.com/58170246/125830512-df4e36bf-dea2-42e4-a77f-ab11d5668ba9.png)

![image](https://user-images.githubusercontent.com/58170246/125830706-e9bf91f7-b500-44f8-a4ce-a776b7858b39.png)

![image](https://user-images.githubusercontent.com/58170246/125830754-8feafe9a-5ff6-486e-8b2b-e153966a8cc6.png)

![image](https://user-images.githubusercontent.com/58170246/125831602-55df53d3-b878-49ea-a1ab-959ef1881530.png)

![image](https://user-images.githubusercontent.com/58170246/125831647-4acd843f-072c-4bd9-a8b5-4e75ff23c699.png)

![image](https://user-images.githubusercontent.com/58170246/125831678-6d342fd3-1aba-4a79-9430-a42ee97d143f.png)

![image](https://user-images.githubusercontent.com/58170246/125831708-dbbda98c-925d-4347-965e-08aa389b1fa7.png)

![image](https://user-images.githubusercontent.com/58170246/125831770-a3293e49-30ef-43de-b921-602ddbc19428.png)

![image](https://user-images.githubusercontent.com/58170246/125831844-1a72f8d8-ff09-4abc-af56-86d39c549dc2.png)

без IP адрессмережа не працює

![image](https://user-images.githubusercontent.com/58170246/125832174-57546731-d655-43ad-ae82-ea30dad255dd.png)

![image](https://user-images.githubusercontent.com/58170246/125832206-604cd968-ad9e-4580-8bce-1d46ee39cff5.png)

Hab не знає куди направляти пакети.

Робота мережі відбувається наступним чином пакет відправляється на Hab потім не кожний  компютер в мережі. Далі  компютери  перевіряють адрессу адресата. коли адресса не збігається, компютер не приймає пакет. коли адреса  збіглася, підтвердження відправляється на Hab після нього знову на усі  компютери  мережі.  Але  пакет приймає лише компютер з потрібним IP.



2.  Зібрати наступний проект (рис. 5). У нього входять: PC0-PC5, Server, 2  Hubs.  Однойменні  пристрої  з'єднуються  за  допомогою  кросового  кабелю (Copper Cross-over)

![image](https://user-images.githubusercontent.com/58170246/125838516-5065dffb-9220-40bd-b1a5-bf9ba63fd597.png)


![image](https://user-images.githubusercontent.com/58170246/125838561-78c2cd04-d0fd-43fc-bc1b-4e29970ad9e6.png)

![image](https://user-images.githubusercontent.com/58170246/125838615-9cf0d8ef-18ae-440a-9fd5-368ebfbf0b0d.png)

![image](https://user-images.githubusercontent.com/58170246/125838639-595ac7ba-6576-4ef9-a9b4-14fb15c6b2ae.png)

![image](https://user-images.githubusercontent.com/58170246/125838766-c5ef818f-09b4-453a-b2d4-54d9d347fe68.png)

![image](https://user-images.githubusercontent.com/58170246/125838877-5e31ddd6-9d27-4b48-ba70-ef3f8facf876.png)

![image](https://user-images.githubusercontent.com/58170246/125838915-57aa5476-544c-4c00-8af6-2901b5cfa281.png)


3. Створити  новий  проект,  який  включає  в  себе:  4  ПК  типу  PC-PT, Комутатор    (Switch).    Кожен    комп'ютер    повинен    бути    з'єднаний    з концентратором  за допомогою  крученоїпари  (Copper  Straight-through) 

![image](https://user-images.githubusercontent.com/58170246/125839853-e4add50f-1c95-49a2-9a0d-ec393e501f5e.png)

![image](https://user-images.githubusercontent.com/58170246/125839941-4365c0c0-ae5b-4f96-b6d7-30015d561bfe.png)

![image](https://user-images.githubusercontent.com/58170246/125839997-fc20bed3-5d66-44f3-8bb8-e8afc403c4e5.png)

свіч на відміну  від хабу запамятовує IP адрессу, тобто після першого відправлення на хости, він запамятовує шлях. І нразад відповідь йде вже по правильному шляху.

4. Розширити проект до такого вигляду (рис. 7). У нього входять: 8 ПК типу PC-PT, 2 комутатори (Switch). Кожен комп'ютер повинен бути з'єднаний з   комутатором   за   допомогою   крученоїпари   (Copper   Straight-through), комутатори  між  собою з'єднуються  за допомогою кросового кабелю (Copper Cross-over).

![image](https://user-images.githubusercontent.com/58170246/125840267-c4b6e386-c631-440a-97ea-10ae7666e027.png)

![image](https://user-images.githubusercontent.com/58170246/125840680-d15584c6-8d2c-48a0-89f6-e9064c11b23d.png)

![image](https://user-images.githubusercontent.com/58170246/125840704-4e6731b4-a417-458b-9566-bd50b19b0858.png)

![image](https://user-images.githubusercontent.com/58170246/125840780-a9d68444-278b-4a28-9777-8acfde705dd0.png)

5. Існуючу  мережу  розбити  на  дві  рівні  підмережі.  І  з'єднати  їх  за допомогою   маршрутизатора   Router-PT   з   декількома   портами   (рис.   8). Маршрутизатор і комутатори з'єднати між собою за допомогою оптоволокна (Fiber)

![image](https://user-images.githubusercontent.com/58170246/125842327-25a6da04-6ec8-43dd-ac47-8490bb852395.png)


![image](https://user-images.githubusercontent.com/58170246/125841902-41119b5c-3216-4449-ad18-eb215ac83e4d.png)

![image](https://user-images.githubusercontent.com/58170246/125842610-f74f76e0-da59-4328-b122-b7f96cef0582.png)

![image](https://user-images.githubusercontent.com/58170246/125843159-4b4c6706-a9f2-430c-ba29-4a8d3c69bd95.png)

На відміну від четвертої топології, п'ята мала дві різні мережі. Цей приклад наочно демонструє, що маршрутизатор, як правило, з'єднує принаймні дві мережі разом, наприклад, дві локальні мережі, дві глобальні мережі або локальну мережу та її мережу ISP.







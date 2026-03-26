# Практическая работа №2. Основы XML-разметки. Менеджеры размещения LinearLayout и GridLayout
Выполнила: Тристан Владислава Дмитриевна ИНС-б-о-24-2 

# Цель работы 
Изучить основы языка разметки XML для описания пользовательского интерфейса Android-приложений. Научиться использовать менеджеры размещения (контейнеры) LinearLayout и GridLayout для создания сложных экранов. Освоить основные атрибуты View и создание простых Drawable-ресурсов.

# Ход работы 
Задание 1. Создание проекта и подготовка ресурсов.

 1.1. Создайте новый проект с шаблоном Empty Views Activity. Назовите проект LayoutsLab.
<img width="897" height="608" alt="Снимок экрана 2026-03-25 151817" src="https://github.com/user-attachments/assets/54371e6e-1c3a-47f4-ae36-31bc711a6019" />

 1.2.- 1.3. В паке res/drawable создайте два файла rectangle.xml и circle.xml. Заполните их содержимым, как показано в теоретической части.
<img width="612" height="186" alt="Снимок экрана 2026-03-25 151516" src="https://github.com/user-attachments/assets/19c8cda6-116d-4b2a-9e89-e9bd235ecc40" />

Задание 2. Работа с LinearLayout.

 2.1. Откройте файл activity_main.xml. 
 
 2.2. Создайте веритикальный LinearLayout с тремя ImageView, отображающими созданные drawable-ресурсы.
 
 2.3. Запустите приложение и убедитесь, что фигуры отображаются вертикально.
<img width="814" height="755" alt="Снимок экрана 2026-03-26 143321" src="https://github.com/user-attachments/assets/54c87677-ca2b-44c0-a2e8-b2af5297863a" />

Задание 3. Изменение ориентации и выравнивания.

3.1. Измените android:orientation на horizontal. Посмотрите, как изменится расположение.

<img width="1024" height="863" alt="Снимок экрана 2026-03-26 144059" src="https://github.com/user-attachments/assets/384f9540-4b40-47e8-8362-5a1c4dba216f" />

3.2. Добавьте к LinearLoyout атрибут android:layoutDirection="rtl". Запустите и посмотрите на расположение эдементов.

<img width="995" height="850" alt="Снимок экрана 2026-03-26 144743" src="https://github.com/user-attachments/assets/28f40a57-7af9-465a-8e55-8715a67a6dbc" />

3.3. Верните ориентацию на вертикальную и поэксперементируйте с android:graviry у родителя и android:layout_gravity у дочерних элементов. 

<img width="1165" height="689" alt="Снимок экрана 2026-03-26 145218" src="https://github.com/user-attachments/assets/2d0e09a2-21b1-4ca5-b8e8-b15c604b3c46" />

Задание 4. Работа с GridLayout.
4.1. Создайте новый XML-файл разметки activity_grid.xml 

4.2. Используйте Gird













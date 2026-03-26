# Практическая работа №2. Основы XML-разметки. Менеджеры размещения LinearLayout и GridLayout
Выполнила: Тристан Владислава Дмитриевна ИНС-б-о-24-2 

# Цель работы 
Изучить основы языка разметки XML для описания пользовательского интерфейса Android-приложений. Научиться использовать менеджеры размещения (контейнеры) LinearLayout и GridLayout для создания сложных экранов. Освоить основные атрибуты View и создание простых Drawable-ресурсов.

# Ход работы 
# Задание 1. Создание проекта и подготовка ресурсов.

 1.1. Создайте новый проект с шаблоном Empty Views Activity. Назовите проект LayoutsLab.
<img width="897" height="608" alt="Снимок экрана 2026-03-25 151817" src="https://github.com/user-attachments/assets/54371e6e-1c3a-47f4-ae36-31bc711a6019" />

 1.2.- 1.3. В паке res/drawable создайте два файла rectangle.xml и circle.xml. Заполните их содержимым, как показано в теоретической части.
<img width="612" height="186" alt="Снимок экрана 2026-03-25 151516" src="https://github.com/user-attachments/assets/19c8cda6-116d-4b2a-9e89-e9bd235ecc40" />

# Задание 2. Работа с LinearLayout.

 2.1. Откройте файл activity_main.xml. 
 
 2.2. Создайте веритикальный LinearLayout с тремя ImageView, отображающими созданные drawable-ресурсы.
 
 2.3. Запустите приложение и убедитесь, что фигуры отображаются вертикально.
<img width="814" height="755" alt="Снимок экрана 2026-03-26 143321" src="https://github.com/user-attachments/assets/54c87677-ca2b-44c0-a2e8-b2af5297863a" />

# Задание 3. Изменение ориентации и выравнивания.

3.1. Измените android:orientation на horizontal. Посмотрите, как изменится расположение.

<img width="1024" height="863" alt="Снимок экрана 2026-03-26 144059" src="https://github.com/user-attachments/assets/384f9540-4b40-47e8-8362-5a1c4dba216f" />

3.2. Добавьте к LinearLoyout атрибут android:layoutDirection="rtl". Запустите и посмотрите на расположение эдементов.

<img width="995" height="850" alt="Снимок экрана 2026-03-26 144743" src="https://github.com/user-attachments/assets/28f40a57-7af9-465a-8e55-8715a67a6dbc" />

3.3. Верните ориентацию на вертикальную и поэксперементируйте с android:graviry у родителя и android:layout_gravity у дочерних элементов. 

<img width="1165" height="689" alt="Снимок экрана 2026-03-26 145218" src="https://github.com/user-attachments/assets/2d0e09a2-21b1-4ca5-b8e8-b15c604b3c46" />

# Задание 4. Работа с GridLayout.
4.1. Создайте новый XML-файл разметки activity_grid.xml 

4.2. Используйте GirdLayout для создания таблицы кнопок 3х3
<img width="817" height="699" alt="Снимок экрана 2026-03-26 150015" src="https://github.com/user-attachments/assets/6c345e62-e377-4a76-8941-ac4a2ad244ef" />

4.3. Создайте соответсвующую Activity и запустите её.

<img width="462" height="707" alt="Снимок экрана 2026-03-26 150951" src="https://github.com/user-attachments/assets/ae3d5aa7-1f18-428c-b096-7fd74311bf6b" />

# Задание 5. Объединение ячеек в GirdLayout
Создайте разметку, аналогичную примеру из теории, где одна кнопка занимает две ячейки по горизонтали.
<img width="502" height="802" alt="Снимок экрана 2026-03-26 151248" src="https://github.com/user-attachments/assets/e580f73b-6b77-49c8-b26a-3d5133609e1a" />

# Задания для самостоятельного выполнения.
Часть 1. Базовое задание.
1. Реализуйте размещение элементов, как на Рисунке 5 из исходного документа. Используйте горизонтальные и вертикальные контейнеры.

```java
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    android:padding="16dp">

    <!-- Верхняя горизонтальная секция -->
    <LinearLayout
        android:layout_width="match_parent"
        android:layout_height="0dp"
        android:layout_weight="1"
        android:orientation="horizontal"
        android:gravity="center"
        android:layout_marginBottom="16dp">

        <View
            android:layout_width="0dp"
            android:layout_height="match_parent"
            android:layout_weight="1"
            android:background="#FF5722"
            android:layout_margin="8dp"/>

        <View
            android:layout_width="0dp"
            android:layout_height="match_parent"
            android:layout_weight="1"
            android:background="#4CAF50"
            android:layout_margin="8dp"/>

    </LinearLayout>

    <!-- Средняя вертикальная секция -->
    <LinearLayout
        android:layout_width="match_parent"
        android:layout_height="0dp"
        android:layout_weight="1"
        android:orientation="vertical"
        android:gravity="center"
        android:layout_marginBottom="16dp">

        <View
            android:layout_width="match_parent"
            android:layout_height="0dp"
            android:layout_weight="1"
            android:background="#2196F3"
            android:layout_margin="8dp"/>

        <View
            android:layout_width="match_parent"
            android:layout_height="0dp"
            android:layout_weight="1"
            android:background="#FFC107"
            android:layout_margin="8dp"/>

    </LinearLayout>

    <!-- Нижняя сложная секция (горизонтальная + вертикальная) -->
    <LinearLayout
        android:layout_width="match_parent"
        android:layout_height="0dp"
        android:layout_weight="1"
        android:orientation="horizontal">

        <LinearLayout
            android:layout_width="0dp"
            android:layout_height="match_parent"
            android:layout_weight="1"
            android:orientation="vertical"
            android:layout_marginEnd="8dp">

            <View
                android:layout_width="match_parent"
                android:layout_height="0dp"
                android:layout_weight="1"
                android:background="#9C27B0"
                android:layout_marginBottom="8dp"/>

            <View
                android:layout_width="match_parent"
                android:layout_height="0dp"
                android:layout_weight="1"
                android:background="#FF4081"/>

        </LinearLayout>

        <LinearLayout
            android:layout_width="0dp"
            android:layout_height="match_parent"
            android:layout_weight="1"
            android:orientation="vertical">

            <View
                android:layout_width="match_parent"
                android:layout_height="0dp"
                android:layout_weight="1"
                android:background="#00BCD4"
                android:layout_marginBottom="8dp"/>

            <View
                android:layout_width="match_parent"
                android:layout_height="0dp"
                android:layout_weight="1"
                android:background="#FF9800"/>

        </LinearLayout>

    </LinearLayout>

</LinearLayout>
```
<img width="445" height="734" alt="Снимок экрана 2026-03-26 153424" src="https://github.com/user-attachments/assets/397087c3-8ea9-4128-a6c7-cc8753c03160" />

2. Нарисуйте на экране композицию, представленную на Рисунке 8 из исходного документа. Используйте View с установленным android:background для цветных блоков.

```java
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    android:padding="16dp"
    android:background="#F5F5F5">
    
    <!-- Первая строка: 3 прямоугольника -->
    <LinearLayout
        android:layout_width="match_parent"
        android:layout_height="0dp"
        android:layout_weight="1"
        android:orientation="horizontal"
        android:layout_marginBottom="16dp">
        
        <View
            android:layout_width="0dp"
            android:layout_height="match_parent"
            android:layout_weight="1"
            android:background="#FF0000"
            android:layout_margin="4dp"/>
        
        <View
            android:layout_width="0dp"
            android:layout_height="match_parent"
            android:layout_weight="1"
            android:background="#00FF00"
            android:layout_margin="4dp"/>
        
        <View
            android:layout_width="0dp"
            android:layout_height="match_parent"
            android:layout_weight="1"
            android:background="#0000FF"
            android:layout_margin="4dp"/>
        
    </LinearLayout>
    
    <!-- Вторая строка: 2 прямоугольника (один широкий) -->
    <LinearLayout
        android:layout_width="match_parent"
        android:layout_height="0dp"
        android:layout_weight="1"
        android:orientation="horizontal"
        android:layout_marginBottom="16dp">
        
        <View
            android:layout_width="0dp"
            android:layout_height="match_parent"
            android:layout_weight="2"
            android:background="#FF9800"
            android:layout_margin="4dp"/>
        
        <View
            android:layout_width="0dp"
            android:layout_height="match_parent"
            android:layout_weight="1"
            android:background="#9C27B0"
            android:layout_margin="4dp"/>
        
    </LinearLayout>
    
    <!-- Третья строка: 3 прямоугольника разных цветов -->
    <LinearLayout
        android:layout_width="match_parent"
        android:layout_height="0dp"
        android:layout_weight="1"
        android:orientation="horizontal"
        android:layout_marginBottom="16dp">
        
        <View
            android:layout_width="0dp"
            android:layout_height="match_parent"
            android:layout_weight="1"
            android:background="#FFC107"
            android:layout_margin="4dp"/>
        
        <View
            android:layout_width="0dp"
            android:layout_height="match_parent"
            android:layout_weight="1"
            android:background="#00BCD4"
            android:layout_margin="4dp"/>
        
        <View
            android:layout_width="0dp"
            android:layout_height="match_parent"
            android:layout_weight="1"
            android:background="#E91E63"
            android:layout_margin="4dp"/>
        
    </LinearLayout>
    
    <!-- Четвертая строка: сложная композиция -->
    <LinearLayout
        android:layout_width="match_parent"
        android:layout_height="0dp"
        android:layout_weight="1"
        android:orientation="horizontal">
        
        <View
            android:layout_width="0dp"
            android:layout_height="match_parent"
            android:layout_weight="1"
            android:background="#3F51B5"
            android:layout_margin="4dp"/>
        
        <LinearLayout
            android:layout_width="0dp"
            android:layout_height="match_parent"
            android:layout_weight="1"
            android:orientation="vertical">
            
            <View
                android:layout_width="match_parent"
                android:layout_height="0dp"
                android:layout_weight="1"
                android:background="#4CAF50"
                android:layout_margin="4dp"/>
            
            <View
                android:layout_width="match_parent"
                android:layout_height="0dp"
                android:layout_weight="1"
                android:background="#FF5722"
                android:layout_margin="4dp"/>
            
        </LinearLayout>
        
    </LinearLayout>
    
</LinearLayout>
```
<img width="453" height="740" alt="Снимок экрана 2026-03-26 153824" src="https://github.com/user-attachments/assets/7af44e79-687c-4f6c-bf96-7541b1c40c20" />

Часть2. Задание по варианту.
Используя менеджеры размещения LinearLayout и/или GridLayout, создайте указанную композицию из кнопок. Для вариантов 1-7 используйте соответсвующие рисунки из исходного документа (Рисунки 9-15). Для враинтов 8-10 создайте буквы из кнопок. Вариант 3. 

```java
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    android:padding="16dp"
    android:background="#F5F5F5">
    
    <!-- Дисплей -->
    <TextView
        android:layout_width="match_parent"
        android:layout_height="100dp"
        android:background="#FFFFFF"
        android:text="0"
        android:textSize="36sp"
        android:gravity="end|center_vertical"
        android:padding="16dp"
        android:layout_marginBottom="16dp"/>
    
    <GridLayout
        android:layout_width="match_parent"
        android:layout_height="0dp"
        android:layout_weight="1"
        android:columnCount="4"
        android:rowCount="6"
        android:padding="4dp">
        
        <!-- Строка 1: C CE % √ -->
        <Button
            android:layout_width="0dp"
            android:layout_height="0dp"
            android:layout_columnWeight="1"
            android:layout_rowWeight="1"
            android:layout_margin="4dp"
            android:text="C"
            android:background="#E0E0E0"/>
        
        <Button
            android:layout_width="0dp"
            android:layout_height="0dp"
            android:layout_columnWeight="1"
            android:layout_rowWeight="1"
            android:layout_margin="4dp"
            android:text="CE"
            android:background="#E0E0E0"/>
        
        <Button
            android:layout_width="0dp"
            android:layout_height="0dp"
            android:layout_columnWeight="1"
            android:layout_rowWeight="1"
            android:layout_margin="4dp"
            android:text="%"
            android:background="#E0E0E0"/>
        
        <Button
            android:layout_width="0dp"
            android:layout_height="0dp"
            android:layout_columnWeight="1"
            android:layout_rowWeight="1"
            android:layout_margin="4dp"
            android:text="√"
            android:background="#E0E0E0"/>
        
        <!-- Строка 2: 7 8 9 / -->
        <Button
            android:layout_width="0dp"
            android:layout_height="0dp"
            android:layout_columnWeight="1"
            android:layout_rowWeight="1"
            android:layout_margin="4dp"
            android:text="7"
            android:textSize="24sp"/>
        
        <Button
            android:layout_width="0dp"
            android:layout_height="0dp"
            android:layout_columnWeight="1"
            android:layout_rowWeight="1"
            android:layout_margin="4dp"
            android:text="8"
            android:textSize="24sp"/>
        
        <Button
            android:layout_width="0dp"
            android:layout_height="0dp"
            android:layout_columnWeight="1"
            android:layout_rowWeight="1"
            android:layout_margin="4dp"
            android:text="9"
            android:textSize="24sp"/>
        
        <Button
            android:layout_width="0dp"
            android:layout_height="0dp"
            android:layout_columnWeight="1"
            android:layout_rowWeight="1"
            android:layout_margin="4dp"
            android:text="/"
            android:textSize="24sp"
            android:background="#FF9800"/>
        
        <!-- Строка 3: 4 5 6 * -->
        <Button
            android:layout_width="0dp"
            android:layout_height="0dp"
            android:layout_columnWeight="1"
            android:layout_rowWeight="1"
            android:layout_margin="4dp"
            android:text="4"
            android:textSize="24sp"/>
        
        <Button
            android:layout_width="0dp"
            android:layout_height="0dp"
            android:layout_columnWeight="1"
            android:layout_rowWeight="1"
            android:layout_margin="4dp"
            android:text="5"
            android:textSize="24sp"/>
        
        <Button
            android:layout_width="0dp"
            android:layout_height="0dp"
            android:layout_columnWeight="1"
            android:layout_rowWeight="1"
            android:layout_margin="4dp"
            android:text="6"
            android:textSize="24sp"/>
        
        <Button
            android:layout_width="0dp"
            android:layout_height="0dp"
            android:layout_columnWeight="1"
            android:layout_rowWeight="1"
            android:layout_margin="4dp"
            android:text="*"
            android:textSize="24sp"
            android:background="#FF9800"/>
        
        <!-- Строка 4: 1 2 3 - -->
        <Button
            android:layout_width="0dp"
            android:layout_height="0dp"
            android:layout_columnWeight="1"
            android:layout_rowWeight="1"
            android:layout_margin="4dp"
            android:text="1"
            android:textSize="24sp"/>
        
        <Button
            android:layout_width="0dp"
            android:layout_height="0dp"
            android:layout_columnWeight="1"
            android:layout_rowWeight="1"
            android:layout_margin="4dp"
            android:text="2"
            android:textSize="24sp"/>
        
        <Button
            android:layout_width="0dp"
            android:layout_height="0dp"
            android:layout_columnWeight="1"
            android:layout_rowWeight="1"
            android:layout_margin="4dp"
            android:text="3"
            android:textSize="24sp"/>
        
        <Button
            android:layout_width="0dp"
            android:layout_height="0dp"
            android:layout_columnWeight="1"
            android:layout_rowWeight="1"
            android:layout_margin="4dp"
            android:text="-"
            android:textSize="24sp"
            android:background="#FF9800"/>
        
        <!-- Строка 5: 0 00 . + -->
        <Button
            android:layout_width="0dp"
            android:layout_height="0dp"
            android:layout_columnWeight="1"
            android:layout_rowWeight="1"
            android:layout_margin="4dp"
            android:text="0"
            android:textSize="24sp"/>
        
        <Button
            android:layout_width="0dp"
            android:layout_height="0dp"
            android:layout_columnWeight="1"
            android:layout_rowWeight="1"
            android:layout_margin="4dp"
            android:text="00"
            android:textSize="24sp"/>
        
        <Button
            android:layout_width="0dp"
            android:layout_height="0dp"
            android:layout_columnWeight="1"
            android:layout_rowWeight="1"
            android:layout_margin="4dp"
            android:text="."
            android:textSize="24sp"/>
        
        <Button
            android:layout_width="0dp"
            android:layout_height="0dp"
            android:layout_columnWeight="1"
            android:layout_rowWeight="1"
            android:layout_margin="4dp"
            android:text="+"
            android:textSize="24sp"
            android:background="#FF9800"/>
        
        <!-- Строка 6: = (занимает 2 колонки) -->
        <Button
            android:layout_width="0dp"
            android:layout_height="0dp"
            android:layout_columnWeight="2"
            android:layout_rowWeight="1"
            android:layout_margin="4dp"
            android:text="="
            android:textSize="24sp"
            android:background="#4CAF50"
            android:layout_columnSpan="2"/>
        
        <Button
            android:layout_width="0dp"
            android:layout_height="0dp"
            android:layout_columnWeight="1"
            android:layout_rowWeight="1"
            android:layout_margin="4dp"
            android:layout_gravity="fill"/>
        
    </GridLayout>
    
</LinearLayout>
```

<img width="412" height="686" alt="Снимок экрана 2026-03-26 154658" src="https://github.com/user-attachments/assets/c6f78d44-53db-43cf-a444-d7f0c51264be" />

# Контрольные вопросы
1. Что такое XML? Для каких целей он используется в Android-разработке? 
XMl - это расширяемый язык разметки, предназначенный для храрения и передачи структурированных данных.

В Android-разработке XML используется для: 
 Создания пользовательского интерфейса
 Определения ресурсво
 Создания меню 
 Настройки анимаций 
 Конфигурация приложения 
 Создания drawable-ресурсов 

2. Что такое тег(элемент) в XML? Из каких частей он состоит?
   Тег - это основная структурная единица XML-документа.
   Части тега:
   Открывающий тег: <TextView
   Атрибуты: android:layout_width="match_parent"
   Содержимое: текст или вложенные элементы
   Закрывающий тег: </TextView

3. Какие менеджеры размещения (контейнеры) вы знаете? Кратко опишите каждый.
   LinearLayout - распологает элементы в один ряд (вертикально или горизонтально). Использует android:orientation и android:layout_weight

   RelativeLayout - распологает элементы относительно друг друга или родителя. Позволяет создавать сложные экраны с минимальной вложенностью.

   ConstrainLayout - гибкий контейнер с ограничениями. Современный стандарт, плоская иерархия, высокая производительность.

   GirdLayout - располагает элементы в виде таблицы. Позволяет объединять ячейки, подходит для калькуляторов.

4. В чем разница между LinearLayout и GirdLayout? В каких случаях какой контейнер удобне использовать?
   LinearLayout распологается в одну линию, требует вложенныех контейнеров для сетки, объединение ячеек не поддерживается, производительность хуже при глубокой вложенности.
   GirdLayout распологается в виде сетки, один контейнер для всей сетки, объединения ячеек поддерживается, производительность лучше при сетчатой структуре.

   Когда использовать:
   LinearLayout: простые списки, формы, панели инструментов, последовательное расположение.
   GirdLayout: калькуляторы, галереи, таблицы, игровые поля, клавиатуры.

5. Что такое match_parent и wrap_content? Приведите примеры использования.
   Это описание. match_parent занимает все доступное пространство родительского контейнера. wrap_content занимает только сктолько места, сколько необходимо для содержимого.
   Примеры:
   ```java
 
<Button
    android:layout_width="match_parent"
    android:layout_height="wrap_content"
    android:text="Нажми меня"/>


<TextView
    android:layout_width="wrap_content"
    android:layout_height="wrap_content"
    android:text="Короткий текст"/>


<LinearLayout
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"/>
    ```
6. В чем разницы между android:gravity и android:layout_gravity?
android:gravity - внутреннеее выравнивание содержимого текста, выравнивает дочерние жлементы внутри контейнера.
android:layout_gravity - внешнее выравнивание элемента в родителе, выравнивает элемент относительно родительского контейнера.

7. Какие единицы измерения используются в Android? Для чего предназначен dp и sp?
   dp - независимые от плотности экрана пиксели. Используется для размеров элементов, отступов, полей.
   sp - масштабируемые пиксели. Используется только для размера шрифтов.

8. Как создать простую фигуру (прямоугольрик, круг) с помощью XML-ресурса в папке drawable?
   Прямоугольник:
   
   ```java
  <?xml version="1.0" encoding="utf-8"?>
<shape xmlns:android="http://schemas.android.com/apk/res/android"
    android:shape="rectangle">
    
    <solid android:color="#FF5722"/>                   
    <corners android:radius="8dp"/>                     
    <stroke                                         
        android:width="2dp"
        android:color="#000000"/>
    <padding                                        
        android:left="10dp"
        android:top="10dp"
        android:right="10dp"
        android:bottom="10dp"/>
    
</shape>
```

Круг: 
```java
<?xml version="1.0" encoding="utf-8"?>
<shape xmlns:android="http://schemas.android.com/apk/res/android"
    android:shape="oval">
    
    <solid android:color="#4CAF50"/>                   
    <size                                            
        android:width="100dp"
        android:height="100dp"/>
    <stroke                                      
        android:width="3dp"
        android:color="#FFFFFF"/>
    
</shape>
```







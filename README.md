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

2. Нарисуйте н аэкране композицию, представленную на Рисунке 8 из исходного документа. Используйте View с установленным android:background для цветных блоков.

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












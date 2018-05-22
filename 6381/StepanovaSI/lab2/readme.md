•	В абстрактном классе Shape объявлены только те элементы, которые присущи абсолютно всем фигурам: цвет (Colour), идентификационный номер (ID), угол поворота (Angle); а так же реализованы методы для работы с этими данными: поворот на заданный угол (Rotation), установка цвета (setColour) и получение цвета (getColour). Чисто виртуальными методами объявлены: масштабирование (Scaling) и перемещение в указанные координаты (Movement). Они будут переопределены в классах наследниках.

•	В классах-наследниках от абстрактного класса Shape – Parallelogram и Ellipse переопределены виртуальные функции базового класса, а так же был перегружен оператор вывода в поток. В классе Parallelogram добавлены такие поля как: координаты центра (X0 и Y0),  длина первой диагонали (D1), длина второй диагонали (D2), угол между диагоналями (AngleBetweenDiagonal). Это позволяет однозначным образом задать фигуру. В классе Ellipse, помимо координат центра, добавлены так же длины большего и меньшего радиусов (R1 и R2). 

•	Класс SectorEllipse является наследником класса Parallelogram т.к. они имеют одинаковую реализацию основных методов. Для «вырезания» сектора из эллипса в класс добавлены поля Angle1 и Angle2, которые отвечают за угол между осью OX и первой стороной сектора и за угол между осью OX и второй стороной сектора.

•	Метод Rotation выполняет поворот фигуры на заданный пользователем угол. На вход функция получает значение угла (в градусах) типа double которое присваивается полю класса Angle. После этого проводится проверка на то, что угол лежит за пределами промежутка [0,360): если это так, то значение приводится к аналогичному из промежутка. 

•	Метод Movement выполняет перемещение фигуры в заданные пользователем координаты. Для фигур из данного варианта реализация схожа: у эллипса и параллелограмма есть центр. Его координаты хранятся в полях класса X0 и Y0.  Эти координаты изменяются на соответствующие координаты точки, в которую необходимо перенести фигуру.

•	Метод Scaling масштабирует фигуру на заданный коэффициент. Как и предыдущий метод, для фигур из данного варианта его реализация схожа: заданный пользователем коэффициент проверяется на то, что он меньше либо равен 0 (фигуры не могут иметь отрицательные стороны). Если это так, то масштабирования не происходит. Иначе, происходит масштабирование: радиусы эллипса и диагонали параллелограмма умножаются на заданный коэффициент. 

•	Методы setColour и getColour соответственно устанавливают и получают поле класса Colour.

•	Оператор вывода в поток перегружен таким образом, чтобы выводилась вся основная информация о фигуре.

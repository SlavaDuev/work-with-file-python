Справочник по работе с файлами при помощи pandas:

1. Чтение файла: 
   - Используйте функцию read_csv() для чтения файла CSV.
   - Используйте функцию read_excel() для чтения файла Excel.
   Пример:

   import pandas as pd
   data = pd.read_csv('file.csv')  # Чтение файла CSV
   data = pd.read_excel('file.xlsx')  # Чтение файла Excel

2. Запись данных в файл:
   - Используйте функцию to_csv() для записи данных в файл CSV.
   - Используйте функцию to_excel() для записи данных в файл Excel.
   Пример:

   data.to_csv('new_file.csv', index=False)  # Запись данных в файл CSV
   data.to_excel('new_file.xlsx', index=False)  # Запись данных в файл Excel

3. Получение информации о файле:
   - Используйте атрибут shape, чтобы узнать размерность данных.
   - Используйте функцию info(), чтобы получить общую информацию о данных (типы данных, количество ненулевых значений, использование памяти и др.).
   Пример:

   print(data.shape)  # Размерность данных (количество строк и столбцов)
   data.info()  # Общая информация о данных

4. Просмотр данных:
   - Используйте функцию head() или tail(), чтобы просмотреть первые или последние строки данных.
   Пример:

   data.head()  # Просмотр первых строк данных
   data.tail()  # Просмотр последних строк данных

5. Копирование данных из одного файла в другой:
   - Пользователь должен ввести номер строки, которую необходимо перенести из одного файла в другой.
   - Используйте функцию iloc[] для доступа к определенной строке и копируйте ее в новый DataFrame.
   - Запишите новый DataFrame в файл.
   Пример:

   row_number = int(input("Введите номер строки: "))  # Ввод номера строки пользователем
   data2 = data1.iloc[row_number]  # Копирование строки в новый DataFrame
   data2.to_csv('new_file.csv', index=False)  # Запись нового DataFrame в файл

   Можно расширить функциональность, например, добавить обработку ошибок и проверку введенного номера строки на валидность, но данный пример демонстрирует общий подход к переносу данных из одного файла в другой.

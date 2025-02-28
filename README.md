## Обзор

Данный проект реализует алгоритм поиска строк в текстовом файле, где каждая строка содержит три поля, представленных в табличном виде. Задача алгоритма – отфильтровать строки по заданному шаблону поиска и вывести результаты двух вариантов обработки в отдельные файлы, включая замер затраченного времени.

---

## Описание задачи

Каждая строка входного файла имеет формат:

```
пасспорт ФИО адрес проживания
```

**Пример строки:**

```
5432 343564 Комаров Даниил Иванович г. Владивосток, ул. Карбышева д. 52
```

Пользователь вводит поисковый запрос (например, `"ул. Карбышева"`). Алгоритм осуществляет поиск по строкам входного файла и возвращает те строки, где встречается заданный шаблон.

---

## Входные данные

1. **Текстовый файл.**  
   - Каждая строка файла содержит три поля:
     - Первое поле – паспорт.
     - Второе поле – ФИО.
     - Третье поле – адрес проживания.
   - Поля должны соответствовать типам данных в предметной области. Все числовые данные хранятся в виде числовых значений (например, время – это структура из двух целочисленных полей).  
   - Количество строк файла: **1 000 000**.

2. **Целое число `n`.**  
   - Задает количество строк входного файла, подлежащих обработке.  
   - Ограничения: **10 ≤ n ≤ 1 000 000**.

3. **Параметры поиска для каждого поля:**
   - **Шаблон поиска** (или список шаблонов, если алгоритм предусматривает множественный поиск).
   - **Количество вхождений.**  
     Определяет, сколько раз заданный шаблон (или сколько из заданных шаблонов) должно встречаться в соответствующем поле.

---

## Выходные данные

Алгоритм генерирует **два** текстовых файла:

- **Файл 1:** Результаты поиска, выполненного первым алгоритмом.
- **Файл 2:** Результаты поиска, выполненного вторым алгоритмом.

**Формат каждой строки в файлах:**

- Номер строки исходного файла.
- Данные строки из входного файла, удовлетворяющие условиям поиска.

Последняя строка каждого файла содержит информацию о времени, затраченном на выполнение поиска. Все данные в выходном файле должны быть представлены в табличном виде.

---

## Пример использования

**Входная строка для поиска:**  
```
ул. Карбышева
```

**Ожидаемый результат:**  
Алгоритм находит и выводит все строки, содержащие подстроку `"ул. Карбышева"`, вместе с их номерами и данными.

---

## Технические детали

- **Язык реализации:** [указать язык программирования/технологию]
- **Производительность:**  
  Алгоритм рассчитан на обработку файлов объемом до 1 000 000 строк.
- **Тестирование:**  
  Все входные данные считаются корректными, дополнительная проверка не производится.
- **Замер времени:**  
  В конце результатов поиска указывается время выполнения алгоритма, что позволяет оценить эффективность реализации.

---

## Заключение

Проект нацелен на эффективный поиск информации в больших объемах данных, используя современные алгоритмы обработки текстовых файлов. Это решение позволяет быстро фильтровать данные по заданным условиям и представляет результаты в удобном табличном формате.
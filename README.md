Урок 9. Работа с табличными данными

**Читаем библиотеку**

df = pd.read_csv('california_housing_train.csv')

**Задача 40: Работать с файлом california_housing_train.csv, который находится в папке sample_data. Определить среднюю стоимость дома, где кол-во людей от 0 до 500 (population).**

mean = df.loc[df['population']<500]['median_house_value'].mean()

print(f'Cредняя стоимость дома: {mean}')

**Задача 42: Узнать какая максимальная households в зоне минимального значения population.**

print(f'Максимальная households в зоне минимального значения population: {df.describe().min().households}')

**Ответы:**

40_ Cредняя стоимость дома: 206683.83635227982

42_ Максимальная households в зоне минимального значения population: 1.0
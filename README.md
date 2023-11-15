<a id='ENG'></a>
<a href="#RUS"><img src='https://img.shields.io/badge/ENG -Go to RUS description-blue'></a>

 # Analyzing and predicting customer churn in telecom company

### Project objective
To research and develop a machine learning model to predict customer churn in order to retain them with special offers.

### Data
Personal data about customers, their tariffs and contracts from 4 sources:

- `contract_new.csv` - contract information valid as of February 1, 2020
- `personal_new.csv` - customer's personal 
- `internet_new.csv` - information about internet services
- `phone_new.csv` - information about telephony services.

### Skills and tools
`Exploratory Data Analysis`  ·  `Python` · `Pandas` · `SciPy` · `Seaborn` · `Clustering` `KMeans` · `Shap`  
`Scikit-learn` · `LogisticRegression` · `RandomForest` · `CatBoost`

### Results
The result of the EDA was **a portrait of the exiting customer**:
- Service tenure 1 - 4.7 years
- Relatively high monthly fees monthly_charges
- Customer prefers to use advanced technologies and comfortable service:
- Fiber Optic internet connection internet_service
     - package of services at once, most critical 7-9 services at once number_services
     - cashless_billing
     - automatic debit from bank account or credit card paymen_method
     - contract with annual payment types type
- Personal characteristics: married, has dependents, retired, any gender.

CatBoostClassifier gradient binning with StandardScaler, OrdinalEncoder data preprocessing is selected as the best model for prediction. Test results:
- ROC-AUC = 0.93
- Error in prediction of positive class (client will exit) - 20% and negative (client will stay) - 9%.

<br>
<br>


<a id='RUS'></a>
<a href="#ENG"><img src='https://img.shields.io/badge/RUS -Go to ENG description-blue'></a>

# Анализ и прогнозирование оттока клиентов в телеком-компании
 
### Задача проекта
Провести исследование и разработать модель машинного обучения для предсказания ухода пользователя с целью его удержания специальными предложениями.

### Данные  
Персональные данные о клиентах, их тарифах и договорах из 4-х источников:  
- `contract_new.csv` — информация о договорах, актуальна на 1 февраля 2020
- `personal_new.csv` — персональные данные клиента
- `internet_new.csv` — информация об интернет-услугах
- `phone_new.csv` — информация об услугах телефонии.

### Навыки и инструменты
`Exploratory Data Analysis` ·  `Python`  ·  `Pandas` ·  `SciPy`  ·  `Seaborn`  ·  `Clustering`  `KMeans`  ·  `Shap`  
`Scikit-learn` ·  `LogisticRegression`  ·  `RandomForest`  ·  `CatBoost`  

### Результаты проекта
Результатом EDA стал **портрет ушедшего клиента**:
- Срок обслуживания `tenure` 1 - 4.7 лет
- Относительно высокая ежемесячная плата `monthly_charges`
- Клиент предпочитает использовать передовые технологии и комфортное обслуживание:
    - интернет-подключение Fiber Optic `internet_service`
    - сразу пакет услуг, наиболее критично 7-9 услуг сразу `number_services`
    - безналичная оплата `paperless_billing`
    - автоматическое списание с банковского счёта или кредитной карты `paymen_method`
    - контракт с годовыми типами оплаты `type`
- Персональные характеристики: состоит в браке, имеет иждивенцев, пенсионер, любого пола.

В качестве лучшей модели для предсказания выбран градиентный бустинг **CatBoostClassifier** с предобработкой данных StandardScaler, OrdinalEncoder. Результаты тестирования:
- ROC-AUC = 0.93 
- Ошибка в предсказании положительного класса (клиент уйдёт) - 20% и отрицательного (клиент останется) - 9%.


<h1 >Проект по автоматизации тестирования API сервиса <a href="https://petstore.swagger.io/#/"> Petstore</a></h1>

# :man_student:: Содержание:

- <a href="#tools"> Стек используемых технологий</a>
- <a href="#checking"> Реализованные проверки</a>
- <a href="#jenkins"> Сборка в Jenkins</a>
- <a href="#console"> Запуск тестов из терминала</a>
- <a href="#allureReport"> Allure отчет</a>
- <a href="#allure"> Интеграция с Allure TestOps</a>
- <a href="#tg"> Уведомления в Telegram с использованием бота</a>

<a id="tools"></a>
## 🧰: Стек используемых технологий

<p align="center">
<a href="https://www.jetbrains.com/idea/"><img src="media/logo/Idea.svg" width="50" height="50"  alt="IDEA"/></a>
<a href="https://rest-assured.io/"><img src="media/logo/RestAssured.png" width="50" height="50"  alt="Rest-Assured"/></a>
<a href="https://www.java.com/"><img src="media/logo/Java.svg" width="50" height="50"  alt="Java"/></a>
<a href="https://github.com/"><img src="media/logo/GitHub.svg" width="50" height="50"  alt="Github"/></a>
<a href="https://junit.org/junit5/"><img src="media/logo/JUnit5.svg" width="50" height="50"  alt="JUnit 5"/></a>
<a href="https://gradle.org/"><img src="media/logo/Gradle.svg" width="50" height="50"  alt="Gradle"/></a>
<a href="https://github.com/allure-framework/allure2"><img src="media/logo/Allure.svg" width="50" height="50"  alt="Allure"/></a>
<a href="https://https://qameta.io/"><img src="media/logo/AllureTestOps.svg" width="50" height="50"  alt="AllureTestOps"/></a>
<a href="https://www.jenkins.io/"><img src="media/logo/Jenkins.svg" width="50" height="50"  alt="Jenkins"/></a>
<a href="https://https://telegram.org/"><img src="media/logo/Telegram.svg" width="50" height="50"  alt="Telegram"/></a>
</p>

<a id="checking"></a>
## :male_detective:: Реализованные проверки

- ✓ Проверка создания нового животного в магазине
- ✓ Проверка чтения существующего животного в магазине
- ✓ Проверка удаления существующего животного из магазина
- ✓ Проверка ошибки при удалении несуществующего животного из магазина
- ✓ Проверка ошибки при чтении несуществующего животного в магазине

<a id="jenkins"></a>
## <img src="media/logo/Jenkins.svg" width="25" height="25"  alt="Jenkins"/></a> Сборка в <a target="_blank" href="https://jenkins.autotests.cloud/job/QA.GURU_PetstoreProject/"> Jenkins </a>
<p align="center">
<a href="https://jenkins.autotests.cloud/job/QA.GURU_PetstoreProject/allure/"><img src="media/screens/Petstore_jenkins.png" alt="Jenkins1"/></a>
</p>
После выполнения сборки, в блоке <code>История сборок</code> напротив номера сборки появятся значки <code>Allure Report</code> и <code>Allure TestOps</code>, при клике на которые откроется страница с сформированным html-отчетом и тестовой документацией соответственно.


## 🧪: Пример авто-тест кейса
<p align="center">
<img title="AllureSuite" src="media/screens/Petstore_alluretc.png">
</p>

<a id="console"></a>
## :rocket:: Запуск тестов из терминала
Команда запуска тестов:
```
gradle clean test
```


<a id="allureReport"></a>
## <img width="4%" style="vertical-align:middle" title="Allure Report" src="media/logo/Allure.svg"> </a> Пример <a target="_blank" href="https://jenkins.autotests.cloud/job/QA.GURU_PetstoreProject/allure/"> Allure-отчета </a>
## ⛅: Основной отчет

<p align="center">
<img title="Allure Overview" src="media/screens/Petstore_allurereport.png">
</p>

<a id="allure"></a>
## <img src="media/logo/AllureTestOps.svg" width="25" height="25"  alt="Allure_TO"/></a> Интеграция с  <a target="_blank" href="https://allure.autotests.cloud/project/3730/dashboards"> Allure TestOps</a>

## :bar_chart:: Доска
На *Dashboard* в <code>Allure TestOps</code> видна статистика количества тестов. Новые тесты, а так же результаты прогона приходят по интеграции при каждом запуске сборки.

<p align="center">
<img title="Allure TestOps DashBoard" src="media/screens/Petstore_dashboard.png">
</p>

## :pinching_hand:: Пример тест-кейса
<p align="center">
<img title="AllureTC" src="media/screens/Petstore_testcase.png">
</p>

## :runner:: Прогоны
<p align="center">
<img title="Allure Tests" src="media/screens/Petstore_launches.png">
</p>

<a id="tg"></a>
## <img src="media/logo/Telegram.svg" width="25" height="25"  alt="Telegram"/></a> Уведомления в телеграм с использованием бота
После завершения сборки специальный бот, созданный в <code>Telegram</code>, автоматически обрабатывает и отправляет сообщение с отчетом о прогоне тестов.

<p align="center">
<img title="telegram" src="media/screens/Petstore_telegram.png">
</p>
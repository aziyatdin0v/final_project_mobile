# <img width="5%" title="Wikipedia" src="images/logo/Wikipedia.svg"> Дипломный проект по тестирования мобильного приложения [Wikipedia](https://github.com/wikimedia/apps-android-wikipedia/)

## :open_book: Содержание:

- [Технологии и инструменты](#technologist-технологии-и-инструменты)
- [Тест кейсы](#bookmark_tabs-тест-кейсы)
- [Запуск тестов из терминала](#computer-запуск-тестов-из-терминала)
- [Запуск тестов в Jenkins](#-запуск-тестов-в-jenkins)
- [Отчет о результатах тестирования в Allure Report](#-отчет-о-результатах-тестирования-в-Allure-report)
- [Интеграция с Allure TestOps](#-интеграция-с-allure-testops)
- [Уведомления в Telegram](#-уведомления-в-telegram-с)
- [Пример запуска теста в Browserstack](#-пример-запуска-теста-в-Browserstack)

## :gear: Технологии и инструменты

<p align="left">
<a href="https://www.jetbrains.com/idea/"><img src="images/logo/Intelij_IDEA.svg" width="50" height="50"  alt="IDEA" title="IntelliJ IDEA"/></a>
<a href="https://www.java.com/"><img src="images/logo/Java.svg" width="50" height="50" alt="Java" title="Java"/></a>
<a href="https://gradle.org/"><img src="images/logo/Gradle.svg" width="50" height="50" alt="Gradle" title="Gradle"/></a>
<a href="https://junit.org/junit5/"><img src="images/logo/JUnit5.svg" width="50" height="50" alt="JUnit 5" title="JUnit 5"/></a>
<a href="https://github.com/"><img src="images/logo/GitHub.svg" width="50" height="50" alt="Github" title="GitHub"/></a>
<a href="https://developer.android.com/"><img src="images/logo/Android-studio.svg" width="50" height="50" alt="Android-studio" title="Android-studio"/></a>
<a href="https://appium.io/"><img src="images/logo/Appium.svg" width="50" height="50" alt="Appium" title="Appium"/></a>
<a href="https://www.browserstack.com/"><img src="images/logo/Browserstack.svg" width="50" height="50" alt="Browserstack" title="Browserstack"/></a>
<a href="https://github.com/allure-framework/allure2"><img src="images/logo/Allure_Report.svg" width="50" height="50" alt="Allure" title="Allure"/></a>
<a href="https://qameta.io/"><img src="images/logo/Allure_TO.svg" width="50" height="50" alt="Allure_TO" title="Allure_TO"></a>
<a href="https://www.jenkins.io/"><img src="images/logo/Jenkins.svg" width="50" height="50" alt="Jenkins" title="Jenkins"/></a>
<a href="https://web.telegram.org/"><img src="images/logo/Telegram.svg" width="50" height="50" alt="Telegram" title="Telegram"></a>
</p>

## :bookmark_tabs: Тест кейсы:

- Проверка поиска в приложении
- Проверка прохождения начального экрана
- Проверка добавления нового языка в настройках приложения

## :computer: Запуск тестов из терминала

### Удаленный запуск тестов

```bash
gradle clean test -DdeviceHost=browserstack
```

### Локальный запуск тестов

```bash
gradle clean test-DdeviceHost=local
```

## <img width="4%" title="Jenkins" src="images/logo/Jenkins.svg"> Запуск тестов в [Jenkins](https://jenkins.autotests.cloud/)

Для запуска сборки необходимо перейти в раздел <code><strong>*Собрать с параметрами*</strong></code> и нажать кнопку <code><strong>*Собрать*</strong></code>.

<p align="center">
  <img src="images/screen/start_jenkins.png" alt="Jenkins" width="800">
</p>

После выполнения сборки, в блоке <code><strong>*История сборок*</strong></code> напротив номера сборки появится
значок *Allure Report*, кликнув по которому, откроется страница с сформированным html-отчетом.

## <img width="4%" title="Allure Report" src="images/logo/Allure_Report.svg"> Отчет о результатах тестирования в [Allure Report](https://jenkins.autotests.cloud/)

<p align="center">
  <img src="images/screen/jenkins_overview.png" alt="allure-report" width="900">
</p>

<p align="center">
  <img src="images/screen/jenkins_behaviors.png" alt="allure-report_1" width="900">
</p>

## <img width="4%" title="Allure TestOPS" src="images/logo/Allure_TO.svg"> Интеграция с [Allure TestOps](https://allure.autotests.cloud/launch/18294)

### Основной дашборд

<p align="center">
  <img src="images/screen/dashboards.png" alt="dashboard" width="900">
</p>

### Список тестов с результатами прогона

<p align="center">
  <img src="images/screen/allure-testops-results.png" alt="dashboard" width="900">
</p>

## <img width="4%" title="Telegram" src="images/logo/Telegram.svg"> Уведомления в Telegram с использованием бота
После завершения сборки специальный бот, созданный в <code>Telegram</code>, автоматически обрабатывает и отправляет сообщение с отчетом о прогоне тестов.

<p align="center">
<img title="Telegram Notifications" src="images/screenshot/Telegram.png">

## <img width="4%" title="Selenoid" src="images/logo/Browserstack.svg"> Пример запуска теста в Browserstack

К каждому тесту в отчете прилагается видео.

На данном видео выполняется:

- Проверка добавления нового языка в настройках приложения


<p align="center">
  <img title="Browserstack Video" src="images/video/mobile_test.gif">
</p>
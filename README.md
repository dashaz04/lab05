### Задание
1. Создайте `CMakeList.txt` для библиотеки *banking*.
[CMakeLists.txt](banking/CMakeLists.txt)
2. Создайте модульные тесты на классы `Transaction` и `Account`.
    * Используйте mock-объекты.
    * Покрытие кода должно составлять 100%.
[test.cpp](tests/test.cpp)
3. Настройте сборочную процедуру на **GitHub Actions**.
[file](.github/workflows/cicd.yml)
4. Настройте [Coveralls.io](https://coveralls.io/).
[![Coverage Status](https://coveralls.io/repos/github/dashaz04/lab05/badge.svg?branch=main)](https://coveralls.io/github/dashaz04/lab05?branch=main)

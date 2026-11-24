cmake_minimum_required(VERSION 3.14)
project(SimpleCIProject)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

# Основной исполняемый файл
add_executable(app src/main.cpp src/m_utils.cpp)

# Включаем тестирование
enable_testing()

# Исполняемый файл с тестами
add_executable(unit_tests tests/tests.cpp src/m_utils.cpp)

# Регистрируем тест в CTest
add_test(NAME MathUnitTests COMMAND unit_tests)

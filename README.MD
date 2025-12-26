# RU and EN README



## RU: Описание проекта



Данный репозиторий содержит реализацию методики динамической идентификации аппаратной части персонального компьютера (ПК) на основе измерения скорости выполнения кода. Метод основан на оригинальной работе Iskander Sanchez-Rola под названием "Clock Around the Clock: Time-Based Device Fingerprinting", опубликованной в 2018 году.



Цель проекта заключается в разработке алгоритма, позволяющего создавать уникальный идентификатор (HWID) на основе матрицы времени выполнения специально подобранных фрагментов кода. Такой подход позволяет избежать прямой привязки к каким-либо аппаратным характеристикам ПК, что затрудняет обнаружение и обход системы идентификации.



Проект включает серию экспериментов и практических реализаций с целью оценки эффективности предложенного метода и улучшения стабильности результатов.



---



## Особенности реализации



### Первая версия



Первоначально была разработана простая версия алгоритма, использующая встроенный инструмент \*\*RandBytes()\*\* для измерения скорости выполнения. Несмотря на положительные результаты, стабильность оказалась недостаточной, что подтолкнуло к дальнейшим изысканиям.



### Вторая версия



Во второй попытке были учтены рекомендации оригинального автора и применены дополнительные меры оптимизации:



- Измерение времени выполнения кода с помощью высокочастотных таймеров (HPET, ACPI) и низкоуровневых методов доступа к процессору.

- Улучшенная обработка шума и артефактов измерений благодаря нормализации и фильтрации результатов.

- Увеличение количества замеров для уменьшения эффекта случайных отклонений.



Тем не менее, несмотря на улучшение стабильности, проблема полной надежности решения осталась нерешенной.



---



## Результаты исследований



Проведённые эксперименты показали следующее:



- Матрица времени выполнения действительно отражает уникальные характеристики конкретного ПК.

- На стабильность результатов влияют внешние условия, такие как нагрузка на систему и состояние центрального процессора.

- Полностью устранить влияние указанных факторов пока не удалось, хотя достигнут значительный прогресс в улучшении качества полученных данных.



---



## Рекомендации по улучшению



Рекомендуется продолжить разработку с учетом выявленных проблем и предложить новые подходы к решению следующих вопросов:



- Устойчивость к изменению рабочей нагрузки системы.

- Возможность адаптации алгоритмов к различным конфигурациям железа и операционных систем.

- Оптимизация работы с разными видами таймеров (например, выбор наилучшего сочетания аппаратных и программных таймеров).



---













## EN: Project Description



This repository contains an implementation of a technique for dynamically identifying the hardware of a personal computer (PC) based on measuring the speed of code execution. The method is based on the original work by Iskander Sanchez-Rola titled "Clock Around the Clock: Time-Based Device Fingerprinting", published in 2018.



The goal of the project is to develop an algorithm that allows you to create a unique identifier (HWID) based on the execution time matrix of specially selected code fragments. This approach avoids direct reference to any hardware characteristics of the PC, which makes it difficult to detect and bypass the identification system.



The project includes a series of experiments and practical implementations in order to evaluate the effectiveness of the proposed method and improve the stability of the results.



---



## Implementation features



### The first version



Initially, a simple version of the algorithm was developed using the built-in \*\*RandBytes()\*\* tool to measure execution speed. Despite the positive results, stability proved to be insufficient, which prompted further research.



### The second version



In the second attempt, the recommendations of the original author were taken into account and additional optimization measures were applied.:



- Measurement of code execution time using high-frequency timers (HPET, ACPI) and low-level processor access methods.

- Improved processing of noise and measurement artifacts due to normalization and filtering of results.

- Increase the number of measurements to reduce the effect of random deviations.



Nevertheless, despite the improved stability, the problem of complete reliability of the solution remained unresolved.



---



## Research results



The experiments have shown the following:



- The run-time matrix really reflects the unique characteristics of a particular PC.

- The stability of the results is affected by external conditions, such as the load on the system and the state of the CPU.

- It has not yet been possible to completely eliminate the influence of these factors, although significant progress has been made in improving the quality of the data obtained.



---



## Recommendations for improvement



It is recommended to continue the development taking into account the identified problems and propose new approaches to solving the following issues:



- Resistance to changes in the workload of the system.

- The ability to adapt algorithms to different hardware configurations and operating systems.

- Optimization of working with different types of timers (for example, choosing the best combination of hardware and software timers).



---

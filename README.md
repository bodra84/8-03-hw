# Домашнее задание к занятию «GitLab» - Файзиев Давлат.

### Задание 1

**Что нужно сделать:**

1. Разверните GitLab локально, используя Vagrantfile и инструкцию, описанные в [этом репозитории](https://github.com/netology-code/sdvps-materials/tree/main/gitlab).   
2. Создайте новый проект и пустой репозиторий в нём.
3. Зарегистрируйте gitlab-runner для этого проекта и запустите его в режиме Docker. Раннер можно регистрировать и запускать на той же виртуальной машине, на которой запущен GitLab.

В качестве ответа в репозиторий шаблона с решением добавьте скриншоты с настройками раннера в проекте.

---

### Решение 1
 
Cкриншоты с настройками раннера:
 
![Скриншот 1](https://github.com/bodra84/8-03-hw/blob/main/img/1_1.png)
  
![Скриншот 2](https://github.com/bodra84/8-03-hw/blob/main/img/1_2.png)

---

### Задание 2

**Что нужно сделать:**

1. Запушьте [репозиторий](https://github.com/netology-code/sdvps-materials/tree/main/gitlab) на GitLab, изменив origin. Это изучалось на занятии по Git.
2. Создайте .gitlab-ci.yml, описав в нём все необходимые, на ваш взгляд, этапы.

В качестве ответа в шаблон с решением добавьте: 
 
 * файл gitlab-ci.yml для своего проекта или вставьте код в соответствующее поле в шаблоне; 
 * скриншоты с успешно собранными сборками.
 
---
### Решение 2

Листинг кода из файла gitlab-ci.yml:
```
stages:
  - test
  - build

test:
  stage: test
  image: golang:1.17
  script:
   - go test .

build:
  stage: build
  image: docker:latest
  script:
   - docker build .
```
  
Cкриншот  с успешно собранными сборками:

![Скриншот 3](https://github.com/bodra84/8-03-hw/blob/main/img/2_1.png)
![Скриншот 4](https://github.com/bodra84/8-03-hw/blob/main/img/2_2.png)

---

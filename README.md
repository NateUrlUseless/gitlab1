# Задание 1
Здравствуйте, предлагаю вашему вниманию скриншоты с установленным GitLab где находится созданный мной пустой репозито>

![Скриншот 1](https://github.com/NateUrlUseless/gitlab1/blob/main/1.png)
![Скриншот 2](https://github.com/NateUrlUseless/gitlab1/blob/main/2.png)
![Скриншот 3](https://github.com/NateUrlUseless/gitlab1/blob/main/5.png)
Так же представляю настройки doker-runner
```
docker run --rm -v /srv/gitlab-runner/config:/etc/gitlab-runner gitlab/gitlab-runner register \
  --non-interactive \
  --executor "docker" \
  --docker-image alpine:latest \
  --url "https://nate.gitlab.com/" \
  --registration-token "sK1aBJnfSK8zhqBPE8ut" \
  --description "docker-runner" \
  --maintenance-note "gitlab" \
  --tag-list "docker" \
  --run-untagged="true" \
  --locked="false" \
  --access-level="not_protected"
```

# Задание 2

Тут я запушил представленный репозиторий в котором я изменил origin(название origin).
В этом задание репозиторий немного отличается так как я уже делал форк из предыдущего задания, в discord мне ответили что такое допускается.
![Скриншот 4](https://github.com/NateUrlUseless/gitlab1/blob/main/3.png)
![Скриншот 5](https://github.com/NateUrlUseless/gitlab1/blob/main/4.png)

.gitlab-ci.yml:

```
default:
  tags:
    - dmosk

stages:
  - test

test:
  stage: test
  script: echo $CI_PROJECT_DIR/
```

Тут мы создаем pipeline с одним единственным этапом, которое называется test. По данному заданию будет запускаться сккрипт вывода значения переменной $CI_PROJECT_DIR — путь, по которому клонируется проект и где выполняется задание.


Спасибо за внимание! При ответе на это задание, пожалуйста, дайте свою оценку оформлению данного ответа на задание.
Может быть, я смогу как то улучшить его? Зарание спасибо!

# Лабораторная работа 5

Функция 1: 
Автоматизация проверки формата .txt файлов   
* Создайте bash-скрипт pre-commit (с расширением .sh, если нужно) для проверки формата .txt файлов.  
* В Windows используйте Git Bash или аналог, чтобы разместить этот скрипт в .git/hooks и назвать его pre-commit (без расширения).
* Убедитесь, что скрипт имеет права на выполнение (под Windows в Git Bash выполните chmod +x .git/hooks/pre-commit).  
* В скрипте реализуйте логику проверки наличия нужного текста (например, подписи автора).  

Пример содержимого файла pre-commit:
```bash
#!/bin/bash
for file in $(git diff --cached --name-only); do
  if [[ $file == *.txt ]]; then
    if ! grep -q "Author:" "$file"; then
      echo "Файл $file не содержит подписи автора!"
      exit 1
    fi
  fi
done
exit 0
```
### Функция 2: 
Работа с Git Flow 
* Убедитесь, что Git Flow установлен (под Windows может потребоваться отдельная установка или использование git flow через Git Bash).
* В корне репозитория выполните инициализацию Git Flow:  
git flow init
* Начните фичу для новой функциональности:
git flow feature start task-management
* Внесите нужные изменения (например, создайте функцию в task_manager.py), закоммитьте их.
* Завершите фичу:  
git flow feature finish task-management
* Начните релиз (из ветки develop):  
git flow release start v1.0.0
* Обновите версию, закоммитьте изменения, завершите релиз:  
git flow release finish v1.0.0
* Для экстренных исправлений создавайте hotfix-ветки:  
git flow hotfix start hotfix-1.0.1
После исправлений закоммитьте и завершите hotfix:  
git flow hotfix finish hotfix-1.0.1
* тправьте итоговые изменения в удаленный репозиторий:  
git push origin develop
git push origin main

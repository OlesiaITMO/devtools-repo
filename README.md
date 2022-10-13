# DevTools Repo

Настраиваем GitFlow:

1. `git checkout -b develop` - основная ветка разработки;
2. `git checkout -b feature` - ветка с фичей;
3. Сделали файл `main.py` и закоммитили (`git add main.py`, `git commit`);
4. `git checkout develop`, `git merge feature` - переключаемся в основную ветку и вливаем туда ветку с фичей;
5. `git checkout -b release` - релизная ветка, которая делается от основной;
6. Поправили ошибку в `main.py` и закоммитили (`git add main.py`, `git commit`);
7. Вливаем релизную ветку в `develop` (`git checkout develop`, `git merge release`);
8. Вливаем релизную ветку в `main` (`git checkout main`, `git merge release`) и помечаем новую версию тегом (`git tag 'v0.1.0'`);
9. Делаем ветку с хотфиксом файла `main.py` (`git checkout -b hotfix`), делаем его и коммитим (`git add main.py`, `git commit`);
10. Вливаем хотфикс в `develop` (`git checkout develop`, `git merge hotfix`);
11. Вливаем хотфикс в `main` (`git checkout main`, `git merge hotfix`) и помечаем новую версию тегом (`git tag 'v0.1.1'`);
12. Закидываем изменённую историю на GitHub (`git push -u origin --all`, `git push -u origin --tags`).
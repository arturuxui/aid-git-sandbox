# Упражнения

Учебный репозиторий к гайду [Git for Beginners](https://github.com/arturuxui/aid-git-guide).
Здесь можно ошибаться: ничего не выкатывается, ломать не страшно.

Каждое упражнение — к своей главе. Делай руками в GitHub или проси Claude — как в гайде.
Отметка «готово» — твоя: поставь `[x]` в этом файле в одном из своих PR.

Где «коллега» — его играет Claude: попроси «сыграй коллегу в упражнении N».

---

## 1. Ветка и коммит — главы [2](https://github.com/arturuxui/aid-git-guide/blob/main/content/ru/02-commit.md), [3](https://github.com/arturuxui/aid-git-guide/blob/main/content/ru/03-branches.md)

- [ ] Создай ветку `ex1-button-padding` от свежего `main`.
- [ ] В `button.css` поменяй `padding: 12px 16px` на `padding: 12px 20px`.
- [ ] Посмотри, что изменилось («покажи diff»), и закоммить с понятным сообщением.

*Готово, когда:* в ветке есть коммит с сообщением вида «Кнопка: …», `main` не изменился.

## 2. Push и Pull Request — главы [4](https://github.com/arturuxui/aid-git-guide/blob/main/content/ru/04-remote.md), [5](https://github.com/arturuxui/aid-git-guide/blob/main/content/ru/05-pull-request.md)

- [ ] Запушь ветку из упражнения 1.
- [ ] Открой PR в `main` через **Compare & pull request**: название, описание «что и зачем».
- [ ] Пройди вкладки PR: **Conversation**, **Commits**, **Checks**, **Files changed**.

*Готово, когда:* PR открыт, base — `main`, проверки зелёные.

## 3. Ревью — глава [5](https://github.com/arturuxui/aid-git-guide/blob/main/content/ru/05-pull-request.md)

- [ ] Попроси Claude-коллегу оставить замечание к строке в твоём PR.
- [ ] Поправь по замечанию коммитом **в ту же ветку**, ответь на комментарий, **Resolve conversation**.

*Готово, когда:* в PR новый коммит, обсуждение закрыто, нового PR ты не открывал.

## 4. Красный CI — глава [7](https://github.com/arturuxui/aid-git-guide/blob/main/content/ru/07-ci.md)

- [ ] В том же PR поменяй в `button.css` цвет фона на `#7B61FF`, закоммить и запушь.
- [ ] Дождись ❌ у проверки **Цвета**, открой **Details** и найди, что она пишет.
- [ ] Почини: верни `var(--bg-accent-main)` (или попроси Claude «CI красный — разберись»).

*Готово, когда:* ты видел красную проверку и сам довёл её до зелёной.

## 5. Merge — глава [6](https://github.com/arturuxui/aid-git-guide/blob/main/content/ru/06-merge.md)

- [ ] Слей PR через **Squash and merge**, удали ветку (**Delete branch**).
- [ ] Вернись на свежий `main` у себя («переключись на свежий `main`»).
- [ ] Посмотри историю `main`: один коммит на весь PR.

*Готово, когда:* изменения в `main`, ветки нет ни на GitHub, ни у тебя.

## 6. Конфликт — главы [6](https://github.com/arturuxui/aid-git-guide/blob/main/content/ru/06-merge.md), [8](https://github.com/arturuxui/aid-git-guide/blob/main/content/ru/08-teamwork.md)

- [ ] Ветка `ex6-card-padding`: в `card.css` поменяй `padding: 16px` на `padding: 24px`, запушь, открой PR.
- [ ] Попроси Claude-коллегу поменять ту же строку на `padding: 20px` и слить его PR первым.
- [ ] В своём PR — «This branch has conflicts»: **Resolve conflicts**, выбери значение, удали маркеры,
      **Mark as resolved** → **Commit merge**.
- [ ] Дождись зелёных проверок (проверка **Конфликты** поймает забытые маркеры) и слей.

*Готово, когда:* конфликт решён тобой на сайте, PR слит, маркеров в `main` нет.

## 7. Отстал от `main` — глава [8](https://github.com/arturuxui/aid-git-guide/blob/main/content/ru/08-teamwork.md)

- [ ] Открой PR с правкой `gap` в `card.css`.
- [ ] Попроси Claude-коллегу слить в `main` правку другого файла (`button.css`).
- [ ] В своём PR нажми **Update branch**, дождись проверок, слей.

*Готово, когда:* ты обновил ветку кнопкой, конфликта не было, PR слит.

---

Дальше — по желанию.

## 8. Отменить слитое — глава [11](https://github.com/arturuxui/aid-git-guide/blob/main/content/ru/11-oops.md)

- [ ] На странице любого слитого PR нажми **Revert**, слей созданный PR.

*Готово, когда:* в `main` есть revert-коммит, а изменения того PR отменены.

## 9. Релиз — глава [9](https://github.com/arturuxui/aid-git-guide/blob/main/content/ru/09-releases.md)

- [ ] **Releases** → **Draft a new release** → тег `v0.1.0` на `main` → **Generate release notes** → **Publish release**.

*Готово, когда:* на странице репозитория виден релиз `v0.1.0`.

## 10. Issue — глава [10](https://github.com/arturuxui/aid-git-guide/blob/main/content/ru/10-issues.md)

- [ ] Открой issue «Карточка: отступ по сетке 8», сделай PR с `Closes #<номер>` и слей.

*Готово, когда:* issue закрылась сама со ссылкой на PR.

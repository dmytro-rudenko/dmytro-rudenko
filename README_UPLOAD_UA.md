# Як опублікувати GitHub Profile README

## 1. Створи профільний репозиторій

1. Відкрий [github.com/new](https://github.com/new).
2. Назви репозиторій **`dmytro-rudenko`** — точно так само, як твій GitHub username.
3. Вибери **Public** і створи репозиторій. Це спеціальний репозиторій: його `README.md` GitHub покаже у верхній частині профілю.

## 2. Додай файли

Скопіюй у новий репозиторій файли з цього набору, не змінюючи структуру:

```text
README.md
.github/workflows/snake.yml
```

Якщо робиш це через термінал, у папці з завантаженими файлами виконай:

```bash
git clone https://github.com/dmytro-rudenko/dmytro-rudenko.git
cp README.md dmytro-rudenko/
mkdir -p dmytro-rudenko/.github/workflows
cp .github/workflows/snake.yml dmytro-rudenko/.github/workflows/
cd dmytro-rudenko
git add README.md .github/workflows/snake.yml
git commit -m "Add profile README"
git push
```

Або завантаж файли через GitHub: у репозиторії натисни **Add file → Upload files**. Для `snake.yml` спочатку створи файл через **Add file → Create new file** з назвою `.github/workflows/snake.yml`, встав його вміст і натисни **Commit changes**.

## 3. Увімкни змійку

1. Відкрий вкладку **Actions** у профільному репозиторії.
2. Якщо GitHub попросить підтвердити запуск workflow — натисни **I understand my workflows, go ahead and enable them**.
3. Відкрий workflow **Generate contribution snake** і натисни **Run workflow → Run workflow**.

Після завершення з’явиться гілка `output` із двома SVG-файлами. README вже посилається на них; оновлення запускатиметься щодня. Якщо основна гілка твого нового репозиторію називається `master`, у `snake.yml` заміни `main` на `master`.

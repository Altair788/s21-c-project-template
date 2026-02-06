# S21 C Project Template  
**TDD-ready**

## Быстрый старт

```bash
# 1. Клонируй шаблон
git clone git@github.com:Altair788/s21-c-project-template.git my_project
cd my_project

# 2. Тестируй (работает из коробки!)
cd src
make test
# Running suite(s): helpers | 100%: Checks: 6, Failures: 0

# 3. Разработка (TDD цикл)
make clean && make && make test

# 4. Coverage report
make gcov_report
open report/coverage_report.details.html

---

## Создание своего проекта из шаблона

```bash
# В ~/my_new_project
mkdir your_project_name
cd your_project_name

git clone git@github.com:Altair788/s21-c-project-template.git temp
rsync -av --exclude='.git' temp/ ./
rm -rf temp
find . -name ".git" -type d -exec rm -rf {} + 2>/dev/null || true
rm -rf .git
git init
git remote add origin git@github.com:YOUR_USERNAME/my_new_project.git
git branch -M main
git add . && git commit -m "Initial project"
git push -u origin main
git remote -v  # Проверка привязки к репо на GitHub
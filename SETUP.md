# Настройка репозитория

## Git

```bash
git config --global user.name "Карчевский Лев Олегович"
git config --global user.email "ваш_email@example.com"
git config --global init.defaultBranch main
```

## Основной workflow

```bash
git switch -c feature/my-change
git add .
git commit -m "feat: describe change"
git push -u origin feature/my-change
```

После этого создайте Pull Request в `main`, дождитесь Code Review и выполните merge через GitHub.

## Versioned hook

```bash
mkdir -p .git/hooks
cp .githooks/commit-msg .git/hooks/commit-msg
chmod +x .git/hooks/commit-msg
```

## Полезные операции из практической работы №3

```bash
git remote add gitlab git@gitlab.com:USERNAME/devops-mirror.git
git push gitlab --all
git push gitlab --tags
git cherry-pick COMMIT_HASH
git reflog
git revert HEAD
git rebase -i HEAD~6
```


# Github事始め

##　Git操作
### ヘルプ
- すべてのgitガイド: `git help -g`
- gitで利用できるすべてのコマンド一覧を表示する: `git help -a`
- gitで利用できるすべてのコマンド一覧をページで表示する: `git --paginate help -a`
- gitの用語集を表示する: `git help glossary`
- gitヘルプのヘルプ: `git help help`

### SETUP
- ユーザー名を設定する: `git config --global user.name "{ユーザー名}"`
- メールアドレスを設定する: `git config --global user.email "{メールアドレス}"`
- デフォルトのエディタを設定する: `git config --global core.editor "{エディタ名}"`
- カラー表示を有効にする: `git config --global color.ui true`
- pullするときに、rebaseするかmergeするかを設定する: `git config --global pull.rebase true`
- git configの設定値一覧を表示する: `git config --list`

### SETUP&INIT
- カレントディレクトリをGitリポジドリとして初期化する: `git init`
- リモートリポジドリからクローンする: `git clone {リモートリポジドリURL}`

### STAGE&SNAPSHOT
- カレントディレクトリの状態を表示する: `git status`
- 変更したファイルをステージングする: `git add {ファイル名}`
- 変更したすべてのファイルをステージングする: `git add .`
- 変更した箇所をステージングする: `git add -p`
- ステージングするときに、なにが実行されるかを表示する: `git add --dry-run .`
- 差分を表示する: `git diff`
- ステージングエリアとリモートリポジドリ間で差分があれば表示する: `git diff --staged`
- 指定したコミット間の差分を表示する: `git diff {コミットID1} {コミットID2}`
- 各行の変更を表示する: `git blame {ファイル名}`
- ステージングしたファイルをコミットする: `git commit -m "{なんらかのコミットメッセージ}"`
- ステージング不要で、すべての変更をコミットする: `git commit -a`
- 直前のコミットを修正する: `git commit --amend`

### BRANCH&MERGE
- ローカルに存在するブランチの一覧を表示する: `git branch`
- 新しいブランチを作成する: `git branch {ブランチ名}`
- ブランチを削除する: `git branch -d {ブランチ名}`
- 指定したブランチに切り替える: `git switch {ブランチ名}`
- 新しいブランチを作成して、そのブランチに切り替える: `git switch -c {ブランチ名}`
- ~~ 新しいブランチを作成して、そのブランチに切り替える: `git checkout -b {ブランチ名}` ~~
- 指定したブランチを現在のブランチにマージする: `git merge {ブランチ名}`
- マージコミットを作成して、履歴を残す: `git merge --no-ff {ブランチ名}`

### INSPECT&COMPARE
- コミット履歴を表示する: `git log`
- コミット履歴を1行で表示する: `git log --oneline`
- コミット履歴をグラフで表示する: `git log --graph`
- すべてのブランチのコミット履歴をグラフで表示する: `git log --graph --oneline --decorate --all`
- gitのオブジェクトを人間が読める形で表示する: `git show {SHA}`

### TRACKING PATH CHANGES
- ステージングエリアからファイルを削除する: `git rm {ファイル名}`
- ファイルパスを変更する: `git mv {旧パス} {新パス}`

### IGNORING PATTERNS
- すべてのローカルリポジトリに対して無視する: `git config --global core.excludesfile {ファイル名}`

### SHARE&UPDATE
- リモートリポジドリの一覧を表示する: `git remote`
- リモートリポジドリから変更を取得する: `git fetch {リモート名} {ブランチ名}`
- リモートリポジドリを追加する: `git remote add {リモート名} {リモートURL}`
- リモートリポジドリを削除する: `git remote remove {リモート名}`
- ローカルのブランチをリモートリポジドリにプッシュする: `git push {リモート名} {ブランチ名}`
- リモートリポジドリのブランチを削除する: `git push {リモート名} --delete {ブランチ名}`
- リモートリポジドリから変更を取得してマージする: `git pull {リモート名} {ブランチ名}`
- タグの一覧を表示する: `git tag`
- 新しいタグを作成する: `git tag {タグ名}`
- 指定したコミットにタグを作成する: `git tag {タグ名} {コミットID}`
- アノテーションタグを作成する: `git tag -a {タグ名} -m "{メッセージ}"`

### REWRITE HISTORY
- 指定したブランチを現在のブランチにリベースする: `git rebase {ブランチ名}`
- インタラクティブリベースを実施する: `git rebase -i {コミットID}`
- ステージングエリアをリセットして、ファイルをコミット予定から外す: `git reset {ファイル名}`

### TEMPRARY COMMITS
- 変更を一時的に退避する: `git stash`
- 退避した変更の一覧を表示する: `git stash list`
- 最後に退避した変更を復元する: `git stash pop`
- 指定したコミットを現在のブランチに取り込む: `git cherry-pick {コミットID}`

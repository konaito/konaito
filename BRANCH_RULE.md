# FYBE ブランチルール

このドキュメントは、FYBE（[https://fybe.jp](https://fybe.jp)）での開発を円滑に進めるためのガイドラインです。**mainブランチを中心にシンプルかつ柔軟な開発フロー**を実現し、一貫性のあるコラボレーションを目指します。

---

## 1. 基本方針

- **mainブランチ**  
  `main` ブランチは、全ての作業の集約地点として使用します。  
  **developブランチは使用せず**、`main` ブランチに対して直接作業を進めます。

---

## 2. feature ブランチの運用

- **mainからfeatureブランチを作成**し、タスクを進めます。
- ブランチ名には**操作タイプ（`add` / `fix`）**を明示し、以下のフォーマットで命名してください：

  ```
  {ニックネーム}/{プロジェクト名}/{操作タイプ}-{作業タイトル}
  ```

- 目的：この形式により、**ブランチ名から作業者を一目で把握**でき、管理が容易になります。  
- **issueベースでブランチを作成する際**にも、この命名規則を厳守してください。

### 例
```bash
# 新しいフロントエンドのナビゲーションを追加する場合
git switch -c konaito/frontend/add-header-navigation

# バグ修正用のブランチを作成する場合
git switch -c konaito/backend/fix-login-bug
```

---

## 3. コミットメッセージについて

- コミットメッセージは、開発者の判断で適当な内容でも構いません。  
- 例えば、**ブランチ名をそのままコミットメッセージに使用**するような自動化もOKです。

### 自動化の例（オプション）

```bash
alias gk="git commit -m \"\$(git symbolic-ref --short HEAD)\""
```

---

## 4. プルリクエストの運用

- 各featureブランチでの作業が完了したら、**自分でプルリクエスト（PR）を作成**してください。  
- **レビューの必要なく、自分でマージ**しても構いません。
- **ブランチとプルリクエストは削除せず**、履歴として残してください。

---

## 5. ニックネームとGitHubアカウント

各開発者は、以下のようにニックネームを定義し、GitHubアカウントを紐付けます。

- **最初の作業**として、ニックネームを定義するためのブランチを作成し、READMEを改変・更新してください。その後、**プルリクエストを通してマージ**します。

```bash
git switch -c {ニックネーム}/readme/fix-define-nickname
```

### FYBEの開発者一覧

- **konaito**: [https://github.com/konaito](https://github.com/konaito)

---

このREADMEに基づき、効率的かつ一貫性のある開発を行いましょう。質問や不明点がある場合は、GitHub上で各メンバーにお問い合わせください。

---

konaito

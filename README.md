# Claude Code プロジェクトテンプレート

このテンプレートは、Claude Codeを使用したプロジェクト開発において、言語・フレームワークに依存しない基本的な設定ファイルを提供します。

## 📋 含まれるファイル

### Claude Code専用設定
- `CLAUDE.md` - プロジェクト固有の指示書テンプレート
- `.claude.json` - MCP servers基本設定
- `.claude/settings.local.json` - ローカル設定サンプル

### バージョン管理
- `.gitignore` - 汎用的な除外設定
- `.gitattributes` - Git属性設定（改行コード、バイナリファイル識別）

### エディタ・開発環境
- `.editorconfig` - エディタ設定統一

### その他
- `.env.example` - 環境変数サンプル
- `.github/workflows/claude-code.yml` - GitHub Actions基本設定

## 🚀 使い方

1. このテンプレートを新しいプロジェクトにコピー
2. `CLAUDE.md` を編集してプロジェクト固有の情報を記載
3. `.claude.json` でMCPサーバーの設定を調整
4. `.env.example` を参考に環境変数を設定
5. プロジェクトに応じて他の設定ファイルを追加

## 📝 カスタマイズ例

### プロジェクトタイプ別の追加設定

#### Node.js/TypeScript プロジェクト
```bash
# 追加で必要なファイル
package.json
tsconfig.json
eslint.config.js
.prettierrc
```

#### Python プロジェクト
```bash
# 追加で必要なファイル
requirements.txt
pyproject.toml
.flake8
```

#### Go プロジェクト
```bash
# 追加で必要なファイル
go.mod
go.sum
```

## 🔧 Claude Code設定

### MCP Servers
デフォルトで以下のMCPサーバーが設定されています：
- `filesystem` - ファイルシステム操作
- `git` - Git操作
- `time` - 時間関連機能

### カスタムMCPサーバーの追加
`.claude.json` に新しいサーバーを追加できます：

```json
{
  "mcpServers": {
    "your-server": {
      "command": "npx",
      "args": ["-y", "your-mcp-server"],
      "env": {
        "API_KEY": "your-api-key"
      }
    }
  }
}
```

## 📚 CLAUDE.mdの書き方

`CLAUDE.md` には以下の情報を記載してください：

1. プロジェクトの概要と目的
2. 使用している技術スタック
3. プロジェクト構造
4. コーディング規約
5. 重要な制約事項
6. 開発フロー
7. よく使うコマンド

## 🤝 貢献

改善提案や新しい設定ファイルの追加は、Issueまたはプルリクエストでお知らせください。

## 📄 ライセンス

このプロジェクトは MIT ライセンスの下で公開されています。

## 🙏 謝辞

このテンプレートは、日本のエンジニアコミュニティのベストプラクティスを参考に作成されました。

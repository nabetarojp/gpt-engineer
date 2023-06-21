# GPT Engineer

[![Discord Follow](https://dcbadge.vercel.app/api/server/4t5vXHhu?style=flat)](https://discord.gg/4t5vXHhu)
[![GitHub Repo stars](https://img.shields.io/github/stars/AntonOsika/gpt-engineer?style=social)](https://github.com/AntonOsika/gpt-engineer)
[![Twitter Follow](https://img.shields.io/twitter/follow/antonosika?style=social)](https://twitter.com/AntonOsika)

\*\*何を作って欲しいかを指定すると、AI が説明を求めて、それを作ってくれます。

GPT Engineer は、適応、拡張が容易で、あなたのコードがどのように見えるかをエージェントに学習させることができるように作られています。プロンプトに基づきコードベース全体を生成します。

[Demo](https://twitter.com/antonosika/status/1667641038104674306) 👶🤖

## Project philosophy

- シンプルに価値を得ることができる
- 柔軟で簡単に独自の "AI ステップ "を追加できる。`steps.py`を参照してください。
- 以下のようなユーザーエクスペリエンスを目指して、段階的に構築していきます：
  1. 高レベルのプロンプト
  2. AI が時間をかけて記憶するようなフィードバックを与える。
- AI と人間の間を素早く行き来できる。
- すべての計算は「再開可能」であり、ファイルシステムに永続化される。

## Usage

**stable**または**development**のいずれかを選択してください。

For **stable** release:

- `pip install gpt-engineer`

For **development**:

- `git clone git@github.com:AntonOsika/gpt-engineer.git`
- `cd gpt-engineer`
- `make install`
- `source venv/bin/activate`

**Setup**

GPT4 アクセスランを持つ api キーで：

- `export OPENAI_API_KEY=[your api key]`

**Run**:

- Create an empty folder. If inside the repo, you can run:
  - `cp -r projects/example/ projects/my-new-project`
- Fill in the `main_prompt` file in your new folder
- Run: `gpt-engineer projects/my-new-project`

**Results**

- Check the generated files in `projects/my-new-project/workspace`

## Features

`identity`フォルダのファイルを編集することで、AI エージェントの「アイデンティティ」を指定することができます。

アイデンティティを編集し、`main_prompt`を進化させることは、現在、プロジェクト間でエージェントに物事を覚えさせる方法です。

`steps.py` の各ステップは GPT4 との通信履歴が logs フォルダに保存され、 `scripts/rerun_edited_message_logs.py` で再実行することが可能です。

## Contributing

私たちは、開発者がいじくりまわして、個人的なコード生成ツールボックスを構築するためのオープンプラットフォームを構築しています。

If you want to contribute, please check out the [roadmap](https://github.com/AntonOsika/gpt-engineer/blob/main/ROADMAP.md), [projects](https://github.com/AntonOsika/gpt-engineer/projects?query=is%3Aopen) or [issues tab](https://github.com/AntonOsika/gpt-engineer/issues) in the GitHub repo. You are welcome to read the [contributing document](.github/CONTRIBUTING.md) and join our [Discord 💬](https://discord.gg/4t5vXHhu).

We are currently looking for more maintainers and community organisers. Email anton.osika@gmail.com if you are interested in an official role.

## Example

https://github.com/AntonOsika/gpt-engineer/assets/4467025/6e362e45-4a94-4b0d-973d-393a31d92d9b

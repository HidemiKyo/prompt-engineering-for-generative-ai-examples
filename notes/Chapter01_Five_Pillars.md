# Chapter 1: プロンプトの5つの原則

## 🔑 Key Concepts
- 方向性を示す
- 出力形式を指定する
- 例を示す
- 品質を評価する
- タスクを分割する

## 💡 Insights
- 方向性を示す
    - 背景情報（context）
        - 誰に向けた、何のための、どんな雰囲気で
    - Role Prompting
        - ex. スティーブ・ジョブズの命名スタイルでブレインストーミングしてください
    - PrewarmingまたはInternal Retrieval（内部検索）
        - モデルに「何を期待されているか」を理解させるために、前置きのプロンプトを使って“ウォームアップ”させる
    - タスクに対する助言をコンテキストとして挿入（プロンプト長増大によりコストが増える）
    - 方向性が少なすぎるとサンプル不足で生成できず、多すぎると創造性が狭まる
- 出力形式指定
    - ソフトウェアに組み込む際には、形式の指定と形式の誤りを確認する仕組み（ex.JSONパーサー）が必要
     - [structured-outputs](https://platform.openai.com/docs/guides/structured-outputs) で出力形式をJSONに固定可能
- 例を示す
    - 例はモデルの出力精度に大きく影響
    - 例の数が多いと精度が上がる
    - 信頼性と創造性はトレードオフ
- 品質を評価する
    - 同じプロンプトを複数回試すことで、出力のばらつきや安定性を確認できる
    - [OpenAI Evals](https://github.com/openai/evals)という、LLMやそれを活用したシステムの性能を評価するためのフレームワークがある
        - 出力の精度、プロンプトの有効性、AIモデル間の比較などが検証可能
- 複雑な指示を段階的に処理させると、AIが混乱せず、各ステップでFBを反映しやすくなる

## 🧪 実験メモ
- GPT-4で「Dividing Labor」を試したプロンプト例と結果

## 📚 参考リンク
- [教材ノートブック](https://github.com/BrightPool/prompt-engineering-for-generative-ai-examples/tree/main/content)


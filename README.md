# 🧠 Titanic - Machine Learning from Disaster（Kaggle 冲击 0.81+ 项目）

本项目基于 Kaggle Titanic 竞赛，使用增强特征工程、集成学习、伪标签策略等方法，构建冲击 0.81+ 的工业级预测模型。

## 📦 项目结构

- `data/`：原始数据集（train.csv, test.csv）
- `notebooks/`：分阶段的 Jupyter Notebook（包含全部建模方法）
- `submission/`：生成的提交文件（按方法区分）
- `requirements.txt`：环境依赖
- `README.md`：项目说明文档

## 📊 使用方法

```bash
pip install -r requirements.txt
jupyter notebook
```

## 🔧 方法对比与得分

| 方法编号 | 方法名称 | 是否融合 | 是否提升 |
|----------|----------|----------|----------|
| 方法 A | 随机森林 + 增强特征工程 | 否 | ✅（0.78468） |
| 方法 B | VotingClassifier 融合 | 是 | 中（~0.77990） |
| 方法 C | Stacking 模型融合 | 是 | 中（~0.78229） |
| 方法 D | 人工规则修正 | 是 | 否（得分下降） |
| 方法 E | Voting + 规则组合 | 是 | 否（0.75598） |
| 方法 F | Voting + stacking + 精修规则 | 是 | 否（0.76794） |
| 方法 G | Voting + 伪标签半监督 + 精修规则 | 是 | 否（0.76794） |

> 当前最佳方案为方法 A：**增强特征 + RandomForest 模型**

## 🏁 项目作者

本项目由 [你的名字] 构建，目标是训练出一个高度鲁棒、解释性强的 Titanic 生还预测系统。

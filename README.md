# 🚢 Titanic - Machine Learning from Disaster（Kaggle 0.81+ 精细建模项目）

本项目基于 Kaggle 经典入门竞赛《Titanic》，目标是预测泰坦尼克号乘客是否生还。  
通过系统构建特征工程 + 模型融合 + 半监督学习等模块，冲击排行榜高分（最高得分：**0.78468**）。

---

## 📌 项目亮点

- 📦 **增强型特征工程**（姓氏/家庭/船舱/票号等高阶特征构造）
- 🧠 **集成学习融合模型**（RandomForest、XGBoost、LightGBM、Stacking）
- 🔁 **半监督学习伪标签**（伪标签样本反向补强训练集）
- 🛠️ **人工规则修正机制**（针对弱模型误判人群定向优化）
- 📊 多策略得分对比（冲击 0.81 的精细路线图）

---

## 🏆 模型方法对比分数表

| 方法编号 | 方法名称 | 是否融合 | 得分 | 提升效果 |
|----------|-----------|-----------|--------|-----------|
| 方法 A | 随机森林 + 增强特征 | 否 | ✅ **0.78468** | ⭐ 当前最佳 |
| 方法 B | VotingClassifier 融合 | 是 | ~0.77990 | 中 |
| 方法 C | Stacking 模型融合 | 是 | ~0.78229 | 中 |
| 方法 D | 人工规则修正 | 是 | ~0.75598 | ❌ |
| 方法 E | Voting + 精修规则组合 | 是 | ~0.76794 | ❌ |
| 方法 F | Voting + 伪标签增强 | 是 | ~0.76794 | ❌ |

---

## 📁 项目结构
titanic-kaggle/
│
├── data/               # 原始数据（train/test）
├── notebooks/          # Jupyter 分阶段 Notebook
│   └── 0.81+_副本.ipynb
├── submission/         # 提交文件（含最佳方案）
├── requirements.txt    # 依赖包列表
└── README.md           # 项目说明

---

## 🚀 快速开始

```bash
git clone https://github.com/Lin93555/titanic-kaggle.git
cd titanic-kaggle
pip install -r requirements.txt
jupyter notebook

---

📎 推荐阅读顺序
	1.	notebooks/0.81+_副本.ipynb → 主体代码与策略清晰记录
	2.	submission/submission_final_ensemble_boosted.csv → 各方法输出文件
	3.	README.md → 方法总览 + 冲分路径图

---

🙋‍♂️ 作者

	本项目由 Lin93555 构建
如果你觉得有帮助，请点击 ⭐ Star 支持一下！

---

📫 联系与交流

如需交流建模策略、Kaggle 学习方法、入门路径，欢迎联系我或发 Issue 👇

---


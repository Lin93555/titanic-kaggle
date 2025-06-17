# NYC Taxi Trip Duration – LightGBM Baseline

![Python](https://img.shields.io/badge/Python-3.8%2B-blue?logo=python) ![LightGBM](https://img.shields.io/badge/LightGBM-3.x-success)

> 🚕 Kaggle「New York City Taxi Trip Duration」比赛的简洁 baseline：  
> *纯 Python + LightGBM* —— 带中文注释，适合从 0 到 1 学习回归建模流程

---

## 📂 仓库结构
```
├── nyc_taxi_lgbm_cn.py      # 主脚本（含中文注释）
├── submission.csv           # 运行脚本后自动生成
├── lgb_model.pkl            # 训练完保存的最佳模型
├── titanic-kaggle/          # 原有 Titanic 文件夹（保留）
└── README.md
```

---

## ✨ 脚本特点
| 模块 | 说明 |
|------|------|
| 数据清洗 | 剔除 > 1 h 长尾订单 |
| 特征工程 | 时间拆分（小时 / 星期 / 月 / 周末 / 高峰）<br>经纬差 → 公里，欧几里得 & 曼哈顿距离 |
| 验证方式 | **TimeSeriesSplit** 5 折，验证集是真正“未来” |
| 模型 | LightGBM 回归 + early-stopping |
| 输出 | `submission.csv` + `lgb_model.pkl` |

---

## 🖥️ 环境依赖
```bash
pip install pandas numpy scikit-learn lightgbm joblib
```

---

## 🚀 一键运行
```bash
# 确保 train.csv / test.csv 与脚本在同目录
python nyc_taxi_lgbm_cn.py
```

执行日志示例：
```
🔄 Fold 1 ... ✅ Fold 1 best RMSE = 0.41
🎯 交叉验证最优 RMSE = 0.40
📤 已保存 submission.csv
💾 已保存模型 lgb_model.pkl
```
将 `submission.csv` 上传 Kaggle，公榜 RMSLE ≈ **0.40–0.45**。

---

## 📊 进一步提升
| 改进方向 | 预期分数 |
|----------|---------|
| 加天气 / 区域聚类特征 | 0.36 ± |
| 模型融合（LGB + XGB + Catboost） | 0.33 ± |
| Optuna 全局调参 | 0.32 ± |

---

## 📜 参考
* Kaggle 竞赛主页：<https://www.kaggle.com/competitions/nyc-taxi-trip-duration>
* LightGBM 文档：<https://lightgbm.readthedocs.io/>

---

© 2024 Lin93555 — 仅供学习交流，禁止商用

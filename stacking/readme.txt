stacking集成算法

算法说明
1） 在原始特殊的基础上增加，每个grid以及每个grid每小时的最大值、最小值、标准差、偏度、峰度等统计值
2） 使用lightgbm、RandomForestRegressor、XGBRegressor、Ridge、LinearRegression、BaggingRegressor、GradientBoostingRegressor 7个模型，对所有数据分别训练、预测，将预测结果以及这些结果的差值作为新增的特征加到数据集中；
3） 再用lgb、xgb做训练、预测；
4） 融合lgb、xgb的预测结果做最后结果


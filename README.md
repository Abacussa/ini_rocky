# Crypto Transformer Trading System

一个基于 Transformer 深度学习模型的加密货币量化交易系统，集成多种技术指标分析和实时交易执行。

## 🚀 项目特色

- **多时间框架分析**: 支持 15分钟、1小时、4小时、日线等多周期数据
- **Transformer 模型**: 使用先进的 Transformer 架构进行价格预测
- **技术指标集成**: MACD、RSI、KDJ、布林带、均线等 60+ 技术指标
- **实盘交易支持**: 支持 Binance 交易所的实盘交易
- **多币种并行**: 可同时监控和交易多个加密货币对
- **风险控制**: 内置止损止盈、仓位管理机制

## 📊 支持交易对

- BTCUSDT, DOGEUSDT, BNBUSDT, XRPUSDT, SOLUSDT, ADAUSDT, UNIUSDT

## 🛠 技术架构

### 核心组件
- **数据获取**: CCXT 库获取实时市场数据
- **特征工程**: 68 维技术指标特征
- **深度学习**: PyTorch Transformer 模型
- **交易执行**: 多线程实时交易引擎
- **风险控制**: 动态止损止盈策略

### 技术栈
- Python 3.8+
- PyTorch
- Pandas, NumPy
- CCXT
- Scikit-learn
- mplfinance

## 📁 项目结构
1.主程序是：transformer_crypto_trading.py
  1)训练某个标的命令如下：
  python3 transformer_crypto_trading.py BTCUSDT 3 train
  2)实盘交易命令如下：
  python3 transformer_crypto_trading.py all 1 real
2.基础数据工程：common_eng.py，主要是各样指标的加工和计算
3.行情数据抓取工程：data_eng.py
4.特征加工工程：features_eng.py
5.交易工程：deal_eng.py
6.交易标的配置文件：products--transformer.txt


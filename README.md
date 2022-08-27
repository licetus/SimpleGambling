# SimpleGambling

## 本合约意在实现一个简单的赌博游戏，通过猜测BTC/USD价格小数点后第二位的单双来押注

### 详细规则说明：
1. 合约中所指的时间均为UTC时间，即格林尼治标准中时区时间
2. BTC/USD价格通过chainlink预言机实时获取
3. 开奖时间为UTC时间每小时整点，指每小时整点向chainlink发送请求获取实时价格，获取价格后会显示获取时的实际时间
4. 考虑到获取价格时间的延迟，兑付开始时间为每小时整点后10分
5. 投注时间为每小时的20分-50分，50分之后停止投注
6. 兑付奖金会扣除相应gas费用以及合约运行成本，所以会比理论值略低
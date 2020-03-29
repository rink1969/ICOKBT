# ICOKBT

IOT and CKB.  

Send transaction from an IOT device, pay for something. 

Then there will be a script to deal with clearing and settlement.

---

一个IOT设备与CKB交互的demo。

一个停车场可能是由场地业主，停车场系统供应商，可能还有资金提供方一起建设的。

停车收费之后，需要将收到的费用，按照事先约定的比例分发给所有参与方。

例如，一个停车场道闸设备。在有车出去的时候，识别车辆信息和收费信息。

然后发送交易到链上一个合约，直接以token的方式做清分。

### 相关项目

[ckb-cli for arm](https://github.com/rink1969/ckb-cli/tree/iot)

[ckb for aarch64](https://github.com/rink1969/ckb/tree/aarch64)

### 吐槽

1. ckb-cli基本把ckb都包含进来，编译ckb-cli比ckb还复杂。
2. Rust对glibc版本要求太高了。
3. 自动清分合约，好像在ckb实现不了？solidity可以在fallback函数里实现，有人向这个合约转账的时候，自动将金额分给另外几个账户。
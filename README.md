### 支付模块测试
安装支付SDK：
```
<dependency>
    <groupId>cn.hyperzhu</groupId>
    <artifactId>Payment_SDK</artifactId>
</dependency>
```

使用SDK:
```
public ResponseEntity<String> payNotify(
            @RequestParam String code,
            @RequestParam String timestamp,
            @RequestParam String mch_id,
            @RequestParam String order_no,
            @RequestParam String out_trade_no,
            @RequestParam String pay_no,
            @RequestParam String total_fee,
            @RequestParam String sign,
            @RequestParam String pay_channel,
            @RequestParam String trade_type,
            @RequestParam String success_time,
            @RequestParam String attach,
            @RequestParam String openid) {
        try {
            log.info("请求参数：{} {} {} {} {} {} {} {} {} {} {} {} {}",
                    code,
                    timestamp,
                    mch_id,
                    order_no,
                    out_trade_no,
                    pay_no,
                    total_fee,
                    sign,
                    pay_channel,
                    trade_type,
                    success_time,
                    attach, openid);

            return new ResponseEntity<>("SUCCESS", HttpStatus.OK);
        } catch (Exception e) {
            return new ResponseEntity<>("FAIL", HttpStatus.BAD_REQUEST);
        }
    }
```
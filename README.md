### 测试地址
https://bank-static-stg.pingan.com.cn/brac-ia/universal_h5/pages/accStatus/index.html?channel=XXX&source=XXX&outerSource=XXX&returnUrl=XXX&halfUrl=XXX&aladdin=X

### 生产环境地址
https://bank-static.pingan.com.cn/brac-ia/universal_h5/pages/accStatus/index.html?channel=XXX&source=XXX&outerSource=XXX&returnUrl=XXX&halfUrl=XXX&aladdin=XXX

### 打开页面方式：
	bow.navigator.forward({
		url: url
	)};

|参数   |描述   |必输   |备注   |
|-------|-------|-------|-------|
|channel   |渠道   |Y   |C0001 - 营业柜台   <br>C0002 - 网上银行   <br>C0003 - 口袋银行   <br>C0004 - 爱客   <br>C0005 - 橙E网   <br>C0006 - 智能投顾   <br>C0007 - 千人千面   <br>C0008 - 橙子银行   <br>C0009 - 口袋插件   <br>C0010 - 厅堂   <br>C0011 - 银保通   <br>C0012 - 新口袋银行   <br>C0013 - 聚合首   <br><br>如不是以上渠道，请联系刘权分配   |
|halfUrl   |终止流程返回地址   |N   |URL需要做encodeURIComponent()处理   <br>URL有白名单控制，在白名单内才允许跳转，非平安域名、bow域名的URL接入前请联系林秋桂（LINQIUGUI177）配置   <br>不传默认执行bow.navigator.back();   |
|returnUrl   |成功页返回地址   |N   |URL需要做encodeURIComponent()处理   <br>URL有白名单控制，在白名单内才允许跳转，非平安域名、bow域名的URL接入前请联系林秋桂（LINQIUGUI177）配置   <br>不传默认执行bow.navigator.back();   |
|source   |开户来源   |N   |请联系产品经理刘权（LIUQUAN281）确认数值   |
|outerSource   |二级开户来源   |N   |请联系产品经理刘权（LIUQUAN281）确认数值   |
|aladdin   |需要执行的aladdin方法   |N   |返回前执行监听事件aladdin.broadcast(value);   |
|secCardSign   |需要状态翻转的卡号加密串   |N   |默认取第一张二类户卡

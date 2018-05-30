---
layout:         post
title:          블로그 테스트
subtitle:       블로그 텍스트 테스트
card-image:     https://ww1.sinaimg.cn/mw690/906cb9dbgw1fayoxw9jh0j20b407e3zn.jpg
date:           2018-05-31 01:20:00
tags:           life
post-card-type: image
---

처음으로 github 블로그를 작성해본다.

## 테스트

소스코드 표시：

```
org.flowable.engine.common.api.FlowableException: Unknown property used in expression: ${hrTask.responseStatusCode == 200}
at org.flowable.engine.common.impl.el.JuelExpression.getValue(JuelExpression.java:50)
at org.flowable.engine.impl.el.UelExpressionCondition.evaluate(UelExpressionCondition.java:37)
at org.flowable.engine.impl.util.condition.ConditionUtil.hasTrueCondition(ConditionUtil.java:47)
...
Caused by: org.flowable.engine.common.impl.javax.el.PropertyNotFoundException: Cannot resolve identifier 'hrTask'
at org.flowable.engine.common.impl.de.odysseus.el.tree.impl.ast.AstIdentifier.eval(AstIdentifier.java:97)
at org.flowable.engine.common.impl.de.odysseus.el.tree.impl.ast.AstProperty.eval(AstProperty.java:68)
at org.flowable.engine.common.impl.de.odysseus.el.tree.impl.ast.AstBinary$SimpleOperator.eval(AstBinary.java:31)
...
```

## 이렇게도 쓸 수 있음

텍스트 사이사이에 ```execution.setVariable(request.getPrefix() + ".responseProtocol", response.getProtocol())``` 이런식으로 ```execution.setVariable(request.getPrefix() + "ResponseProtocol", response.getProtocol())``` 내용 작성이 가능함



github 주소：[https://github.com/ahw9995](https://github.com/ahw9995)

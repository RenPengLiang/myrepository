# 基于DFA的JAVA敏感词过滤

#### 项目介绍
基于DFA算法实现敏感词过滤组件：将文本段敏感词替换为特定字符(*)
DFA实现思路如下：
1.DFA采用Map的hash机制，将敏感词单个拆分，以第1个字符为key，其他值依旧使用map相连，形成了大map套用小map。
2.遍历需要过滤的字符串，获取每一个字符，根据get(key)来检测是否为敏感词。

#### 集成步骤
1.引入jar包
   <dependency>
      <groupId>com.cjkj</groupId>
      <artifactId>cjkj-sensitivewordfilter-spring-boot-starter</artifactId>
      <version>1.5.0</version>
    </dependency>
2.调用SensitiveWordFilter工具类的filterInfo方法进行敏感词过滤

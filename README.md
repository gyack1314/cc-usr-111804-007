# 训练数据标注更正与原始片段引用采集

现有项目保存标注分页与质检决定的冻结来源响应。transport 核对请求和原文字节，domain 提取来源声明的资料身份，ledger 原子保存版本，view 展示已收资料及待核状态。合成样例不访问外部站点，跨来源业务归属尚未形成。

在项目根目录运行：

    python -m unittest discover -s tests -v
    python -m compileall -q capture_service tests
    python -m capture_service.cli inspect data/normal.json

容器运行：docker build -t robot-collection-007 .；docker run --rm robot-collection-007。

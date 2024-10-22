## INSTATLL
git clone 
uvicorn backend.app:app --reload
streamlit run frontend/main.py

step 1:
query：{query}
你是一位情报领域的专家，擅长处理各种情报数据。请使用72B的qwen2.5模型生成3条化学品价格相关的情报数据，每条数据字数在50-100字, 结果以["s1", "s2", "s3]格式返回。
(bp)

step 2:
    遍历{1}:
        使用gemma-2-27b模型对内容进行分类，分类规则如下：   
        `价格`: 情报主要内容为价格的变化、涨跌情况;
        `供应`: 情报主要内容是生产、库存以及供应量的变化情况；
        请将情报数据归纳到对应的分类中，只返回情报所属的类别名。

step 3:
    tool_call('send_email', texts={1}通过我的邮箱发送给客户，主题为化学品调研。我的邮箱为“lby15356@gmail.com”，密码为“seulby356..”，客户邮箱为“Young.liu@aishu.cn。使用llama3-8b-8192模型。”)

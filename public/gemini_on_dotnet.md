---
title: .NET(C#)でGemini proを扱ったときのメモ。
tags:
  - '.NET'
  - '備忘録'
private: false
updated_at: ''
id: null
organization_url_name: null
slide: false
ignorePublish: false
---
# .NET(C#)でもGemini proを扱える！
APIのドキュメンテーションをはじめて見たときは、.NET(C#)はなかったように記憶しているが、気づいたら説明が追加されてた。試しに触ってみたので、備忘録として残しておく。

## コード

'''c#:main.cs
using System;

namespace Gemini_api_test
{
    class Program
    {
        static async Task Main(string[] args)
        {
            var secret_key = WebApplication.CreateBuilder(args).Configuration["secret_key"];
            var chatSample = new MultiTurnChatSample();
            await chatSample.GenerateContent(
                projectId: secret_key
                );
        }
    }
}
'''


## 参考文献

https://cloud.google.com/vertex-ai/generative-ai/docs/start/quickstarts/quickstart-multimodal#gemini-beginner-samples-csharp


---
title: "[.NET] Runtime에 따른 Destructor 호출 차이"
categories:
  - .NET
tags:
  - C#
  - Distructor
  - Class
  - GC
  _ Memory
---



```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp8
{
    class Program
    {
        static void Main(string[] args)
        {
            MyClass a = new MyClass();

            a = null;

            Console.WriteLine("1");
            GC.Collect();
            Console.WriteLine("2");
            GC.WaitForPendingFinalizers();
            Console.WriteLine("3");
        }
    }
    internal class MyClass
    {
        public MyClass()
        {
            Console.WriteLine("Create");
        }

        ~MyClass()
        {
            Console.WriteLine("Delete");
        }
    }
}

```

```bash
Create
1
2
Delete
3
```

```bash
Create
1
2
3
```

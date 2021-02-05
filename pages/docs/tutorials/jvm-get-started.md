---
type: tutorial
layout: tutorial
title:  "Getting Started with IntelliJ IDEA"
description: "This tutorial demonstrates how to use IntelliJ IDEA for creating a console application. "
authors: Kate Volodko
date: 2020-07-07
showAuthorInfo: false
---

To get started, first download and install the latest version of [IntelliJ IDEA](http://www.jetbrains.com/idea/download/index.html).

## 创建一个 application 

你已经下载了 IntelliJ 运行环境的程序（Android开发环境）, 是时候去创建你自己的第一个 Kotlin application.


1. 在 IntelliJ IDEA, 依次点击 **File** \| **New** \| **Project**.---->>创建第一个项目
2. 在左边的列表里, 选择 **Kotlin**.------->>选择语言
3. 写入你的项目名称, 依次点击 **Console Application** as the project template, and click **Next**.----->>从文件名开始你的创作
   
   ![Create a console application]({{ url_for('tutorial_img', filename='getting-started/jvm-new-project-1.png') }})
   
   默认状态下, 你的项目将使用 Gradle 创建 Kotlin DSL.

3. 浏览并接受了默认设置, 就点击  **Finish**.
  
   ![Configure a console application]({{ url_for('tutorial_img', filename='getting-started/jvm-new-project-2.png') }}) 

   你的项目将要打开. 一般情况下, 你将看到一个文件 `build.gradle.kts`, 这是这个项目已经帮您创建了脚本
   Wizard based on your configuration. It includes the `kotlin("jvm")` plugin and dependencies required for your console application.

3. 打开 `main.kt` 文件在 `src/main/kotlin`.  
   The `src` directory contains Kotlin 源代码文件和资源文件 . The `main.kt` file contains sample code that will print 
   `Hello World!`.

   ![main.kt with main fun]({{ url_for('tutorial_img', filename='getting-started/jvm-main-kt-initial.png') }})

4. Modify the code so that it requests your name and says `Hello` to you specifically, and not to the whole world.  
   
   * Introduce a local variable `name` with the keyword `val`. It will get its value from an input where you will enter your name – `readLine()`.
   * Use a string template by adding a dollar sign `$` before this variable name directly in the text output like this – `$name`.
   
   <div class="sample" markdown="1" theme="idea" mode="kotlin" data-highlight-only>
   
   ```kotlin
   fun main() {
       println("What's your name?")
       val name= readLine()
       println("Hello $name!")
   }
   ```
   
   </div>

   <img class="img-responsive" src="{{ url_for('tutorial_img', filename='getting-started/jvm-main-kt-updated.png') }}" alt="Updated main fun" width="400"/>

## 运行 application

Now the application is ready to run. The easiest way to do this is to click the green __Run__ icon in the gutter and select __Run 'MainKt'__.

<img class="img-responsive" src="{{ url_for('tutorial_img', filename='getting-started/jvm-run-app.png') }}" alt="Running a console app" width="400"/>

You can see the result in the **Run** tool window.

![Kotlin run output]({{ url_for('tutorial_img', filename='getting-started/jvm-output-1.png') }})
   
Enter your name and accept the greetings from your application! 

![Kotlin run output]({{ url_for('tutorial_img', filename='getting-started/jvm-output-2.png') }})

恭喜！ 你现在运行了第一个 Kotlin 应用程序。

## What's next?

Once you’ve created this application, you can start to dive deeper into Kotlin syntax:

*   Add sample code from [Kotlin examples](https://play.kotlinlang.org/byExample/overview) 
*   Install the [EduTools plugin](https://plugins.jetbrains.com/plugin/10081-edutools) for IDEA and complete exercises 
from the [Kotlin Koans course](https://www.jetbrains.com/help/education/learner-start-guide.html?section=Kotlin%20Koans)

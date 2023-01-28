# Self-editing
## Adopt a style guide
[Google Developer Documentation Style Guide](https://developers.google.com/style)

## Think like your audience
It can be helpful to outline a **persona** for your audience. A persona can consist of any of the following attributes:
- A role, such as Systems Engineer or QA Tester.
- An end goal, such as Restore the database.
- A set of assumptions about the persona and their knowledge and experience. For example, you might assume that your persona is:
  - Familiar with Python.
  - Running a Linux operating system.
  - Comfortable following instructions for the command line.

**Tips:** Tell your audience about any assumptions you've made. Provide links to resources where they can learn more if they need to brush up on a specific topic.

## Read it out aloud
To check if your writing is conversational, read it out loud. Listen for awkward phrasing, too-long sentences, or anything else that doesn't feel natural. Alternatively, consider using a [screen reader](https://en.wikipedia.org/wiki/Screen_reader) to voice the content for you.

For more information on adjusting the style of your writing to suit your audience, see [Style and authorial tone](https://developers.google.com/style/tone).

## Come back to it later
After you write your first draft (or second or third), set it aside. Come back to it after an hour (or two or three) and try to read it with fresh eyes. You'll almost always notice something that you could improve.

## Change the context
A change of context when reviewing your own work can help you find things to improve.For example, print your documentation and review a paper copy. For a modern take on this classic tip, copy your draft into a different document and change the font, size, and color.

## Find a peer editor

## 练习
> Determine whether or not you can simplify your document through the use of terminology that is equivalent but relatively shorter in length and therefore more easily comprehensible by your audience. It's important to make sure your document is edited before it is seen by your audience, which might include people that are less or more familiar with the matter covered by your document. The first thing you need is a rough draft. Some things that can help make your document easier to read are making sure you have links to background information, and also checking for active voice instead of passive voice. If you have long sentences you can consider shortening them or implementing the use of a list to make the information easier to scan.
>
> 参考答案
> To help your audience understand your document, apply these basic editing principles:
> - Use active voice instead of passive voice.
> - Consider using simpler words that mean the same thing.
> - Include links to background information.
> - Break long sentences into shorter sentences or lists.


# Organizing large documents
The remainder of this unit covers techniques that can be useful for writing longer documents, such as tutorials and some conceptual guides.
## Organize a document
### Outline a document
You might find it useful to think of an outline as the narrative for your document. There is no standard approach to writing an outline, but the following guidelines provide practical tips you might find useful:
- Before you ask your reader to perform a task, explain to them why they are doing it. 
>For example, the following bullet points illustrate a section of an outline from a tutorial about auditing and improving the accessibility of web pages:
  >- Introduce a browser plugin that audits the accessibility of web pages; explain that the reader will use the results of the audit report to fix several bugs.
  >- List the steps to run the plugin and audit the accessibility of a web page.
- Limit each step of your outline to describing a concept or completing a specific task.
- Structure your outline so that your document introduces information when it's most relevant to your reader. 
For example, your reader probably doesn't need to know (or want to know) about the history of the project in the introductory sections of your document when they're just getting started with the basics. If you feel the history of the project is useful, then include a link to this type of information at the end of your document.
- Explain a concept and then demonstrating how the reader can apply it either in a sample project or in their own work. 
- Before you start drafting, share the outline with your contributors. Outlines are especially useful if you're working with a team of contributors who are going to review and test your document.

[练习](https://developers.google.com/tech-writing/two/large-docs#outline_exercise)

### Introduce a document
If readers of your documentation can't find relevance in the subject, they are likely to ignore it. To set the ground rules for your users, we recommend providing an introduction that includes the following information:
- What the document covers.
- What prior knowledge you expect readers to have.
- What the document doesn't cover.

DO NOT try to cover everything in the introduction.

例子：
The following paragraph demonstrates the ideas from the preceding list as an overview for a hypothetical document publishing platform called Froobus:
>This document explains how to publish Markdown files using the Froobus system. Froobus is a publishing system that runs on a Linux server and converts Markdown files into HTML pages. // This document is intended for people who are familiar with Markdown syntax. To learn about the syntax, see the Markdown reference. You also need to be comfortable running simple commands in a Linux terminal.// This document doesn't include information about installing or configuring a Froobus publishing system. For information on installing Froobus, see Getting started.

After you've completed the first draft, check your entire document against the expectations you set in your overview. 

#### 练习
For this exercise, review and revise the following introduction for a best practices guide for a hypothetical programming language called F@. Remove any information you feel is irrelevant in this context and add any information you feel is missing.

> This guide lists best practices for working with the F@ programming language. F@ was developed in 2011 as an open source community project. This guide supplements the F@ style guide. In addition to the best practices in this guide, make sure you also install the F@ command-line linter and run it on your code. The programming language is widely adopted in the health industry. If you have suggestions for additions to the list of best practices, file an issue in the F@ documentation repository.

参考答案
>This guide lists best practices for working with the F@ programming language. Before you review this guide, complete the introductory tutorial for new F@ developers. This guide supplements the F@ style guide. In addition to the best practices in this guide, make sure you also install the F@ command-line linter and run it on your code. If you have suggestions for additions to the list of best practices, file an issue in the F@ documentation repository.

## Add navigation
Clear navigation includes:
- introduction and summary sections
- a clear, logical development of the subject
- headings and subheadings that help users understand the subject
- a table of contents menu that shows users where they are in the document
- links to related resources or more in-depth information
- links to what to learn next

### Prefer task-based headings
Choose a heading that describes the task your reader is working on. Avoid headings that rely on unfamiliar terminology or tools. 
> For example, suppose you are documenting the process for creating a new website. To create the site, the reader must initialize the Froobus framework. To initialize the Froobus framework, the reader must run the carambola command-line tool. At first glance, it might seem logical to add either of the following headings to the instructions:
>- Running the carambola command
>- Initializing the Froobus framework

Unless your readers are already very experienced with the terminology and concepts for this topic, a more familiar heading might be preferable, such as:
> - Creating the site.

### Provide text under each heading
Most readers appreciate at least a brief introduction under each heading to provide some context. Avoid placing a level three heading immediately after a level two heading.(不要大标题立马接小标题，要有个简短的介绍)
[Heading exercise](https://developers.google.com/tech-writing/two/large-docs#heading_exercise)

## Disclose information progressively
Readers are more likely to be receptive to longer documents that progressively disclose new information to them when they need it. The following techniques can help you incorporate progressive disclosure in your documents:
- Try introducing new terminology and concepts near to the instructions that rely on them if possible.
- Avoid multiple large paragraphs on a single page, aim to introduce tables, diagrams, lists, and headings where appropriate.
- Break up large series of steps. If you have a particularly long list of complicated steps, try to re-arrange them into shorter lists that explain how to complete sub-tasks.
    - Start with simple examples and instructions, and add progressively more interesting and complicated techniques. 
    - For example, in a tutorial for creating forms, start by explaining how to handle text responses, and then introduce other techniques to handle multiple choice, images, and other response types.

# Illustrating（作图说明）
## Write the caption（标题） first
It is often helpful to write the caption before creating the illustration. 
Good captions have the following characteristics:
- **Brief**. Typically, a caption is just a few words.
- Explain the **takeaway**(启示). *After viewing this graphic, what should the reader remember?*
- Focus the reader's **attention**. Focus is particularly important when a photograph or diagram contains a lot of detail.

## Constrain the amount of information in a single drawing
一个图中不要超过一个段落能解释完的内容，或者5个列表中的点能解释完的内容。[具体示例](https://developers.google.com/tech-writing/two/illustrations#constrain_the_amount_of_information_in_a_single_drawing)

## Focus the reader's attention
图要重点突出，通过箭头、圆圈等标记指示[具体实例](https://developers.google.com/tech-writing/two/illustrations#focus_the_readers_attention)

# Illustrating is re-illustrating
As with writing, the first draft of an illustration is seldom good enough. Revise your illustrations to clarify the content. As you revise, ask yourself the following questions:
How can I **simplify** the illustration?
Should I **split** this illustration into two or more simpler illustrations?
Is the text in the illustration **easy to read**? Does the text **contrast** sufficiently **with its background**?
What's the **takeaway**?

[示例](https://developers.google.com/tech-writing/two/illustrations#exercise_2)

## Illustration tools
There are many options available for creating diagrams. Three options that are free or have free options include:
- [Google Drawings](https://drawings.google.com/)
- [diagrams.net](https://diagrams.net/)
- [LucidChart](https://www.lucidchart.com/pages/)

When exporting diagrams from these tools to use in documentation, it is usually best to export the files as **Scalable Vector Graphics (SVG)**. The SVG format easily scales diagrams based on space constraints so that no matter the size, you end up with a high quality image.

# Creating sample code
Good samples are **correct** and **concise** code that your readers can **quickly understand** and **easily reuse** with **minimal side effects**.

# Correct
Sample code should meet the following criteria:
- Build **without errors**.
- Perform the task it claims to perform.
- Be as **production-ready** as possible. For example, the code shouldn't contain any security vulnerabilities.
- Follow **language-specific** conventions.（命名习惯？）

Sample code should set the best way to use your product. 
- If there is more than one way to code the task, code it in the manner that your team has decided is best. If your team hasn't considered the pros and cons of each approach, take time to do so.

Always test your sample code. Over time, systems change and your sample code may break. Be prepared to test and maintain sample code as you would any other code.

DO NOT reuse unit tests as sample programs. The primary goal of a unit test is to test; the only goal of a sample program is to educate.

## Running sample code
Good documents explain how to run sample code. For example, your document might need to tell users to perform activities such as the following prior to running the samples:
- Install a certain library.
- Adjust the values assigned to certain environment variables.
- Adjust something in the integrated development environment (IDE).

In some situations, users prefer to run or (experiment with) sample code directly in the documentation. ("Click here to run this code.")

Describing the expected output or result of sample code, especially for sample code that is difficult to run.

# Concise
Sample code should be **short**, including only essential components. When a novice C programmer wants to learn how to call the malloc function, give that programmer a brief snippet, not the entire Linux source tree. (A **snippet** is a piece of a sample program, possibly only one or a few lines long.)

**Prefer correctness over conciseness**. Never use bad practices to shorten your code.

# Understandable
Follow these recommendations to create clear sample code:
- Pick **descriptive** class, method, and variable names.
- Avoid confusing your readers with hard-to-decipher programming tricks.
- Avoid deeply **nested**（嵌套） code.
- Optional: Use bold or colored font to draw the reader's attention to a specific section of your sample code. But DO NOT use too much.

# Commented
Consider the following recommendations about comments in sample code:
- Keep comments short, but always prefer **clarity** over **brevity**.
- **Avoid** writing comments about obvious code, but remember that what is obvious to you (the expert) might not be **obvious to newcomers**.
- Focus your commenting energy on anything **non-intuitive** in the code.
- **When** your readers are very **experienced** with a technology, **don**'t explain **what** the code is doing, explain **why** the code is doing it.

Should you place descriptions of code inside code comments or in text (paragraphs or lists) outside of the sample code? Note that readers who **copy-and-paste(复制黏贴)** a snippet gather not only the code but also any embedded comments. So, put any descriptions that belong in the pasted code into the code comments. By contrast, when you must explain a lengthy or tricky concept, you should typically place the text before the sample program.
是在代码注释中or代码外的文件中写描述，因为复制代码的时候会连注释一起复制，所以写在代码中。

## 练习
What problems do you see in the comments within the following snippet? Assume that the code is aimed at programmers who are new to the br API but who have some experience with the concept of streams:

```python
/* Create a stream from the text file at pathname /tmp/myfile. */
mystream = br.openstream(pathname="/tmp/myfile", mode="z")
```

参考答案：
The comments contain the following flaws:
- The comment elaborates on a fairly obvious part of the code.
- The snippet doesn't explain the non-obvious portion of the code. Namely, what is the mode parameter and what does a value of z mean?

# Reusable
For your reader to easily reuse your sample code, provide the following:
- All **information necessary** to run the sample code, including any **dependencies** and **setup**.
- Code that can be **extended** or **customized** in useful ways.

**Secure and efficient:** Having easy-to-understand sample code that's concise and compiles is a great start. If it blows up your reader's app, though, they won't be happy. Therefore, when writing sample code, consider any potential side effects caused by your code being integrated into another program. Nobody wants insecure or grossly inefficient code.

## The example and the anti-example
正反例子都要举，不仅要告诉他们怎么做，还要告诉他们不要怎么做

# Sequenced
A good set of sample code provides a healthy range of simple, moderate, and complex sample programs.
## 练习
Which of the following would be a good set of sample functions to support a tutorial introducing newcomers to the concept of functions?

1. The following set of functions:
  - A function that takes no parameters and doesn't return anything.
  - A function that takes one parameter but doesn't return anything.
  - A function that takes one parameter and returns one value.
  - A function that takes three parameters and returns one value.
2. The following set of functions:
- A function that takes three parameters and returns one value.
3. The following set of functions:
- A function that takes one parameter and returns one value.
- A function that takes three parameters and returns one value.

参考答案：
The best answer is 1. Providing samples that cover a range of complexity is usually the wisest choice—particularly for newcomers. Resist the temptation to rush towards very complex sample programs, bypassing the beginner and intermediate sample programs that newcomers crave.

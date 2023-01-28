
# vocabulary
terminology
abbreviations
acronyms
ambiguous pronouns
active voice
passive voice
bulleted list
numbered list
comma
parentheses
colons
dashes
semicolons
variable 变量
compile 编译
synonyms 同义词
## Words
### Define new or unfamiliar *terms*
定义新或不常见术语
  When writing or editing, learn to recognize terms that might be unfamiliar to some or all of your target audience. When you spot such a term, take one of the following two tactics:
- If the term already exists: link to a good existing explanation. (*Don't reinvent the wheel*.)
  如果术语以及存在，链接到一个好的术语解释，不要重复造轮子
- If your document is introducing the term:
  如果你的文档在介绍这个术语，定义这个术语
   define the term. 
   - If your document is introducing many terms, collect the definitions into a *glossary*.（如果术语较多，将定义汇集成一个词汇表）

### Use terms consistently
就像在编程中使用同一个变量名一样，术语也需要前后使用一致.

The moral: apply the same unambiguous word or term consistently throughout your document. Once you've named a component thingy, don't rename it thingamabob. For example, the following paragraph mistakenly renames Protocol Buffers to protobufs:

>Protocol Buffers provide their own definition language. Blah, blah, blah. And that's why protobufs have won so many county fairs.

Namely, when introducing a long-winded concept name or product name, you may also specify a shortened version of that name. Then, you may use that shortened name throughout the document. For example, the following paragraph is fine:
当定义一个比较冗长的术语的时候，往往会指定其缩写版，并在后文中一直使用缩写版，例如

>Protocol Buffers (or protobufs for short) provide their own definition language. Blah, blah, blah. And that's why protobufs have won so many county fairs.

### Use *acronyms* properly
On the initial use of an unfamiliar *acronym* within a document or a section, spell out the *full term*, and then put the acronym in parentheses. Put both the spelled-out version and the acronym *in boldface*. For example:
在初次使用缩写的时候，要一并写出全称并加粗：

> This document is for engineers who are new to the **Telekinetic Tactile Network (TTN)** or need to understand how to order TTN replacement parts through finger motions.

You may then use the acronym going forward, as in the following example:
在之后的文章里，你可以使用缩写，如下所示：

> If no cache entry exists, the Mixer calls the **OttoGroup Server (OGS)** to fetch Ottos for the request. The OGS is a repository that holds all servable Ottos. The OGS is organized in a logical tree structure, with a root node and two levels of leaf nodes. The OGS root forwards the request to the leaves and collects the responses.

Do not cycle back-and-forth between the acronym and the *expanded version* in the same document.
不要再一个文章中来回切换全称和缩写

### Use the acronym or the full term?
Sure, you can introduce and use acronyms properly, but should you use acronyms? Well, acronyms do reduce sentence size. For example, TTN is two words shorter than Telekinetic Tactile Network. However, acronyms are really just a layer of abstraction; readers must mentally expand recently learned acronyms to the full term. For example, readers convert TTN to Telekinetic Tactile Network in their heads, so the "shorter" acronym actually takes a little longer to process than the full term.
缩写虽然可以缩短句子结构，但是读者依然要子啊脑海中将其展开，会消耗读者时间

Heavily used acronyms develop their own identity. After a number of occurrences, readers generally stop expanding acronyms into the full term. Many web developers, for example, have forgotten what HTML expands to.
频繁使用的术语会形成他们自己的可辨识性，在多次出现后，读者就会停止在脑海中展开缩写，就像很多Web开发者已经忘记HTML的意思一样。

Here are the guidelines for acronyms:
###一些使用缩写的指导

- Don't define acronyms that would only be used a few times.
不要定义只出现几次的单词的缩写
- **Do define acronyms that meet both of the following criteria**:
出现以下情形时 定义缩写
    - The acronym is significantly shorter than the full term. （缩写明显短语全称）
    - The acronym appears many times in the document.（缩写在文中多次出现）

### Recognize ambiguous pronouns 发现语义不清的代词
Many pronouns point to a previously introduced noun. Such pronouns are analogous to pointers in programming. Like pointers in programming, pronouns tend to introduce errors. Using pronouns improperly causes the cognitive equivalent of a null pointer error in your readers’ heads. In many cases, you should simply avoid the pronoun and just reuse the noun. However, the utility of a pronoun sometimes outweighs its risk (as in this sentence).
很多单词会指代签名的名词，就想编程中的指针一样。但是使用代词的风险往往大于其便利
#### 使用代词的指引 Consider the following pronoun guidelines:

- Only use a pronoun after you've introduced the noun; never use the pronoun before you've introduced the noun.
只在介绍完名词的时候使用代词，不要在介绍前使用代词。
- Place the pronoun as close as possible to the referring noun. In general, if more than five words separate your noun from your pronoun, consider repeating the noun instead of using the pronoun.
代词离其指代的名词越近越好，一般来说，不要超过五个词，否则用原名词取代代词。
- If you introduce a second noun between your noun and your pronoun, reuse your noun instead of using a pronoun.
如果你在名词和代词之间介绍第二个名词，使用名词而非代词。

#### 常见的错误实例
##### It and they/them/their
For example, in the following sentence, does It refer to Python or to C++?
- Python is interpreted, while C++ is compiled. It has an almost cult-like following.

As another example, what does their refer to in the following sentence?
- Be careful when using Frambus or Carambola with HoobyScooby or BoiseFram because a bug in their core may cause accidental mass unfriending.

##### This and that
For example, in the following ambiguous sentence, This could refer to the user ID, to running the process, or to all of these:

- Running the process configures permissions and generates a user ID. This lets users authenticate to the app.

###### 改进办法
To help readers, avoid using this or that in ways where it's not clear what they refer to. Use either of the following tactics to clarify ambiguous uses of this and that:

- Replace this or that with the appropriate noun. 使用名词替换
- Place a noun immediately after this or that. 在this/that后面马上放置名词

###### 修改示例
Substitute or add explicit terms as needed, as in the following rewrites of the example's second sentence:

> - This user ID lets users authenticate.
> - The process of configuring permissions lets users authenticate.
> - The combination of permissions and a user ID lets users authenticate.

##### 小练习
Identify all possible meanings for the ambiguous pronouns in each of the following passages:
1. Aparna and Phil share responsibilities with Maysam and Karan and they are next on call.
2. You may import Carambola data via your configuration file or dynamically at run time. This may be a security risk.

答案：
1. The pronoun they could refer to any of the following:
   - Aparna and Phil
   - Maysam and Karan
   - Aparna, Phil, Maysam, and Karan
   - any one of the individuals as a singular gender-neutral pronoun
2. The pronoun this could refer to any of the following:
   - importing via the configuration file
   - importing dynamically at run time
   - both


# Active voice vs. passive voice 主动和被动语态
Prefer active voice to passive voice

# Clear Sentences
## Choose strong verbs
To engage and educate readers, choose precise, strong, specific verbs. Reduce imprecise, weak, or generic verbs, such as the following:
- forms of be: is, are, am, was, were, etc.
- occur
- happen

For example, consider how strengthening the weak verb in the following sentences ignites a more engaging sentence:
Weak Verb | Strong Verb
--- | ---
The exception **occurs** when dividing by zero.	 | Dividing by zero **raises** the exception.
This error message **happens** when...	| The system **generates** this error message when...
We **are** very careful to ensure...	| We carefully **ensure**...

### 练习
1. When a variable declaration doesn't have a datatype, a compiler error happens.
    参考答案：
   When a variable declaration doesn't specify a datatype, the compiler generates an error message.
   If you declare a variable but don't specify a datatype, the compiler generates an error message.
2. Compiler errors occur when you leave off a semicolon at the end of a statement.
   参考答案：
   Compilers issue errors when you omit a semicolon at the end of a statement.
   A missing semicolon at the end of a statement triggers compiler errors.

## 减少there be
Removing There is replaces the generic subject with a better subject. For example, either of the following sentences is clearer than the original:
> There is a variable called met_trick that stores the current accuracy.
参考修改：
A variable named met_trick stores the current accuracy.
The met_trick variable stores the current accuracy.

You can sometimes repair a There is or There are sentence by moving the true subject and true verb from the end of the sentence to the beginning. For example, notice that the pronoun you appears towards the end of the following sentence:

> There are two disturbing facts about Perl you should know.
参考修改：
You should know two disturbing facts about Perl.

In other situations, writers start sentences with There is or There are to avoid the hassle of creating true subjects or verbs. If no subject exists, consider creating one. For example, the following There is sentence does not identify the receiving entity:
有时候there be是为了避免创造主语，如果没有主语，自己造一个。

> There is no guarantee that the updates will be received in sequential order.

Replacing "There is" with a meaningful subject (such as clients) creates a clearer experience for the reader:

> Clients might not receive the updates in sequential order.
### 练习
1. There is a lot of overlap between X and Y.
2. There is no creator stack for the main thread.
3. There is a low-level, TensorFlow, Python interface to load a saved model.
4. There is a sharding function named distribute that assigns keys.
   参考答案
   1. X and Y overlap a lot.The main thread does not provide a creator stack.
   2. TensorFlow provides a low-level Python interface to load a saved model.
   3. The distribute sharding function assigns keys.

## Minimize certain adjectives and adverbs

# Short sentences
## Focus each sentence on a single idea
如代码精简的道理一样，简短的句子更容易阅读、维护、不易出错

Focus each sentence on a single idea, thought, or concept. Just as statements in a program execute a single task, sentences should execute a single idea. For example, the following very long sentence contains multiple thoughts:
#### 例子
> The late 1950s was a key era for programming languages because IBM introduced Fortran in 1957 and John McCarthy introduced Lisp the following year, which gave programmers both an iterative way of solving problems and a recursive way.

Breaking the long sentence into a succession of single-idea sentences yields the following result:
>The late 1950s was a key era for programming languages. IBM introduced Fortran in 1957. John McCarthy invented Lisp the following year. Consequently, by the late 1950s, programmers could solve problems iteratively or recursively.

##### 练习
> In bash, use the if, then, and fi statements to implement a simple conditional branching block in which the if statement evaluates an expression, the then statement introduces a block of statements to run when the if expression is true, and the fi statement marks the end of the conditional branching block.
参考答案
In bash, use an **if**, then, and **fi** statement to implement a simple conditional branching block. The **if** statement evaluates an expression. The **then** statement introduces a block of statements to run when the **if** expression is true. The **fi** statement marks the end of the conditional branching block. (The resulting paragraph remains unclear but is still much easier to read than the original sentence.)

## Convert some long sentences to lists
When you see the conjunction **or** in a long sentence, consider refactoring that sentence into a bulleted list. When you see an embedded list of items or tasks within a long sentence, consider refactoring that sentence into a bulleted or numbered list. For example, the preceding example contains the conjunction or, so let's convert that long sentence to the following bulleted list:
注意长句中的or

### 例子：
> To alter the usual flow of a loop, you may use either a break statement (which hops you out of the current loop) or a continue statement (which skips past the remainder of the current iteration of the current loop).

To alter the usual flow of a loop, call one of the following statements:
- `break`, which hops you out of the current loop.
- `continue`, which skips past the remainder of the current iteration of the current loop.
  
### 练习
1. To get started with the Frambus app, you must first find the app at a suitable store, pay for it using a valid credit or debit card, download it, configure it by assigning a value for the Foo variable in the /etc/Frambus file, and then run it by saying the magic word twice.
参考答案：
    Take the following steps to get started with the Frambus app:
    1. Find the app at a suitable store.
    2. Pay for the app using a valid credit or debit card.
    3. Download the app.
    4. Configure the app by assigning a value for the Foo variable in the **/etc/Frambus** file.
    5. Run the app by saying the magic word twice.
2. KornShell was invented by David Korn in 1983, then a computer scientist at Bell Labs, as a superset of features, enhancements, and improvements over the Bourne Shell (which it was backwards compatible with), which was invented by Stephen Bourne in 1977 who was also a computer scientist at Bell Labs.
参考答案：
The following two Bell Labs computer scientists invented popular shells:
   - Stephen Bourne invented the Bourne Shell in 1977.
   - David Korn invented the KornShell in 1983.
   The KornShell is a backwards-compatible superset of the Bourne Shell, containing many improvements over the older shell.


## Eliminate or reduce extraneous words
### 例子
> 1. An input value greater than 100 causes the triggering of logging.
> 修改后：
> An input value greater than 100 triggers logging.
> 2. This design document provides a detailed description of Project Frambus.
> 修改后
> This design document describes Project Frambus.
### 常见替换
Wordy | Concise
--- | ---
at this point in time | now
determine the location of | find
is able to | can
### 练习
1. In spite of the fact that Arnold writes buggy code, he writes error-free documentation.
   修改后：
   Although Arnold writes buggy code, he writes error-free documentation.
   Arnold writes buggy code. However, he writes error-free documentation.
2. Changing the sentence from passive voice to active voice enhances the clarification of the key points.
   修改后
   Changing the sentence from passive voice to active voice clarifies the key points.
3. Determine whether Rikona is able to write code in COBOL.
   修改后
   Determine whether Rikona can code in COBOL.
4. Frambus causes the production of bugs, which will be chronicled in logs by the LogGenerator method.
   修改后
   Frambus produces bugs, which the LogGenerator method logs.

## 减少从句
## 区分which和that
In the United States, reserve which for nonessential subordinate clauses, and use that for an essential subordinate clause that the sentence can't live without. For example, the key message in the following sentence is that Python is an interpreted language; the sentence can survive without Guido van Rossum invented:
which引导的可独立成句，that不行，例如：
> Python is an interpreted language, **which** Guido van Rossum invented.
> Fortran is perfect for mathematical calculations **that** don't involve linear algebra.

有停顿的时候用which(,)，没有停顿的时候用that

# Lists and Tables
## Choose the correct type of list
Use a **bulleted list** for unordered items; use a **numbered list** for ordered items.

## Keep list items parallel（一致性?）
All items in a **parallel** list look like they "belong" together. That is, all items in a parallel list match along the following parameters:
For example, the following list is parallel because all the items are <u>plural nouns (grammar), edible (logical category), lower case (capitalization), and without periods or commas (punctuation).</u>
- carrots
- potatoes
- cabbages
By contrast, the following list is painfully nonparallel along all four parameters:
- carrots
- potatoes
- The summer light obscures all memories of winter.

## Start numbered list items with imperative verbs 有序列表使用祈使句

### 练习
> 1. Stop Frambus
> 2. The key configuration file is /etc/frambus. Open this file with an ASCII text editor.
> 3. In this file, you will see a parameter named Carambola, which is currently set to the default value (32). Change this value to 64.
> 4. When you are finished setting this parameter, save and close the configuration file
> 5. now, start Frambus again.

修改后：
> 1. Stop Frambus.
> 2. Open the key configuration file, /etc/frambus, with an ASCII text editor.
> 3. Change the Carambola parameter from its default value (32) to 64.
> 4. Save and close the configuration file.
> 5. Restart Frambus.

## Punctuate items appropriately 正确使用大小写
如果列表元素是句子，使用开头大写，否则，不要使用开头大写

## Create useful tables
创建表格的建议：
- Label each column with a meaningful header. Don't make readers guess what each column holds. 写一个有意义的标题，不要让读者猜每一列的意思
- Avoid putting too much text into a table cell. If a table cell holds more than two sentences, ask yourself whether that information belongs in some other format. 一个单元格中不要有太多东西，如果太多，请反省一下这些东西是不是应该在同一个单元格中
- Although different columns can hold different types of data, strive for parallelism within individual columns. For instance, the cells within a particular table column should not be a mixture of numerical data and famous circus performers.虽然不同列代表不同的东西，但是尽量保持单元格之间的一致性

## Introduce each list and table
Give the list or table context. Terminate the introductory sentence with a **colon** rather than a **period**（介绍结束时，使用引号而不是句号）.
Although not a requirement, we recommend putting the word following into the introductory sentence. <u>（建议使用following这个单词）</u>
> The following list identifies key performance parameters:
Take the following steps to install the Frambus package:
The following table summarizes our product's features against our key competitors' features:

# Paragraphs
## Write a great opening sentence 写好开头句
Good opening sentences establish the paragraph's central point. 
### 例子
正面例子：
> A loop runs the same block of code multiple times. For example, suppose you wrote a block of code that detected whether an input line ended with a period. To evaluate a million input lines, create a loop that runs a million times.

反面例子：
> A block of code is any set of contiguous code within the same function. For example, suppose you wrote a block of code that detected whether an input line ended with a period. To evaluate a million input lines, create a loop that runs a million times.

### 练习
Q: Is the opening sentence of the following paragraph effective or defective?
> The Pythagorean Theorem states that the sum of the squares of both legs of a right triangle is equal to the square of the hypotenuse. The k-means clustering algorithm relies on the Pythagorean Theorem to measure distances. By contrast, the k-median clustering algorithm relies on the Manhattan Distance.

参考答案
This opening sentence is defective because it implies that the paragraph will focus on the Pythagorean Theorem. In fact, the paragraph's focus is actually clustering algorithms. The following would be a more effective opening sentence:
> Different clustering algorithms measure distances differently.

## Focus each paragraph on a single topic
A paragraph should represent an independent unit of logic. Restrict each paragraph to the current topic. Don't describe what will happen in a future topic or what happened in a past topic. When revising, ruthlessly delete (or move to another paragraph) any sentence that doesn't directly relate to the current topic.
一段内不要说之后/之前的段落要讲的内容，在修改时，要毫不留情地删除没有用的内容。

## Don't make paragraphs too long or too short
一段话以3-5句为宜，不要大于7。

## Answer what, why, and how
Good paragraphs answer the following three questions:
- What are you trying to tell your reader?
- Why is it important for the reader to know this?
- How should the reader use this knowledge? Alternatively, how should the reader know your point to be true?

示例：
> The garp() function returns the delta between a dataset's mean and median.// Many people believe unquestioningly that a mean always holds the truth. However, a mean is easily influenced by a few very large or very small data points.// Call garp() to help determine whether a few very large or very small data points are influencing the mean too much. A relatively small garp() value suggests that the mean is more meaningful than when the garp() value is relatively high.


# Audience
> good documentation = knowledge and skills your audience needs to do a task − your audience's current knowledge and skills

In other words, make sure your document provides the information that your audience needs but doesn't already have
## Define your audience
你估计没那么多时间，此处有简化版的：
Begin by identifying your audience's role(s). Sample roles include:
- software engineers
- technical, non-engineer roles (such as technical program managers)
- scientists
- professionals in scientific fields (for example, physicians)
- undergraduate engineering students
- graduate engineering students
- non-technical positions

虽然没有科技背景的人可能数学也很好，但是根据角色定义是一个比较高效的方法。但仅仅是角色还不够，同样是软件工程师，有些熟悉C++，有些熟悉Python...
并且，时间也很关键，一般的软件工程师在大学都学过代数，但是工作中用的较少，因此相应知识往往会退化。

## Sample audience analysis
> The target audience for Project Zylmon falls into the following roles:
> - software engineers
> - technical product managers

> The target audience has the following proximity to the knowledge:
> - My target audience already knows the Zyljeune APIs, which are somewhat similar to the Zylmon APIs.
> - My target audience knows C++, but has not typically built C++ programs in the new Winged Victory development environment.
> - My target audience took linear algebra in university, but many members of the team need a refresher on matrix multiplication.

## Determine what your audience needs to learn
Write down a list of everything your target audience needs to learn to accomplish goals. In some cases, the list should hold tasks that the target audience needs to perform. 
> After reading the documentation, the audience will know how to do the following tasks:
> - Use the Zylmon API to list hotels by price.
> - Use the Zylmon API to list hotels by location.
> - Use the Zylmon API to list hotels by user ratings.

Note that your audience must sometimes master tasks in a certain order. For example, your audience might need to learn how to build and execute programs in a new development environment before learning how to write particular kinds of programs.
这些任务可能会有特定的顺序，如最先要配置环境

If you are writing a design spec, then your list should focus on information your target audience should learn rather than on mastering specific tasks. For example:
需要聚焦于你的受众所欠缺的知识，而非他们已经掌握的知识
> After reading the design spec, the audience will learn the following:
> - Three reasons why Zylmon outperforms Zyljeune.
> - Five reasons why Zylmon consumed 5.25 engineering years to develop.

## Fit documentation to your audience
### Vocabulary and concepts
建议见[word部分](#words)

### Curse of knowledge
Experts often suffer from the **curse of knowledge**, which means that their expert understanding of a topic ruins their explanations to newcomers. 

From the novice's point of view, the curse of knowledge is <u>a "File not found" linker error due to a module not yet compiled</u>.

#### 练习：
1. Assume that the following paragraph is the start of a paper aimed at physicians who have never programmed before. Identify the aspects of the paragraph that suffer from the curse of knowledge:
> C is a mid-level language, higher than assembly language but lower than Python and Java. The C language provides programmers fine-grained control over all aspects of a program. For example, using the C Standard Library, it is easy to allocate and free blocks of memory. In C, manipulating pointers directly is mundane.
参考答案：
This paragraph suffers immensely from the curse of knowledge. The target audience has never programmed before, so the following terms are inappropriate or unfamiliar:
- language
- mid-level language
- assembly language
- Python
- Java
- program
- C Standard Library
- allocate and free blocks of memory
- pointers
2. Suppose the preceding paragraph was aimed at undergraduate computer science students new to C but comfortable with Python. Does the paragraph still suffer from the curse of knowledge?
   参考答案：
   This paragraph also suffers from the curse of knowledge for the alternative audience. The average Python programmer is unaware of manipulating memory or pointers. A better introductory paragraph would compare and contrast C with Python.

### Use simple words
### Cultural neutrality and idioms

# documents
## State your document's scope
A good document begins by defining its **scope**. For example:
> This document <u>describes</u> the design of Project Frambus.

A better document additionally defines its **non-scope**—the topics not covered that the target audience might reasonably expect your document to cover. For example:
> This document <u>does not describe</u> the design for the related technology, Project Froobus.

### 练习
Q: What problem do you see in the following paragraph?
> This document explains how to use the Frambus API to create, update, and publish Fwidgets. This document does not explain how to use the Frambus API to delete Fwidgets or cover the history of the Linux operating system.

A: The non-scope should only include information that users would reasonably expect the document to cover. No reasonable user would expect the document to cover the history of the Linux operating system.

## State your audience
- Specifies audience. For example:

   > This document is aimed at the following audiences:
   > - software engineers
   > - program managers

- Specify any prerequisite know
- ledge or experience. For example:
   > This document assumes that you understand matrix multiplication and the fundamentals of backpropagation.

   In some cases, the audience declaration should also specify prerequisite reading or coursework. For example:
   > You must read "Project Froobus: A New Hope" prior to reading this document.

## Summarize key points at the start
### Compare and contrast
compare and contrast your ideas with concepts that your audience already understands. For example:
> This new app is similar to the Frambus app, except with much better graphics.

Or:
>The Froobus API handles the same use cases as the Frambus API, except that the Froobus API is much easier to use.

#### 练习
What problem do you see in the following introduction?

> Frambus Weather app v2 introduces ten features not available in Frambus Weather app v1. Most importantly, v2 offers two-week forecasts, v1 offered only one-week forecasts. Tidal information won't change.

答案：
> The final sentence (about tides) isn't important enough to appear in the opening paragraph. The first sentence mentioned ten new features, so readers would likely expect to hear more about those new features. Instead, the final sentence refers to something other than a new feature.


## Write for your audience
In this section, we focus on audience definition as a means of organizing your document.
Answering the following questions helps you determine what your document should contain:

- Who is your target audience?
- What is your target audience's goal? Why are they reading this document?
- What do your readers already know before they read your document?
- What should your readers know or be able to do after they read your document?

For example, suppose you have invented a new sorting algorithm, which is similar to quicksort. The following list contains some potential answers to the preceding questions:

- Who is your target audience? The target audience consists of all the software engineers in my organization.
- What is your target audience's goal? My target audience wants to find more efficient ways to sort data. They are reading this document to determine whether this new algorithm is worth implementing.
- What do your readers already know before they read your document? My target audience knows how to write code and has previously studied sorting algorithms, including quicksort. However, most people in my target audience haven't implemented or evaluated a sorting algorithm in several years.
- What should your readers know or be able to do after they read your document? My target audience will be able to do all of the following:
   - Understand how the algorithm compares and contrasts with quicksort.
   - Identify the two kinds of datasets for which the algorithm outperforms the quicksort algorithm.
   - Implement the algorithm in their choice of programming language.
   - Identify the two edge cases in which the algorithm performs poorly.

## Organize the document to meet your audience's needs
After defining the audience's needs, organize the document to help readers get the information they need. For example, based on the answers in the previous section, the outline for the document could look as follows:
1. Overview of the algorithm
   - Compare and contrast with quicksort, including Big O comparisons
      - Link to Wikipedia article on quicksort
   - Optimal datasets for the algorithm
1. Implementing the algorithm
   - Implementation in pseudocode
   - Implementation tips, including common mistakes
2. Deeper analysis of algorithm
   - Edge cases
   - Known unknowns

# Punctuation
As a guideline, insert a comma wherever a reader would naturally pause somewhere within a sentence.

## 练习
Add commas where appropriate to the following passage:
> Protocol Buffers sometimes known as protobufs are our team's main structured data format. Use Protocol Buffers to represent store and transfer structured data. Unlike XML Protocol Buffers are compiled. Consequently clients transmit Protocol Buffers efficiently which has led to rapid adoption.

Hint: Read the passage aloud and put a comma everywhere you hear a short pause.
> Protocol Buffers, sometimes known as protobufs, are our team's main structured data format. Use Protocol Buffers to represent, store, and transfer structured data. Unlike XML, Protocol Buffers are compiled. Consequently, clients transmit Protocol Buffers efficiently, which has led to rapid adoption.

avoid using a comma to paste together two independent thoughts:
> Not recommended: Samantha is a wonderful coder, she writes abundant tests.
> Recommended: Samantha is a wonderful coder. She writes abundant tests.


符号没看完，有空再看
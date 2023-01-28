# General error handling rules
- Don't fail silently
- implement the full error model
  找相应的error模型，比如谷歌官网对特定的error有特定的处理范本
- Avoid swallowing the root cause
    报错类型不要过大，比如Server error，类似的还有service failure, network connection drop, mismatching status, permission issues等。建议有细节内容
- Log the error codes
    数字的错误代码更容易帮助用户找到错误
- Raise errors immediately
越早raise损失越小

# Explain the problem
## Identify the error's cause
Tell users exactly what went wrong. Be **specific**— vague error messages frustrate users.
> **Not recommended**
Bad directory.
**Recommended**
The specified directory exists but is not writable. To add files to this directory, the directory must be writable. [Explanation of how to make this directory writable.]

> **Not recommended**
Invalid field 'picture'.
**Recommended**
The 'picture' field can only appear once on the command line; this command line contains the 'picture' field <N> times.
Note: Prior to version 2.1, you could specify the 'picture' field more than once, but more recent versions no longer support this.

## Identify the user's invalid inputs
If the error involves values that the user can enter or modify (for example, text, settings, command-line parameters), then the error message should identify the offending value(s).
如果是用户可以直接解决的错误，要告诉用户准确的错误值。
> **Not recommended**
Funds can only be transferred to an account in the same country.
**Recommended**
You can only transfer funds to an account within the same country. Sender account's country (UK) does not match the recipient account's country (Canada).

> **Not recommended**
Invalid postal code.
**Recommended**
The postal code for the US must consist of either five or nine digits. The specified postal code (4872953) contained seven digits.

If the invalid input is a very long value that spans many lines, consider doing one of the following:
Disclose the bad input progressively; that is, provide one or more clickable ellipses to enable users to control how much additional error information they want to see.(没有特别看懂，但是我觉得意思是如果特别长的话给多个可点击的按钮让用户选择到底哪部分要详细看)
Truncate the bad input, keeping only its essential parts.


## Specify requirements and constraints
Help users understand requirements and constraints. Be specific. Don't assume that users know the limitations of your system.

>**Not recommended**
The combined size of the attachments is too big.
**Recommended**
The combined size of the attachments (14MB) exceeds the allowed limit (10MB). [Details about possible solution.]

>**Not recommended**
Permission denied.
**Recommended**
Permission denied. Only users in <group name> have access. [Details about adding users to the group.]

>**Not recommended**
Time-out period exceeded.
**Recommended**
Time-out period (30s) exceeded. [Details about possible solution.]

**Explain how to fix the problem**
Create actionable error messages. That is, after explaining the cause of the problem, explain how to fix the problem.
> **Not recommended**
The client app on your device is no longer supported.
**Recommended**
The client app on your device is no longer supported. To update the client app, click the Update app button.

# Write clearly
## Be concise
Write concise error messages. Emphasize what's important. Cut unnecessary text. 
> **Not recommended**
Unable to establish connection to the SQL database. [Explanation of how to fix the issue.]
**Recommended**
Can't connect to the SQL database. [Explanation of how to fix the issue.]

>**Not recommended**
The resource was not found and cannot be differentiated. What you selected doesn't exist in the cluster. [Explanation of how to find valid resources in the cluster.]
**Recommended**
Resource <name> isn't in cluster <name>. [Explanation of how to find valid resources in the cluster.]

## Avoid double negatives 双重否定
A **double negative** is a sentence or phrase that contains two negative words, such as:
- not, including contractions like can't, won't
- no

Some double negatives in error messages are blatant:
> You cannot not invoke this flag.

*Other double negatives are more **subtle**.* For example, the words **prevents** and **forbidding** in the following error message are both negatives, leading to a confusing message:

>**Not recommended**
The universal read permission on pathname **prevents** the operating system from **forbidding** access.

>**Recommended**
The universal read permission on pathname **enables anyone** to read this file. Giving access to everyone is a security flaw. See hyperlink for details on how to restrict readers.

Similarly, avoid exceptions to exceptions.
> **Not recommended**
The App Engine service account must have permissions on the image, except the Storage Object Viewer role, unless the Storage Object Admin role is available.
**Recommended**
The App Engine service account must have one of the following roles:
> - Storage Object Admin
> - Storage Object Creator

##Write for the target audience
[同curse of knowledge](technical_writer_google.md#curse-of-knowledge)
For example, the following error message contains terminology appropriate for a target audience of ML experts. If the target audience includes a significant number of people who aren't ML experts, then the error message is mystifying:

> **Recommended for ML experts only**
Exploding gradient problem. To fix this problem, consider gradient clipping.

Now compare the following two error messages. The first error message contains technical truth, but terms like server, client, farm, and CPU are not going to help most consumers:
>**Inappropriate for shoppers**
A server dropped your client's request because the server farm is running at 92% CPU capacity. Retry in five minutes.

The second error message is more suitable (and comforting) for a non-technical audience:

>**Appropriate for shoppers**
So many people are shopping right now that our system can't complete your purchase. Don't worry--we won't lose your shopping cart. Please retry your purchase in five minutes.

## Use terminology consistently
Variety spices up paragraphs. However, variety in error messages can confuse users.
If you call something a "datastore" in one error message, then call the same thing a "datastore" in all the other error messages.

## Format error messages to enhance readability
### Link to more detailed documentation
> **Not recommended**
Post contains unsafe information.
**Recommended**
Post contains unsafe information. Learn more about safety at <link to documentation>.

### Use progressive disclosure
Some error messages are long, requiring a lot of text to explain the problem and solution. Unfortunately, users sometimes ignore long error messages, intimidated by the "**wall of text**." A good compromise is to <u>display a briefer version of the error message</u> and then give users the option to click something to get the full context.

>**Not recommended**
TextField widgets require a Material widget ancestor, but none were located. In material design, most widgets are conceptually “printed” on a sheet of material. To introduce a Material widget, either directly include one or use a widget that contains a material itself.
**Recommended**
TextField widgets require a Material widget ancestor, but none were located.
...(Click to see more.)

  In material design, most widgets are conceptually "printed" on a sheet of material. To introduce a Material widget, either directly include one or use a widget that contains a material itself.

### Place error messages close to the error
For coding errors, place error messages as close as possible to the place where the error occurred.
>**Not recommended**
1: program figure_1;
2: Grade = integer;
3: var
4: print("Hello")
Use ':' instead of '=' when declaring a variable.
**Recommended**
1: program figure_1;
2: Grade = integer; 
---------^ Syntax Error
Use ':' instead of '=' when declaring a variable.
3: var
4: print("Hello")

### Handle font colors carefully
一部分读者是色盲，谨慎使用颜色，使用的同时加粗或左右加空格，或下加^以区隔

## Set the right tone
The tone of your error messages can have a significant effect on how your users interpret them.

### Be positive
Instead of telling the user what they did wrong, tell the user how to get it right.

>**Not recommended**
You didn't enter a name.
**Recommended**
Enter a name.

>**Not recommended**
You entered an invalid postal code.
**Recommended**
Enter a valid postal code. [Explanation of valid postal code.]

>**Not recommended**
ANSI C++ forbids declaration 'ostream' with no type 'ostream'.
**Recommended**
ANSI C++ requires a type for declaration 'ostream' with type 'ostream'.

### Don't be overly apologetic
While maintaining positivity, <u>avoid the words "sorry" or "please."</u> Focus instead on clearly describing the problem and solution.
专注于解决问题，不要说抱歉，因为不同文化对于抱歉的理解不一样，在有些文化中，抱歉代表着较为严重的问题。
### Avoid humor
### Don't blame the user
If possible, focus the error message on what went wrong rather than assigning blame.
> **Not recommended**
You specified a printer that's offline.
**Recommended**
The specified printer is offline.
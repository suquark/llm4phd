# LLM for Phd

Examples and instructions about use LLMs (especially ChatGPT) for PhD. Will add more features gradually.
Feel feel to contribute to this project!

## Example 0: GPT-3.5 vs GPT-4

> ChatGPT, introduce yourself to CS PhD students briefly!

(GPT 3.5) Hello, I am ChatGPT, a large language model created by OpenAI based on the GPT-3 architecture. I am designed to understand and generate human-like language and I have been trained on a diverse set of texts, including books, articles, and websites. My goal is to provide helpful and informative responses to your questions to the best of my abilities.

(GPT-4) Hello **CS PhD students**! I am ChatGPT, a large-scale artificial intelligence language model developed by OpenAI, based on the GPT-4 architecture. My primary function is to understand and generate human-like text in response to a wide range of prompts. I can assist you with **research, programming, problem-solving, and many other aspects of your PhD journey**. My knowledge is up-to-date until September 2021, but I'm eager to help you explore and learn together. Feel free to ask any questions or seek guidance on your projects, and let's collaborate to advance your studies!

**Conclusion**: GPT-4 follows instructions much better than GPT-3.5. We will see more examples later.

## Example 1: Clarifying complex concepts with relatable examples

### Meme-like example

Q: please explain Quantum physics with taco examples

(GPT-4) Quantum physics is a branch of physics that studies the behavior of matter and energy at very small scales, such as atoms and subatomic particles. To explain quantum physics using taco examples, let's first assign some elements of a taco to different aspects of quantum physics:

Taco shell: Represents the boundary or the quantum system.
Taco fillings: Represents the particles within the quantum system.
Different combinations of fillings: Represents the different quantum states the particles can be in.
Now, let's explore a few key concepts in quantum physics using our taco analogy:

...

### Something you are familiar with, but you forget the details

Q1: explain why we need daemon process in linux, what's its usage

(GPT-4) In Linux, a daemon is a background process that runs without direct user interaction, typically performing specific tasks or services. Daemons are essential for various reasons and have multiple uses in a Linux system:

1. ...
2. ...

Q2: how to create a daemon process

(GPT-4) Creating a daemon process in Linux typically involves the following steps:

1. Fork the process: ...
2. Create a new session and process group: ...
3. Set the working directory: ...
4. Reset the file mode creation mask: ...
5. Close standard file descriptors: ...
6. Implement the daemon functionality: ...
7. Handle signals: ...

### Something you have little knowledge

Q1: please explain aws sts:AssumeRole

(GPT-3.5) AWS Security Token Service (STS) is a service that enables you to grant temporary access to AWS resources to users or applications that don't normally have access to them. One way to grant temporary access is by using the AssumeRole API.

...

(GPT-3.5) Q2: give me an example

Sure, here's an example of how the AssumeRole API can be used in AWS:

Let's say you have two AWS accounts, Account A and Account B. Account A has an S3 bucket that contains sensitive data, and you want to give a developer in Account B temporary access to that bucket for a specific project. However, you don't want to give the developer permanent access to the bucket.

...

(AWS documentation) Returns a set of temporary security credentials that you can use to access AWS resources. These temporary credentials consist of an access key ID, a secret access key, and a security token. Typically, you use AssumeRole within your account or for cross-account access. For a comparison of AssumeRole with other API operations that produce temporary credentials, see Requesting Temporary Security Credentials and Comparing the AWS STS API operations in the IAM User Guide.

Permissions

The temporary security credentials created by AssumeRole can be used to make API calls to any AWS service with the following exception: You cannot call the AWS STS GetFederationToken or GetSessionToken API operations.

**Conclusion**: 

1. I really do not expect ChatGPT would explain QM with tacos in a reasonable way. However, it did a good job, and I cannot be better than it (I am familiar with QM).
2. I know daemon process, but creating it is actually non-trivial, it is more than just forking and exit the parent process. ChatGPT explains the whole process end-to-end, which is super efficient and easy to understand.
3. AWS doc explains a concept with a lot more concepts, which makes me scratch my head. ChatGPT generates a much understandable answer with *approachable* words, and it generates an example that helps you understand the concept really well.


## Example 2: Effortlessly extracting keywords from casual conversations

Q1: What's the field of study about the initial job arrival distribution?

(GPT-3.5): (something about job market)

Q2: (context: computer science) What's the field of study about the initial job arrival distribution?

(GPT-3.5): The field of study that deals with the initial job arrival distribution in computer science is known as queuing theory. Queuing theory is the mathematical study of waiting lines, or queues, that arise in various real-world situations, including computer systems.

...

Q3: is there something called "arrival theory"?

(GPT-3.5): I am not aware of a field of study called "arrival theory" in computer science or related fields. However, the term "arrival process" is commonly used in queuing theory and related fields to refer to the pattern or distribution of job arrivals in a system.

The arrival process can be described by various statistical distributions, such as Poisson, exponential, or Weibull distributions. The characteristics of the arrival process, such as the mean arrival rate, variance, and autocorrelation, can significantly impact the performance of a queuing system.

...

Q4: explain "Weibull distributions" to me

(GPT-3.5): Weibull distribution is a continuous probability distribution widely used in reliability engineering to model the failure rates of systems over time. It is named after Waloddi Weibull, who first proposed this distribution in 1951.

The Weibull distribution has two parameters: the shape parameter, denoted by k, and the scale parameter, denoted by λ. The probability density function (PDF) of the Weibull distribution is given by:

f(x) = (k/λ) * (x/λ)^(k-1) * e^(-(x/λ)^k)

where x is the random variable and e is the base of the natural logarithm.

...

Q5: it sounds like gamma process

(GPT-3.5): (wrong answer, they are not related in the way that ChatGPT considered)


**Conclusion**: 

1. When ChatGPT fail to answer your question, simply add more context.
2. You ChatGPT can come up with the termilology from vauge descriptions. Google search actually also works sometimes.
3. However, you can keep the conversation with ChatGPT, and learn something new with this new termilology, w/o another search, so it is more convenient and consistent 
4. ChatGPT could give wrong answers. Here I can understand why (Q5). Both Weibull & Gamma distribution is related to a version which their paramaters are whole numbers. But this does not mean Weibull turns into Gamma distribution when its parameters are whole numbers. ChatGPT only find the correlation, but logically this is wrong.


## Example 3: Crafting stunning WebUI designs for the design-challenged

Here is how I design a web page template including a nice table for displaying data items, iteratively:

Q1: please generate an Jinja2 html template with a two-column table and basic styles

(GPT-3.5): Sure! Here's an example Jinja2 HTML template that creates a two-column table with some basic styling:

... (it is a page with 2 column, one table per column)

Q2: I only need a single table, but the table has two columns

(GPT-3.5): No problem! Here's an example Jinja2 HTML template that creates a single table with two columns:

... (nice)

Q3: add more fancy styles

(GPT-3.5): ...

Q4: further decorate the table header

(GPT-3.5): ...

Q5: add one column for the table

(GPT-3.5): ...

Q6: add a nag bar that returns to homepage with a "homepage" icon button in the nav bar

(GPT-3.5): ... (ChatGPT knows it is a "nav" bar, not "nag")

Q7: you missed the "fa-home" css class

(GPT-3.5): My apologies! You are correct. Here's the updated code snippet with the missing "fa-home" CSS class added:

...

**Conclusion**: 

So what's happening here?

From my observation most PhDs have no idea of how to design a web page from scratch. But they can understand the HTML and stylesheet etc.

ChatGPT can generate a web page from scratch, but often with some issues. So it is good to start with a simple design and improve it iteratively. Use instructions to alter the design or fix the bug.

However, you have to know what ChatGPT is capable of generating. In the end, it adds the missing "fa-home" CSS class (ref link to css script). It includes a SHA-sum of that script for web security. You should understand ChatGPT cannot get them correct under most of the cases, because these shasum are quite random and do not follow typical rules of natural language. I figured out the shasum manually, then this web page works.


## Example 4: Creating natural language-based interactive UIs for seamless project integration

What I do is writing a prompt for SkyPilot, a project I am working on:

-------

You will help the user using a commandline tool called SkyPilot. All topics are related to SkyPilot by default.
You should output the corresponding (do not include unnecessary or default arguments, and always display full argument name ("--" instead of "-")) commandline with SkyPilot according to user's demand.
Surround your output commandline like (with newlines before and after the block):

```
<commandline>
{your_output_commandline}
<commandline/>
```

Some background for you:

SkyPilot is a framework for easily and cost effectively running ML workloads1 on any cloud.

SkyPilot abstracts away the cloud infra burden:

* Launch jobs & clusters on any cloud (AWS, Azure, GCP, Lambda Cloud)
* Find scarce resources across zones/regions/clouds
* Queue jobs & use cloud object stores.

Here are some docs for SkyPilot commandline. You should follow them strictly and do not make up new options:

Usage: sky [OPTIONS] COMMAND [ARGS]...

Options:
  --install-shell-completion [bash|zsh|fish|auto]
                                  Install shell completion for the specified shell.
  --uninstall-shell-completion [bash|zsh|fish|auto]
                                  Uninstall shell completion for the specified shell.
  -v, --version                   Show the version and exit.
  -h, --help                      Show this message and exit.

... (more docs)


-------

Although this is very rough, this enables a NUI (natural language user interface) for Skypilot, which works pretty well.

Here is a real example with SkyPilot NUI:

Q1: hey, give me some cpus

(SkyPilot): To launch an interactive CPU node, you can use the `sky cpunode` command. Here's an example command to launch a default cpunode:

```
<commandline>
sky cpunode
<commandline/>
```

By default, this will launch a new cluster with an auto-generated name. If you want to name the cluster yourself, you can use the `-c` option followed by the name you want. For example:

```
<commandline>
sky cpunode -c my_cluster_name
<commandline/>
```

You can also specify the number of CPUs each instance must have by using the `--cpus` option followed by the number. For example:

```
<commandline>
sky cpunode --cpus=4
<commandline/>
```

This will launch an interactive node with 4 vCPUs.

Q2: use google cloud please

(SkyPilot): Sure. To launch an interactive CPU node on Google Cloud, you can specify `gcp` as the cloud provider using the `--cloud` option. Here's an example command to launch an interactive CPU node with 4 vCPUs on GCP:

```
<commandline>
sky cpunode --cloud gcp --cpus=4
<commandline/>
```

By default, this will launch a new cluster in the us-west1 region with an auto-generated name. You can specify a different region using the `--region` option followed by the region name, such as `us-central1`. For example:

```
<commandline>
sky cpunode --cloud gcp --cpus=4 --region us-central1
<commandline/>
```

If you want to name the cluster yourself, you can use the `-c` option followed by the name you want. For example:

```
<commandline>
sky cpunode --cloud gcp --cpus=4 --region us-central1 -c my_cluster_name
<commandline/>
```

**Conclusion**: It amazes my labmates & advisors.


## Example 5: Demystifying paper reviews during rebuttal to bolster student comprehension

Q1: Do not discuss the paper, but summarize the requirements (e.g., what is a good paper) of OSDI conference from these following reviewer comments:

(... reviewer comments)

(GPT-4): The OSDI conference requires a good paper to:

1. ...
2. ...


Q2: Which are the most vague requirements?

(GPT-4): The most vague requirements are:

1. Clearly present the requirements of the problem being addressed, such as ...
2. Provide concrete examples with ...
3. ...

Q3: Summarize the common points of reviewers' comments

(GPT-4): The common points in the reviewers' comments include:

1. The importance of the problem: Both reviewers recognize the significance of ...
2. Lack of clarity in the paper: Both reviewers mention that the paper lacks a clear and focused explanation of the problem and the proposed solution, and they suggest providing concrete examples and a more detailed ...
3. Evaluation concerns: The reviewers express concerns about the evaluation, mentioning the need for a focus on end-to-end ...
4. Novelty and implementation details: Both reviewers question the novelty of the proposed system and suggest providing more details on the implementation.
5. Paper structure and conclusion: Both reviewers mention that the paper's structure could be improved for better readability, and they point out the absence of ...

**Conclusion**: 

ChatGPT can summarize some high-level comments, but it will not be too useful about coming up with concrete suggestions for a solid rebuttal. However, after GPT-4 (32k context) comes out, we may be able to perform end-to-end rebuttal writing (paper + reviews -> detailed suggestions).

## Example 6: Elevating student paper-writing prowess and deepening understanding of academic literature

### Task 1: Sentence-level correction

Q: output a list of most poorly written sentences (logically inconsistent, grammar errors, vague, not connected well with previous sentence, etc.) when reading the introduction part of the paper until the end, and explain why for each of them, and also show the corrections:

(... paper introduction section)

(GPT-3.5) I'm sorry, but I cannot identify any poorly written sentences in this passage. The passage is well-written, clear, and coherent. It explains the tradeoffs between two popular categories of distributed execution engines and discusses the pros and cons of each. The author provides examples to illustrate their points and explains the benefits and drawbacks of each approach. The passage also uses technical language that is appropriate for the subject matter.

(GPT-4):

1. Poorly written sentence: "If each task ..."

Explanation: The phrasing "..." is grammatically incorrect and unclear. The intention is to say that the system guarantees ... by ensuring ...

Correction: "If each task ... " (add the missing word)

2. ...

### Task 2: Dive into the paper

Q1: output (1) an outline of concrete content that does not contain any logical structure (2) the key logical structure with only high-level concepts when reading the introduction part of the paper until you reach the end. also leave comments for both of them:

(... paper introduction section)

(GPT-4): 

1. Outline of concrete content without logical structure:

* ... examples: ...
* Problem: ...
* Solution: ...
* Layered architecture: ...
* ...

2. Key logical structure with high-level concepts:

1. (... story)
2. Key insight: ...
3. Solution: design a ...
4. Demonstrate the utility of ...

Comments:

1. The outline without logical structure is a useful summary of the content, but it is difficult to understand the main argument and flow of ideas without the logical connections between the concepts.

2. The key logical structure with high-level concepts provides a clear and concise understanding of the main argument and ideas presented in the introduction. This structure helps to guide the reader through the content and demonstrates the importance and utility of the proposed solution.

Q2: try to optimize the previous logical structure (you are feel to change the order, remove items or add new items), and explain what's the difference between two structures and why

(GPT-4): Optimized key logical structure with high-level concepts:

...

Explanation of differences:

The original logical structure provided a clear understanding of the main argument and ideas. However, the optimized version further refines the structure to improve readability and coherence.

1. The order of concepts has been adjusted to create a more natural flow of ideas. ...
2. The optimized structure reduces redundancy by merging related concepts. For example, the original structure had separate points for the challenge of composing applications and the problem of ... The optimized version combines these concepts into a single point, highlighting the challenge of guaranteeing ...
3. The optimized structure emphasizes the key insight and proposed solution more clearly, helping the reader to understand the importance of the ... 

Overall, the optimized logical structure is more concise and coherent, which helps the reader to better grasp the main argument and ideas presented in the introduction.

Q3: compose a new introduction section, based on the optimized logical structure and including ALL concrete content in the concrete content outline.

(GPT-4)

Introduction: (...)


**Conclusion**: 

Quite useful.

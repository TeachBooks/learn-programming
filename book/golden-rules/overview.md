(golden-rules)=
# The Golden Rules

The Golden Rules are a (simple!) set of guidelines to help you build good habits into your programming routines. Here is an overview:

1. {ref}`Use descriptive names <golden-rules-descriptive-names>`
2. {ref}`Make readable code <golden-rules-readable-code>`
3. {ref}`Make readable results <golden-rules-readable-results>`
4. {ref}`Write simple functions, then use them <golden-rules-functions>`
5. {ref}`Document your code <golden-rules-document-code>`
6. {ref}`Test your code <golden-rules-test-code>`
7. {ref}`Learn to collaborate <golden-rules-collaborate>`

The following sections below will provide explanations and examples of each Golden Rule, but first we provide some context.

```{tip}
    
Whether you are a student, teacher or practitioner, we encourage you to **refer back to this document often.** The Golden Rules are something that is best when digested repeatedly over a long period of time; try to refer back while you are programming and add new tricks to your programming toolbox and workflow incrementally over time.

In addition, we will periodically update the examples and topics, so next time you visit, there may be new material!
```

**Why do the Golden Rules for Documentation and Communication exist?**

In your coursework or professional life you may find yourself spending a lot of time writing, reading and debugging code, regardless of your prior programming experience. Your time is valuable, especially once you start working after graduation! Yet it is all too common that most code is never re-used because it is poorly **documented**, making it not understandable to others, or even to yourself at a later moment. In addition, as a young practicing engineer or researcher it is critical that you are able to use your code to effectively **communicate** your results, otherwise the effort put into your analysis is wasted. Good code writing, code documentation and presentation of results such as figures, tables and numbers are all essential for effective collaboration. Even when working individually, it is important to preserve your work such that you can easily understand and re-use in the future. This document will provide and explain a number of recommendations to help you accomplish that.

The following quote summarizes the philosophy of this document concisely:

<div style="text-align: right"><em>Any fool can write code that a computer can understand. Good programmers write code that humans can understand.</em></div>  
<div style="text-align: right"><em> ― Martin Fowler </em></div> 

**A note of Encouragement**

This following pages contain a lot of information that might not appear to be useful to you...*yet*. As a student, keep in mind that the content here was created in collaboration with many colleagues who are working in industry and will be looking to hire you after you graduate from university: they will appreciate good coding documentation and communication skills! As teachers, our primary advice (for the entire duration of your degree program, not only this course!) is that you take a look at this material now, but also keep the Golden Rules in mind and refer back to them often. If you can incorporate them into your work now, you will have made good habits for yourself that we know will serve you well in the future.  

We focused on illustrating good programming practices in a format and language that is approachable to engineers with a varied programming background. As such, specific fundamental programming and computer science concepts are avoided. If you would like to learn more about theses concepts, specifically related to Python, the textbook by Guttag (2021) listed below is an excellent reference.

## Documentation and Communication

The words in the title of this lesson were chosen very carefully. *Documentation* refers to all the work related to a problem you are working on. In your programming work, documentation is not limited to describing the purpose and function of your code only. Clearly documented code is important, but in CEG it is also critical to describe all the steps in your analysis, for example: data and data sources, assumptions, results, discussion and recommendations. Jupyter notebooks provide a fantastic platform for combining documentation and analysis in one file, which is why we rely on them heavily in our courses. However, remember there are many other options available to you for proper documentation of your work, and the topics we cover here always apply. 

*Communication* refers to how you use your code, the analysis you run and the format by which you share it. Rarely are you running a piece of code purely for yourself, but often to share with others---perhaps for a homework assignment, to include in a thesis, a scientific publication, a design at a consultancy, et cetera. Why go through all the trouble of writing and using code if no one can understand what you did with it? It may be clear to you right now, but what if someone wants to use it in the future, or ask about your results, when you are not there? Will the audience understand your work if you have unreadable or overly complex tables and figures in a MSc thesis or conference presentation? Good communication is therefore critical, and there are many aspects, for example: visual formatting (visual appearance of code, text output, figures, tables); transparency and understandability (what did you do? is it repeatable? will someone understand it in the future, perhaps out of context?); and, for code explicitly: readability. This lesson provides a number of useful guidelines that will help your communication improve.

In summary, the title of this document is a bit simplistic. In reality, it should be: *the Golden Rules: a non-exhaustive list of highly recommended habits to build into your life to make sure you can easily and consistently document your work in a way that ensures effective communication with others, as well as your future self.* But that doesn’t roll off the tongue like our current title does. And it doesn’t fit in 79 characters either 😉.

## Next Steps

Hopefully the explanation above makes you understand why it is important to consider documentation and communication in your work. Before we describe the Golden Rules, we need to introduce something that initially may seem like it belongs in a Computer Science course. However, we will see that it contains a number of useful guidelines and insight into how one can write readable Python code: the PEP 8 Style Guide.

### Additional Resources

If you would like more information, we collected a few resources here. The first textbook is oriented on Python programming, whereas the second and third are more generic and focus on the broader scope of software projects.

Guttag, J. V. (2021). *Introduction to Computation and Programming Using Python: With Application to Computational Modeling and Understanding Data.* MIT Press.

The [Good Research Code Handbook](https://goodresearch.dev/index.html)

The [Turing Way Handbook](https://book.the-turing-way.org/index.html)

And of course don't forget to bookmark this page!

[PEP 8 - Style Guide for Python code](https://peps.python.org/pep-0008/)

### Feedback

The Golden Rules were originally written by Robert Lanzafame and Kiril Vasilev in 2022, with the generous support of many colleagues who provided feedback and ideas; especially the quotes the start of each Rule!

We also greatly appreciate feedback, and are always looking for more examples of good (and bad) practices! You can contact Robert Lanzafame at R.C.Lanzafame@tudelft.nl, or creating an Issue, Discussion or Pull Request via the GitHub Repository (use the button at the top right or visit the repository where these files live [github.com/teachBooks/learn-programming/](https://github.com/teachBooks/learn-programming/)).

---

_The primary authors for this chapter are Robert Lanzafame and Kiril Vasilev._

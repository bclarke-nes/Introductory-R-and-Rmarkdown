![](img/header.png) Introductory R and Rmarkdown
================
Brendan Clarke
2023-04-17

# Archived

This repository is now archived. Please see the current version at [https://github.com/NES-DEW/Introductory-R-and-Rmarkdown](https://github.com/NES-DEW/Introductory-R-and-Rmarkdown)



## Introduction

This is an introductory [R](https://www.r-project.org/) and [Rmarkdown](http://rmarkdown.rstudio.com) training course using [Posit Cloud](https://rstudio.cloud). It runs as a series of four interactive sessions, and is designed for those without previous programming experience working in health, care, and housing across Scotland. 

It is intended as a starting point for automating your report writing processes, with the aim of replacing, enhancing, or simplifying, manual report writing. The training also covers ways of producing reports in a variety of formats including .pdf, .docx (Word format), and .html (webpage).

Some examples of routine reports that might be targets for re-working in a dynamic format:

- service-use reports (admission figures, bed utilisation)
- annual reports (public health annual reports)
- engagement and impact data (training, outreach)

### Who is this training for?

This training is intended for someone who:

- is currently spending lots of time manually updating reports in
  health, care, or housing
- **and** would like to reduce the time spent on this routine work over
  the medium-term (months)
- **and** has some time to spend reworking this report-writing process
- **and** are open to gaining some basic programming experience

### What this training is not

- it’s not a full introduction to working in
  [R](https://www.r-project.org/)/[Rmarkdown](http://rmarkdown.rstudio.com).
  [R](https://www.r-project.org/) is deep (like most analytic
  platforms), and this training covers only a little bit of the
  available functionality
- it’s not an introduction to everything that you might like to do with
  a data-driven report either. Instead, it covers some simple examples
  of common tasks as a way of familiarising you with a different
  workflow
- it’s definitely not a production-ready replacement for your existing
  reports. It’s a learning resource, rather than a pre-packed
  replacement
- it won’t teach you how to make real-time dashboards. If you need your
  report to update more than about once a day, you should consider
  building a dashboard instead ([Power
  BI](https://powerbi.microsoft.com/en-gb/),
  [R](https://www.r-project.org/)/[Shiny](https://shiny.rstudio.com/),
  or [Dash](https://plotly.com/dash/))

## About dynamic reports

### Is it worth it for me?

<img src="img/error.png" width="500px" />

A recent personal example of a copy and paste error encountered while
writing a short report. This would have been avoided with a dynamic
report.

Ultimately, it’s for you to decide whether automating your report will
be worth the investment of time. But to help you come to a decision,
here are some of the strengths and weaknesses of dynamic reports
compared to traditionally-produced static reports:

#### Strengths

- **fidelity**. A dynamic report means no manual updating of text,
  graphs, and figures. No more copy and paste problems (see the Teams
  chat message above).
- **standardisation**. If you have lots of similar reports to write,
  this dynamic approach simplifies the process of making your reports
  look alike by applying a standard approach to formatting, analysis,
  and so on. This is a huge time-saver, and is especially true if you
  have lots of graphs and tables to produce.
- **reproducibility**. If someone else looks at the source code for your
  report, they can see exactly how your figures are produced. That means
  that, when it’s time to hand over production of your report to a
  colleague, you won’t need to explain how to build the report. It’s all
  contained in the source-code.
- **efficiency**. Again assuming that everything works properly,
  updating a dynamic report with new data should be much quicker than
  updating a comparable report by hand.

#### Weaknesses

- **set-up cost**. Particularly if you are new to this kind of work,
  writing a new dynamic report takes much longer than a traditional
  report. There’s plenty to learn, and it can be hard to find the time
  to learn, and to rework an established process.
- **errors**. While dynamic reports are a great way of avoiding minor
  errors from copying and pasting, they can introduce entirely new
  sources of error from reworking your analysis. Reports, particularly
  early on, need frequent careful checking to ensure that you haven’t
  swapped small frequent errors for large, subtle ones.
- **Information Governance and data protection concerns** about the
  platforms used to write these kinds of reports.
- **novelty**. Changing processes is often controversial, with a degree
  of resistance. For example, there’s a strong lock-in to the Microsoft
  Office suite (Word and Excel especially) for report writing.
  Suggesting something new can be daunting. Change management and QI
  methods might be helpful if you think this is likely to be a
  substantial concern for your project.

On balance dynamic reports have more advantages than disadvantages. But
decisions about whether to automate a report will depend on the local
factors in play. It might be useful to have a think about how dynamic
report writing might fit into your work before the training session
too - and discuss them with your colleagues.

## Getting started

### How does it work

We’ll use three tools to write the report. First, we’ll use the web
service [Posit Cloud](https://rstudio.cloud). This allows us to run
[R](https://www.r-project.org/) without installing any software or
making any changes to our computer. Next, we’ll use the markup language
[Rmarkdown](http://rmarkdown.rstudio.com) to add some text and images to
our report. Finally, we’ll use the [R](https://www.r-project.org/)
programming language to do some simple data handling, analysis, and
visualisation.

Just in case you’d like to look into how these tools work in advance of
the session, we would recommend:

- a quick [introduction to Posit (RStudio) Cloud from R
  bloggers](https://www.r-bloggers.com/2022/02/rstudio-cloud-how-to-get-started-for-free/)
- [Rstudio’s quick tour of
  Rmarkdown](https://rmarkdown.rstudio.com/authoring_quick_tour.html) is
  a great place to start if R and RMarkdown is completely new to you
- If you’re already somewhat familiar with working in
  [R](https://www.r-project.org/), you might prefer to start with the
  [Rmarkdown chapter in the *R for Data Science*
  book](https://r4ds.had.co.nz/r-markdown.html)

[Posit Cloud](https://rstudio.cloud) is easy to set-up and free for
small-scale work like this demo. This makes it by far the easiest way to
get going from scratch if you’ve never worked with
[R](https://www.r-project.org/) before. Note that because it’s a web
service, it requires you to upload your data to their servers, which
might makes it unsuitable for production work in health and care owing
to information governance concerns. That said, it’s easy to transfer
projects from [Posit Cloud](https://rstudio.cloud) to an installed
version of [R](https://www.r-project.org/), so don’t worry that what you
learn here will be tied to the cloud forever.

One important tip: this is a learning resource, and you’ll need time to
think about it, play around with it, and reflect on how it might inform
your work. Don’t try to use this training to change your way of writing
reports under pressure. There’s quite a lot to think about here, and you
might need to spend a good bit of time working out how to adapt this
demonstration to fit your report. Think of this as the start of a
journey, rather than a destination.

### What you’ll need

As Posit Cloud is a web service, you don’t need a particularly
up-to-date computer to completed this training. As long as you have a
reliable internet connection, and are capable of making a video call
with Microsoft Teams (for the face-to-face part of the training), then
you should be fine. The demonstration has been tested on Windows 10,
Windows 11, and Ubuntu Linux 21.04 without platform-specific
difficulties.

It is **extremely** helpful, although not essential, to have a multi-monitor
setup. That way you can run the demonstration in one screen, and the
Teams call on the other.

### Joining instructions

You’ll need to do a little bit of preparation before the first training
session, which should take about 15 minutes to complete. Please make
sure you have completed this before the start of the first session so
that we can make a prompt start. If you’re new to [Posit
Cloud](https://rstudio.cloud), please follow the step-by-step
instructions below. If you’ve worked with Posit Cloud before, you can
just sign-in to your account at [Posit Cloud](https://rstudio.cloud/),
create a new project from the [GitHub Repository at
https://github.com/bclarke-nes/Introductory-R-and-Rmarkdown](https://github.com/bclarke-nes/Introductory-R-and-Rmarkdown),
and then open the `demo.Rmd` file from the file pane.

#### Step-by-step instructions

1.  Go to <https://rstudio.cloud/> to access Posit Cloud

2.  If you have an account, you can log in as normal. Otherwise, please
    create a new account by selecting `Get started for free`, following
    the steps, and then signing-in

<img src="img/rsc_create.png" width="200px" style="display: block; margin: auto;" />

Several users have reported difficulties completing this account
creation process, particularly if they use a VPN. A quick workaround is to create the account from your
phone (or other non-NHS device). You can then log-in using your new
credentials from your NHS computer.

3.  Once you’ve signed-in to Posit Cloud, add a new project by clicking
    `New Project >> New Project from a Git repository`.

When prompted, enter the URL
`https://github.com/bclarke-nes/Introductory-R-and-Rmarkdown`

If you’ve never used GitHub before, you can think of it as a website
where programmers can store code. All we’re doing in this step is
creating a copy of the training files in your Posit Cloud account. If
you’d like to learn more about GitHub, we recommend [this brief and
non-technical
introduction](https://unito.io/blog/guide-to-github-for-project-managers/).

<img src="img/proj.png" width="200px" style="display: block; margin: auto;" />

4.  That will give you a new project containing the files needed for
    this demonstration:

<img src="img/screen.png" width="500px" style="display: block; margin: auto;" />

Don’t worry if this first sight of the the [Posit
Cloud](https://rstudio.cloud) interface is a shock. There’s an awful lot
happening here, and most of the apparent complexity is just information
overload! We’ll start adapting the interface to be more friendly at the
start of the first interactive session.

5.  Open the `session_01_introduction.Rmd` file from the Files pane in
    the bottom right-hand corner by clicking on its name

<img src="img/load.png" width="400px" style="display: block; margin: auto;" />

That’s it - you’re ready for the first session.

## Aims and objectives

This session will:

- Give an introduction to why we should write dynamic reports
- What kinds of report are most suitable to automate
- Give a basic overview of
  [R](https://www.r-project.org/)/[Rmarkdown](http://rmarkdown.rstudio.com)/[Posit
  Cloud](https://rstudio.cloud), including basic data handling, simple
  data analysis, and drawing graphs
- Show how these functions can be integrated into a simple report format
  that will update as the underlying data changes

By the end of this session, the user should:

- Have gained a basic understanding of [R](https://www.r-project.org/),
  and how [Posit Cloud](https://rstudio.cloud) and
  [Rmarkdown](http://rmarkdown.rstudio.com) can be used to generate
  reports
- Be familiar with the advantages and disadvantages of working in this
  way compared to traditional manual report writing in Word and Excel
- Be able to confidently navigate the parts of an
  [Rmarkdown](http://rmarkdown.rstudio.com) document
- Be able to recognise some simple [R](https://www.r-project.org/) code,
  and with suitable assistance interpret it
- Be able to seek suitable help for their R code needs
- Produce and tweak simple descriptive statistical measures, and simple
  visualisations in [R](https://www.r-project.org/)
- Be confident adding dynamic text elements to an
  [Rmarkdown](http://rmarkdown.rstudio.com) document

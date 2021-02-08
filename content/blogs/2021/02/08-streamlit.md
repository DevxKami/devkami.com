---
title: "My experiment with Streamlit"
date: 2021-02-08
tags: ["data science", "streamlit", "python"]
image: https://res.cloudinary.com/dty81dwqf/image/upload/c_scale,w_577/v1612762752/Screenshot_from_2021-02-08_13-37-52_batvfu.png
author: sweemeng
---
![](https://res.cloudinary.com/dty81dwqf/image/upload/c_scale,w_577/v1612762752/Screenshot_from_2021-02-08_13-37-52_batvfu.png)

Not too long ago I created a survey for Malaysian Software Developers about their tools and practices. The detail can be found [here]({{<ref "blogs/2021/02/08-job-survey.md">}}).

To present the data, I decided to use a tool called [Streamlit](https://www.streamlit.io/). Streamlit is an open source tools based on Python to build data applications. It provides ways to build widgets to manipulate and present data, and present it as a web application. It does it with only python. For R user, similar tools already exist it is called [Shiny](https://shiny.rstudio.com/)

To start, you need to install `streamlit`, and of course to be useful you also need other libraries like `pandas`, `matplotlib` etc. 

`pip install streamlit`

To run you need to create a python file, in this case I use `app.py`. Here’s a simple example. What this does is it will display a header and chart of selected data.

```python
import streamlit as st
import matplotlib.pyplot as plt


def generate_hbar_subplot(x, y, xlabel, ylabel, title, ax):
    x_pos = [i for i, _ in enumerate(x)]
    ax.barh(x_pos, y)
    ax.set(xlabel=xlabel)
    ax.set(ylabel=ylabel)
    ax.set_yticks(x_pos)
    ax.set_yticklabels(x)
    ax.set_title(title)


st.header("General stats")
fig, ax = plt.subplots()
generate_hbar_subplot(['cars', 'dolls', 'dinosaur'], [10, 20, 30], 'Number of Toys', 'Toys', 'Toys Collection', ax)
st.pyplot(fig)
```

Then you run the command `streamlit run app.py`. Open the url http://localhost:8501, you will then see results will look like below. 

![](https://res.cloudinary.com/dty81dwqf/image/upload/c_scale,w_708/v1612768920/Screenshot_from_2021-02-08_15-21-08_spg0ts.png)

You may also add interaction to this app, so you can use this to add filters to your pandas data frame for example. You can refer to the [documentation](https://docs.streamlit.io/en/stable/). 

To share the app you have 2 choices. One is to do a request to https://share.streamlit.io/. As long your code is on github you can host up to three Streamlit apps on the site. You also can set up a reverse proxy on a server in public, the guide to set up a reverse proxy is beyond the scope of the article.

What is good about Streamlit is that you can easily build data applications using only python. You can add interactivity and all sorts of widgets for display purposes. It supports most python libraries. The only complaint I have is that everytime you change the display with the widgets, you trigger a full page refresh.   

The example application that we build can be found [here](https://share.streamlit.io/sweemeng/devkami_dev_survey_streamlit/main/application_explorer.py). The source code is in [github](https://github.com/sweemeng/devkami_dev_survey_streamlit), I even prepare a Dockerfile to make it easier for you to run it locally. 

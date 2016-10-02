---
layout: post
title: Set up Jupyter Notebook and Run IPython on Ubuntu 16.04 server
---

Steps
---

### Install Ipython and Ipython-notebook on server

{% highlight python %}
pip install ipython
pip install "ipython[notebook]"
{% endhighlight %}

### Run Jupyter Notebook on server

{% highlight python %}
jupyter notebook
{% endhighlight %}

**Ignore the error saying no JavaScript.**

### Connect Server Using SSH Tunneling

{% highlight python %}
ssh -L 8000:localhost:8888 your_server_username@your_server_ip
{% endhighlight %}


### Open web browser on local machine


{% highlight python %}
http://localhost:8000
{% endhighlight %}




Reference
---

1. [How To Set Up a Jupyter Notebook to Run IPython on Ubuntu 16.04](https://www.digitalocean.com/community/tutorials/how-to-set-up-a-jupyter-notebook-to-run-ipython-on-ubuntu-16-04)
2. [IPython Tutorial](http://cs231n.github.io/ipython-tutorial/)
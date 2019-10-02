author: Horacio Tapia-McClung
summary: PAAII Description
id: paaii-workshop-micai2019
categories: codelab,markdown
environments: Web
status: Draft
feedback link: https://github.com/Mrc0113/codelab-4-codelab

# Predictive Analytics and Artificial Intelligence for the Industry 4.0 Workshop (with Python)

## Workshop Announcement
Duration: 0:01:00

![image_caption](img/codelabexample.png)

As part of the local activities around the Mexican International Conference MICAI 2019, the *Centro de Investigación en Inteligencia Artificial, CIIA*, of the *Universidad Veracruzana, UV*, announces the **Predictive Analytics and Artificial Intelligence for the Industry 4.0 Workshop (with Python)**.

The workshop is developed in the frame of the Data Challenge Industrial 4.0 event that will take place in the CIIA on the 26<sup>th</sup> and 27<sup>th</sup>sup> of october, 2019, and is prepared and imparted jointly by Dr. Horacio Tapia-McClung (CIIA) and Dr. Gibran Etcheverry Dodger (UDLAP) on <p>Tuesday october 29th 2019 </p>. If you are interested, please use the button below to register. We would be very pleased to see you there.





## Workshop Overview
Duration: 0:02:00

Analytics is revolutionizing our every day lives. From consumer electronics, smartphones, smart appliances, smart cars, etc., to new bussines models, Netflix, Uber, Aribnb, etc., many if not all these comodities are powered by a large and increasing number of new methods, tools and technologies.

Something similar is slowly happening across industrial sectors, but in a data-driven world, industrial data analytics is still far from the innovations we have experienced in the past two decades.

In Mexico these changes occur at a slower rate than in other places around the world like Germany, the U.S., Japan, etc. Nevertheless, data analytics in industrial settings will be crucial in the next 5 years as discussions and initiatives on the Industrial Internet of Things and 'Industria 4.0' are become a reality in the country.

This workshop is intended to present some examples of Predictive Analytics and Artificial Intelligence computational methods applied to concrete problems that often occur accross diverse industry sectors, using the Python programming language. The selected cases are: 
1. Predicting failure in equipment using sensor data;
2. Predicting Time To Failure or Remaining Useful Life, and
3. Chan chan chan chan

In this workshop we will use the Python programming language using Google's [Colaboratory](https://colab.research.google.com/) free Jupyter notebook environment. We are going to assume familiarity with the Python programming language although no strict previous experience with is required. 

The 
Here is an example image of another CodeLab that I created:
![image_caption](img/codelabexample.png)


**Resources:** 
* This codelab's original home is located here: [Link to Codelab](https://www.marcd.dev/codelab-4-codelab)
* The markdown for the original codelab is located here: [codelab.md](https://github.com/Mrc0113/codelab-4-codelab/blob/master/codelab.md)
* [Google CodeLabs Tools Github](https://github.com/googlecodelabs/tools) - The repo that contains the claat tool we'll be using today
* [Google Group for CodeLab Authors](https://groups.google.com/forum/#!forum/codelab-authors) - great forum for asking questions about codelabs and discussing future functionality
* [A blog that I used when getting started with Google Codelabs](https://medium.com/@mariopce/tutorial-how-to-make-tutorials-using-google-code-labs-gangdam-style-d62b35476816)

## Environment Setup
Duration: 0:04:00

In order to create a CodeLab you need *Go* and *claat* (the codelabs command line tool) installed.

The instructions below are what worked for me on Mac, but you can also find instructions [here](https://github.com/googlecodelabs/tools/tree/master/claat) 

#### Install Go 

Install [Go](https://golang.org/dl/) if you don't have it.
You can use Homebrew if you have it on mac 
``` bash
$ brew install go
```

#### Setup Go Environment Variables
Below is what I set on mac, but instructions are [here](https://golang.org/doc/install) for other OS options

``` bash
$ export GOPATH=$HOME/Go
$ export GOROOT=/usr/local/opt/go/libexec
$ export PATH=$PATH:$GOPATH/bin
$ export PATH=$PATH:$GOROOT/bin
```

#### Install claat
Install claat
``` bash
$ go get -u -v -x github.com/googlecodelabs/tools/claat
```

You should now have the *claat* command available to you. 
``` bash
$ claat
```

## Create your initial CodeLab
Duration: 0:05:00

Now that we have the environment setup let's go ahead and create a markdown file where we'll create the actual codelab. 

Negative
: If you're using Windows make sure to set your text editor to use UNIX line endings! 

####
``` bash
$ vim codelab.md
```

#### Fill-in the header metadata
Copy and paste the headers below into your markdown file and change the values appropriately. 
Guidelines are available below the sample headers. 

``` bash
author: Author Name
summary: Summary of your codelab that is human readable
id: unique-codelab-identifier
categories: codelab,markdown
environments: Web
status: Published
feedback link: A link where users can go to provide feedback (Maybe the git repo)
analytics account: Google Analytics ID
```

Metadata consists of key-value pairs of the form "key: value". Keys cannot
contain colons, and separate metadata fields must be separated by blank lines.
At present, values must all be on one line. All metadata must come before the
title. Any arbitrary keys and values may be used; however, only the following
will be understood by the renderer:

* Summary: A human-readable summary of the codelab. Defaults to blank.
* Id: An identifier composed of lowercase letters ideally describing the
  content of the codelab. This field should be unique among
  codelabs.
* Categories: A comma-separated list of the topics the codelab covers.
* Environments: A list of environments the codelab should be discoverable in.
  Codelabs marked "Web" will be visible at the codelabs index. Codelabs marked
  "Kiosk" will only be available at codelabs kiosks, which have special
  equipment attached.
* Status: The publication status of the codelab. Valid values are:
  - Draft: Codelab is not finished.
  - Published: Codelab is finished and visible.
  - Deprecated: Codelab is considered stale and should not be widely advertised.
  - Hidden: Codelab is not shown in index.
* Feedback Link: A link to send users to if they wish to leave feedback on the
  codelab.
* Analytics Account: A Google Analytics ID to include with all codelab pages.

#### Add the Title
Next add your title using a single '#' character
```
# Title of codelab
```

#### Add Sections and Durations
Then for each section use Header 2 or '##' and specify an optional duration beneath for time remaining calculations
Optional section times will be used to automatically total and remaining tutorial times
In markdown I've found that the time is formatted hh:mm:ss

Example
``` bash
## Section 1
Duration: 0:10:00

## Section 2
Duration: 0:05:00
```

#### Add Section Content
Now that we have 2 sections to our titled codelab let's go ahead and add some content to each section. 
Make up your own or copy and paste the example below: 

Copy into section 1 (Below Duration and above Section 2):
```
### Info Boxes
Plain Text followed by green and yellow info boxes 

Negative
: This will appear in a yellow info box.

Positive
: This will appear in a green info box.

You created info boxes!

### Bullets
Plain Text followed by bullets
* Hello
* CodeLab
* World

You created bullets!

### Numbered List
1. List
1. Using
1. Numbers

You created a numbered list!

```

Copy into section 2 (Below Duration): 
```
### Add a Link
Adding a link!
[Example of a Link](https://www.google.com)

### Add an Image
Adding an image!
![image_caption](https://googlecloud.tips/img/031/codelabs.png)

### Embed an iframe
![https://codepen.io/tzoght/embed/yRNZaP](https://en.wikipedia.org/wiki/File:Example.jpg "Try Me Publisher")
```

More Markdown Parser examples can be found [here](https://github.com/googlecodelabs/tools/tree/master/claat/parser/md).

## Export and Serve
Duration: 0:02:00

Now that you have an initial codelab defined in your markdown file let's go ahead and generate the static site content. 
We can export and serve the content locally using the `claat` command that we installed earlier. 

``` bash
$ claat export codelab.md
$ claat serve
```

* Your browser should have opened (if it doesn't then try going to localhost:9090 in your browser). 
* Choose the directory that matches your "id" that you put in the headers. 
* Viola! You should have your first codelab!

## Host Your CodeLab
Duration: 0:01:00

When you ran the `claat export` command you created the static web content needed to host your codelab. 
It placed static web content in a directory specified by your unique "id" and you can view it locally by opening the index.html page. 

Negative
: Note that when you view it locally by opening index.html some of the graphics may not show up (such as access_time, Next, Back), but they work once online. 


Now that you have the static content you can host it however you want.
One option is pushing it to github and serving it up from Netlify.  

If you'd like to create your own landing page for codelabs, [like this one](https://codelabs.developers.google.com), there is a tool to do that as well! 
Check it out here: [CodeLabs Site](https://github.com/googlecodelabs/tools/blob/master/site/README.md)
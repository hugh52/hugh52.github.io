# **NOTE** #

----------------------------------------------------------------------------------------------------

Below there is a link to the actual GitHub website that hosts this project and all of the code
(along with the'README.md' on this site) that goes along with it. Please keep in mind it is far
from finished, but at the same time not meant to be as serious of a project as the documentation, 
testing, etc. would lead many to think; instead, it is just a couple of simple scripts that are
being used to help simulate how a full-scale GitHub project might look, at least to some extent.<br>

[click here for actual GitHub project](https://github.com/hugh52/mods)

----------------------------------------------------------------------------------------------------

# **README** #

----------------------------------------------------------------------------------------------------

## **TODO** ##

----------------------------------------------------------------------------------------------------

- [ ] make actual separate 'TODO.txt' or 'TODO.md' file to remove this from 'README'
- [ ] include installation instructions with 'README' (add after adding PyPI, conda ability)
- [ ] add 'setup.py' and 'make' files (and any others) needed for installation after download 
- [ ] create documentation, most likely using Sphinx
- [ ] run all available tests
- [ ] install and setup everything necessary for continuous integration and testing
- [ ] commit/push data directory with sample files for examples
- [ ] provide screenshot showing the version printouts and include 'requirements.txt' explanation 
- [ ] add explanation concerning 'beautifulsoup4' or 'bs4' download, installation, and import
- [ ] add explanation of 're' and 'requests' download, install, and imports (now included with py)
- [ ] update and add to '.gitignore' file to include all defaults and essential exclude files
- [ ] build and commit/push new scripts with easier capabilities for user to choose or input py
        version, architecture, path(s), files, etc. through GUI or pop-up type interface, instead of
        having to alter actual code
- [ ] eventually put scripts into function or class format to simplify use, etc.
- [ ] add '__init__.py' files to enable import ability (to allow for use with older py versions) 
- [ ] register to 'PyPI', with all scripts bundled, to enable 'pip install' ability
- [ ] use 'conda_build', with all scripts bundled, to enable 'conda install' ability
    
----------------------------------------------------------------------------------------------------
    
## **Installation** ##

----------------------------------------------------------------------------------------------------

----------------------------------------------------------------------------------------------------

## **General Explanation** ##

----------------------------------------------------------------------------------------------------

The purposes behind these scripts are overly simplistic and will surely not apply to many people,
if anyone else at all. Additionally, there are surely multiple other, even easier and more
efficient, methods to accomplish the same goals (some of which I mention near the bottom). 
Nevertheless, I figured this would be at the very least a good exercise for me and at the most 
could help someone out that happens to stumble along this page, even if it just provides
them with a way to fix a recent syntax or other problem they have been facing with their code.
With that being said, below are two brief explanations of these scripts:

   pkg_scraper.py and pkg_scraper_eff.py
   * pull information from a website (in this case python package names), do some formatting to the
    information, then output that info to file on the user's computer for later use.
    
   pkg_names.py and pkg_names_eff.py
   * given a list of information (in this case python packages with version constraints) in a file
    on the user's computer, again apply some formatting to the info (in the form of regular 
    expressions), in order to again output the information to a file on the user's computer.
     

## **Differences and Similarities** ##

----------------------------------------------------------------------------------------------------

While these two scripts might sound the same to some people, and to a great extent they are similar,
once reviewing the code or actually running the examples, it should become clear that they are 
actually different, or at the very least different ways of arriving at very similar conclusions.
They can actually work together in certain situations, and could definitely be merged into one 
larger script to complete all the tasks at once, but only if the data meet the criteria to use both 
scripts together.


## **Explanation Examples** ##

----------------------------------------------------------------------------------------------------

The traditional example would probably deal with a requirements.txt file, often used to set up 
the correct packages in a virtual environment to recreate research or use some program that another
user has built. One reason a user may wish to pull the versions off a list of packages, the goal of
one script here, would be to have conda or pip default to automatically installing the most recent 
version of the package available.<br> 

> Obviously, when supplying a requirements file, users are typically seeking the stability and
> ability to ensure accurate results of their program when run within a virtual environment. For
> this reason, I want to be clear that I am **not** suggesting the user strip package versions
> from a requirements file and update all packages to the newest versions while using the program
> tied to that particular requirements file. This would obviously defeat the purpose of the package 
> file in the first place.<br> 

### **pkg_names and pkg_names_eff** ###

On the other hand, what I am suggesting is this. If a user happens to run across a large
requirements file from an old, unmaintained project, or is able to obtain what the user feels is a 
great list of packages to set up a new data science or other type of environment. Then they soon
discover the list also contains outdated version restrictions for each of the packages, then one
of the scripts here will allow the user to remove the versions without having to manually, line by
line, manipulate the file.<br> 

### **pkg_scraper and pkg_scraper_eff** ##

That being said, the other script available here may keep that problem from arising altogether. The 
example of that script will show how to pull every package listed on Anaconda's website for a
certain version of Python and a certain operating system architecture, then filter out most if
not all of the packages that are Anaconda specific. So the user is left with a file that is a
great example and quite a large list of packages for scientific or statistical computing, without 
having to also bring along the overhead that comes with the installation of an Anaconda
distribution.<br>


## **To Conda Or Not To Conda** ##

----------------------------------------------------------------------------------------------------

I feel like I should mention that I stopped using Anaconda for a couple of years because I realized 
I was not learning everything that was really needed. I had begun using Anaconda not long after
learning Python, but one day I noticed if I tried to work on a computer without Anaconda installed, 
I was hardly able to even access Python. Ok, maybe I am making it sound a little bit worse than
it really was, but if you are someone that feels comfortable with their Python skills, but has
spent little time outside of an Anaconda distribution, I really recommend proving to yourself
that you can operate near the same level without it. After all, I have yet to hear about a coding 
interview where the interviewer said sit down and show me what you can do with this Anaconda
distribution... Actually, after quickly getting back into the flow of not using Anaconda, there
were a number of things I found to be much easier without it. Since then, I have gone back to using 
Anaconda, but I still will not let myself fall into the trap of becoming dependent on it by not
using it exclusively, and there are certain topics for which I will never use it because it makes
the process overcomplicated.<br>


## **Anacondaing** ##

----------------------------------------------------------------------------------------------------

Now, after all that Anaconda bashing, I am going to show a number of examples that can be used in
Anaconda to accomplish similar, or possibly even the same, results that someone can achieve
through the scripts provided. There are also similar methods available for pip with the use of
`pipreqs`, although I cannot speak to the efficacy of this package as I have not used it. Details 
for the package are available at "https://github.com/bndr/pipreqs". Below, I will give a short 
explanation with some simple examples of the techniques available with Anaconda.<br> 

### **Anacondaing Examples** ###

Once packages are installed into a specific virtual environment, the user can then export a list of 
the packages with their respective package versions, build versions, and/or channel URLs in a
text file using any of the following, depending on the user's needs. In addition, a similar option 
exports a YAML (.yml) file with different options and slightly different information. Both of these 
exported files can later be used to install packages into a new virtual environment, or create an 
entirely new virtual environment from scratch (using a .yml file with accurate information). Of 
course, more details and examples can be found in the documentation for Anaconda, the Anaconda
website, and/or the Anaconda cheatsheet...<br>

> create file containing each package channel URL (to download): 
~~~
$ conda list --explicit > pkgs.txt
~~~
> create file containing package, version, build ('=' delimiter format):
~~~
$ conda list --export > pkgs.txt
~~~
> create file containing package, version, build, channel (column format): 
~~~
$ conda list > pkgs.txt
~~~
> create file containing only package names (this requires us to pipe the file so that we remove 
> everything after and including the first equals sign):
~~~
$ conda list --export | cut -f 1 -d '=' > pkgs.txt
~~~
> create file containing environment name, each channel name, each canonical/anaconda package and
> any dependencies along with the respective version and build ('=' delimiter format), each pip 
> package along with the respective version ('==' delimiter format), and a prefix providing the path
> to the virtual environment:
~~~
$ conda env --name base > environment.yml 
~~~
> (example is if environment `base` is not active)
~~~
$ conda env export > environment.yml
~~~
> (example is if environment is already active)

> create same file as above, but without build information:
~~~
$ conda env export --no-builds > environment.yml
~~~
> create same file as the first YAML, but with no package dependencies (only originally installed 
> packages), no versions, and no builds (packages installed with pip may also be excluded from this 
> list, I did not have enough information to determine this for certain or not)
~~~
$ conda env export --from-history > environment.yml
~~~
> of course, just as we used piping with conda list above, we can use it here; 
> create the same file the one above, but with all packages and dependencies:
~~~
$ conda env export | cut -f 1 -d '=' > environment.yml
~~~
> create the same file as the one with versions but no build, but now all delimiters are one '=':
~~~
$ conda env export | sed 's/==/=/g' | cut -f 1,2 -d '=' > environment.yml
~~~
> create the same file as the one above but remove the prefix (path) from the bottom of the file:
~~~
$ conda env export | sed 's/==/=/g' | cut -f 1,2 -d '=' | head -n -2 > environment.yml
~~~
> (using the `head -n -2` method, which deletes the last two rows)
~~~
$ conda env export | sed 's/==/=/g' | cut -f 1,2 -d '=' | grep -v "prefix" > environment.yml
~~~
>(using the `grep -v "prefix"` method, which prints lines that do **not** match pattern defined)

> hopefully there are enough examples above so that any users can figure out what they need to put
> together if they are in need of some combination that is not shown; the only one that may not
> be so obvious is the `sed` command; basically, the `s` inside the parenthesis is for substitute, 
> so in the examples above everything with two equal signs (the pip packages and their versions) are
> being substituted for one equal sign; of course, most anything can be replaced here if needed.


## **Conclusion** ##

Please excuse any sloppiness in coding standards, problems in transferring use to a different
operating system than my own, or other unexpected issues that might/will certainly come up. That
is, assuming anyone actually even views this page and at then at that actually thinks this simple
project is worth cloning/pulling/downloading/etc, and that is one very large assumption. For
information purposes, I dual boot 64-bit versions of Windows 10 and Linux Ubuntu 18.04 LTS, but
hardly ever run Windows any longer because my files are accessible from Linux. The only testing
was completed on Linux, and I am still an amateur in every sense of the word (really to
even be called that is giving myself too much credit...). The explanatory notes and code line 
comments are only under the inefficient, looping implementations of the scripts. The efficient
implementations using list comprehension do not have any comments, since they basically complete 
the same operations, just through different processes. Also, the inefficient, looping methods are
really there to help anyone learning to code, or give insight to those attempting to understand what
was done and why it was done, or my general thought process to initially solve the problems. If
someone does find this page somehow, I hope it helps at least one person, and suggestions or
criticism is always welcome in any form.     

----------------------------------------------------------------------------------------------------


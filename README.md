# Italents

A job portal site like DICE, Naukri, monster


## Dependencies

+    apscheduler
+    crispy_forms
+    django => 1.5
+    haystack
+    httplib2
+    oauth2
+    openid
+    paypal
+    pytz
+    registration
+    rosetta
+    social_auth
+    taggit
+    whoosh
+    BeautifulSoup
+    microsofttranslator
+    virtualenv


## Features

### Registration

There are two type of users, Employer(Reqruiter) & JobSeeker.

+    Employer: can post a job, view profiles of jobseeker.

+    Jobseeker: can view jobs, apply jobs, can participate in quorums and quizess to increase his points, he can add his facebook and stackoverflow accounts.


### crispy forms

i am going to use crispy forms onwards.

<pre>
pip install --upgrade django-crispy-forms
INSTALLED_APPS = (
 
    'crispy_forms',
)
</pre>


### Microsoft Translator usage

+	>>> from msbing import Translator
+	>>> trans = Translator('9c86952f-4c35-4ffe-9987-24726e3a881b', 'hpnPDDdp8JxkYH0xBl/37EM1wN8S1DE4s07dbBMkidM')
+	>>> print trans.translate("Hello", "pt")



### solr installation

    curl -O http://apache.mirrors.tds.net/lucene/solr/3.6.2/apache-solr-3.6.2.tgz
    tar xvzf apache-solr-3.5.0.tgz
    cd apache-solr-3.5.0
    cd example
    java -jar start.jar


### useful paypal website

+    https://developer.paypal.com/webapps/developer/index?state=13476501861111228409

+    https://www.paypal.com/webapps/business/


1.    Go to My Profile

2.    Then Go to My Selling Tools. Its on the Left Side of your Paypal

3.    Then look under a Tab called Selling Online and you'll see Website Prefrences 


## Amazone checkout keys

+    AWSAccessKeyId=AKIAJQCGXRALW7J5I5KQ
+    AWSSecretKey=k/3v7uYOvArkPsSrCOWoUwsdd8YkQ/Jo8uhyN6NK


### Recursive Permission Changes

    sudo chmod 777 -R /path/to/someDirectory


## Flatpages app

Flatpages used for staticpages

### To install the flatpages app, follow these steps:

+    Add `django.contrib.sites` to your INSTALLED_APPS setting
 
+    Also make sure you have correctly set SITE_ID.

+    Add `django.contrib.flatpages` to your INSTALLED_APPS setting.

+    Add an entry in your URLconf  `(r'^pages/', include('django.contrib.flatpages.urls'))`	 
    
+    Run the command manage.py syncdb.

+    create a template `flatpages/default.html` 
     for eg: `<title>{{ flatpage.title }}</title><body>{{ flatpage.content }}</body>`


### how to install sublime3.0

+    sudo add-apt-repository ppa:webupd8team/sublime-text-3
+    sudo apt-get update
+    sudo apt-get install sublime-text-installer


### GIT

##### How to setup git project in server

+    `git clone --bare gsm ngsm`
+    `scp -r ngsm suhail@192.168.1.201:/home/github`

##### To clone my Server Repo(Jobsite) a perticular branch say master

`git clone -b master suhail@192.168.1.201:/home/github/jobsite`


##### To see the existing remote url

`git config  remote.origin.url`

##### To add new remore url,

`git remote set-url origin suhail@192.168.1.201:/home/github/jobsite`


##### To clone Karthik

`git clone capsone-system7@192.168.1.33:/home/capsone-system7/Karthik/Git/repo/userreg.git`


##### creating a new branch and push it to server

`git checkout -b your_branch`
`git push capsone-system7@192.168.1.33:/home/capsone-system7/Karthik/Git/repo/userreg.git forum`

##### to track that branch by some other

`git checkout --track origin/forum`

##### push and pull perticular branch

`git push origin forum`
`git pull origin forum`


##### git checkout to a perticular commit

`git checkout [revision] .`
`wherer [revision] is the commit hash (for example: 12345678901234567890123456789012345678ab).`


### APScheduler

example usages:

    >>> from apscheduler.scheduler import Scheduler
    >>> sc=Scheduler
    >>> sc=Scheduler()
    >>> sc.start()
    >>> def job_function():
    ...   print 'hello'
    ... 
    >>> sc.add_cron_job(job_function,month='7',day='24',hour='10',minute=50)
    
    
### virtualenvwrapper

##### To install (make sure virtualenv is already installed):

    $ pip install virtualenvwrapper
    $ export WORKON_HOME=~/Envs
    $ source /usr/local/bin/virtualenvwrapper.sh
    

##### Create a virtual environment:

`$ mkvirtualenv venv`

This creates the venv folder inside ~/Envs.

##### Work on a virtual environment:

`$ workon venv`

##### Deactivating is still the same:

`$ deactivate`

##### To delete:

`$ rmvirtualenv venv`

##### List all of the environments.

`lsvirtualenv`


crontab -e    Edit your crontab file, or create one if it doesn’t already exist.
crontab -l      Display your crontab file.
crontab -r      Remove your crontab file.

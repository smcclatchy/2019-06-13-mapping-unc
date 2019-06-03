---
layout: workshop      # DON'T CHANGE THIS.
carpentry: ""
venue: "Quantitative Trait Mapping in the Diversity Outbred"
address: "Room 5007, Genetic Medicine Building, 120 Mason Farm Road, University of North Carolina, Chapel Hill, NC"
country: "us"
language: "en"
latlng: "35.915543,-79.049287"
humandate: "June 13-14, 2019"
humantime: "9:00 am - 4:30 pm"
startdate: 2019-06-13
enddate: 2019-06-14
instructor: ["Sue McClatchy", "Dan Gatti"]
helper: [""]
email: ["susan.mcclatchy@jax.org"]
collaborative_notes:             # optional: URL for the workshop collaborative notes, e.g. an Etherpad or Google Docs document
eventbrite:           # optional: alphanumeric key for Eventbrite registration, e.g., "1234567890AB" (if Eventbrite is being used)
---

{% comment %} See instructions in the comments below for how to edit specific sections of this workshop template. {% endcomment %}

{% comment %}
HEADER

Edit the values in the block above to be appropriate for your workshop.
If the value is not 'true', 'false', 'null', or a number, please use
double quotation marks around the value, unless specified otherwise.
And run 'make workshop-check' *before* committing to make sure that changes are good.
{% endcomment %}

{% if page.carpentry != site.carpentry %}
<div class="alert alert-warning">
You specified <code>carpentry: {{page.carpentry}}</code> in <code>index.md</code> and
<code>carpentry: {{site.carpentry}}</code> in <code>_config.yml</code>. Make sure you edit both files. After editing <code>_config.yml</code>, you need to run <code>make serve</code> again to 
see the changes take effect locally.
</div>
{% endif %}

{% comment %}
EVENTBRITE

This block includes the Eventbrite registration widget if
'eventbrite' has been set in the header.  You can delete it if you
are not using Eventbrite, or leave it in, since it will not be
displayed if the 'eventbrite' field in the header is not set.
{% endcomment %}
{% if page.eventbrite %}
<iframe
  src="https://www.eventbrite.com/tickets-external?eid={{page.eventbrite}}&ref=etckt"
  frameborder="0"
  width="100%"
  height="280px"
  scrolling="auto">
</iframe>
{% endif %}


<h2 id="general">General Information</h2>

{% comment %}
INTRODUCTION

Edit the general explanatory paragraph below if you want to change
the pitch.
{% endcomment %}
{% if page.carpentry == "swc" %}
{% include sc/intro.html %}
{% elsif page.carpentry == "dc" %}
{% include dc/intro.html %}
{% elsif page.carpentry == "lc" %}
{% include lc/intro.html %}
{% endif %}

{% comment %}
AUDIENCE

Explain who your audience is.  (In particular, tell readers if the
workshop is only open to people from a particular institution.
{% endcomment %}
{% if page.carpentry == "swc" %}
{% include sc/who.html %}
{% elsif page.carpentry == "dc" %}
{% include dc/who.html %}
{% elsif page.carpentry == "lc" %}
{% include lc/who.html %}
{% endif %}

{% comment %}
LOCATION

This block displays the address and links to maps showing directions
if the latitude and longitude of the workshop have been set.  You
can use https://itouchmap.com/latlong.html to find the lat/long of an
address.
{% endcomment %}
{% if page.latlng %}
<p id="where">
  <strong>Where:</strong>
  {{page.address}}.
  Get directions with
  <a href="//www.openstreetmap.org/?mlat={{page.latlng | replace:',','&mlon='}}&zoom=16">OpenStreetMap</a>
  or
  <a href="//maps.google.com/maps?q={{page.latlng}}">Google Maps</a>.
</p>
{% endif %}

{% comment %}
DATE

This block displays the date and links to Google Calendar.
{% endcomment %}
{% if page.humandate %}
<p id="when">
  <strong>When:</strong>
  {{page.humandate}}.
  {% include workshop_calendar.html %}
</p>
{% endif %}

{% comment %}
SPECIAL REQUIREMENTS

Modify the block below if there are any special requirements.
{% endcomment %}
<p id="requirements">
  <strong>Requirements:</strong> Participants must bring a laptop with a
  Mac, Linux, or Windows operating system (not a tablet, Chromebook, etc.) that they have administrative privileges on. They should have a few specific software packages installed (listed <a href="#setup">below</a>).
</p>

{% comment%}
CODE OF CONDUCT
{% endcomment %}
<p id="code-of-conduct">
<strong>Code of Conduct:</strong>  Everyone who participates  is required to conform to the <a href="https://docs.carpentries.org/topic_folders/policies/code-of-conduct.html">Code of Conduct</a>.
</p>


{% comment %}
ACCESSIBILITY

Modify the block below if there are any barriers to accessibility or
special instructions.
{% endcomment %}
<p id="accessibility">
  <strong>Accessibility:</strong> We are committed to making this workshop
  accessible to everybody.
  The workshop organizers have checked that:
</p>
<ul>
  <li>The room is wheelchair / scooter accessible.</li>
  <li>Accessible restrooms are available.</li>
</ul>
<p>
  Materials will be provided in advance of the workshop and
  large-print handouts are available if needed by notifying the
  organizers in advance.  If we can help making learning easier for
  you (e.g. sign-language interpreters, lactation facilities) please
  get in touch (using contact details below) and we will
  attempt to provide them.
</p>

{% comment %}
CONTACT EMAIL ADDRESS

Display the contact email address set in the configuration file.
{% endcomment %}
<p id="contact">
  <strong>Contact</strong>:
  Please email
  {% if page.email %}
  {% for email in page.email %}
  {% if forloop.last and page.email.size > 1 %}
  or
  {% else %}
  {% unless forloop.first %}
  ,
  {% endunless %}
  {% endif %}
  <a href='mailto:{{email}}'>{{email}}</a>
  {% endfor %}
  {% else %}
  to-be-announced
  {% endif %}
  for more information.
</p>

<hr/>

<h2 id="surveys">Surveys</h2>
<p>Please be sure to complete these surveys before and after the workshop.</p>
<p><a href="https://www.surveymonkey.com/r/pre-mapping">Pre-workshop Survey</a></p>
<p><a href="">Post-workshop Survey</a></p>

<hr/>

<h2 id="schedule">Schedule</h2>

<div class="row">
<div class="col-md-6">
<h3>Thursday, June 13</h3>
<table class="table table-striped">
<tr> <td>09:00</td>  <td><a href="https://smcclatchy.github.io/mapping/01-introduction/">Introductions and Workshop Overview</a></td> </tr>
<tr> <td>09:30</td>  <td><a href="https://smcclatchy.github.io/mapping/02-input-file-format/">Input File Format</a></td> </tr>
<tr> <td>10:00</td>  <td><a href="https://smcclatchy.github.io/mapping/03-calc-genoprob/">Calculating Genotype Probabilities</a></td> </tr>
<tr> <td>10:45</td>  <td>Coffee</td> </tr>
<tr> <td>11:00</td>  <td><a href="https://smcclatchy.github.io/mapping/04-special-x-covar/">Special covariates for the X chromosome</a></td> </tr>
<tr> <td>11:30</td>  <td><a href="https://smcclatchy.github.io/mapping/05-perform-genome-scan/">Performing a genome scan</a></td> </tr>
<tr> <td>12:00</td>  <td>Lunch break</td> </tr>
<tr> <td>13:00</td>  <td><a href="https://smcclatchy.github.io/mapping/05-perform-genome-scan/">Performing a genome scan (continued) </a></td> </tr>
<tr> <td>13:30</td>  <td><a href="https://smcclatchy.github.io/mapping/06-perform-perm-test/">Performing a permutation test</a></td> </tr>
<tr> <td>14:00</td>  <td><a href="https://smcclatchy.github.io/mapping/07-find-lod-peaks/">Finding LOD peaks</a></td> </tr>
<tr> <td>14:30</td>  <td>Coffee</td> </tr>
<tr> <td>14:45</td>  <td><a href="https://smcclatchy.github.io/mapping/08-calc-kinship/">Calculating A Kinship Matrix</a></td> </tr>
<tr> <td>15:45</td>  <td><a href="https://smcclatchy.github.io/mapping/09-perform-genome-scan-lmm/">Performing a genome scan with a linear mixed model</a></td> </tr>
<tr> <td>16:25</td>  <td>Wrap-up</td> </tr>
<tr> <td>16:30</td>  <td>End</td> </tr>
</table>
</div>
<div class="col-md-6">
<h3>Friday, June 14</h3>
<table class="table table-striped">
<tr> <td>09:00</td>  <td><a href="https://smcclatchy.github.io/mapping/09-perform-genome-scan-lmm/">Performing a genome scan with a linear mixed model (brief review)</a></td> </tr>
<tr> <td>09:30</td>  <td><a href="https://smcclatchy.github.io/mapping/10-perform-genome-scan-bin/">Performing a genome scan with binary traits</a></td> </tr>
<tr> <td>09:45</td>  <td><a href="https://smcclatchy.github.io/mapping/11-est-qtl-effects/">Estimated QTL effects</a></td> </tr>
<tr> <td>10:45</td>  <td>Coffee</td> </tr>
<tr> <td>11:00</td>  <td>Diversity Outbred Mice (lecture)</td> </tr>
<tr> <td>12:00</td>  <td>Lunch break</td> </tr>
<tr> <td>13:00</td>  <td><a href="https://smcclatchy.github.io/mapping/13-qtl-in-do/">QTL analysis in Diversity Outbred Mice</a></td> </tr>
<tr> <td>14:30</td>  <td>Coffee</td> </tr>
<tr> <td>14:45</td>  <td><a href="https://smcclatchy.github.io/mapping/13-qtl-in-do/">QTL analysis in Diversity Outbred Mice (continued)</a></td> </tr>
<tr> <td>16:25</td>  <td>Wrap-up</td> </tr>
<tr> <td>16:30</td>  <td>End</td> </tr>
</table>
</div>
</div>

{% comment %}
Collaborative Notes

If you want to use an Etherpad, go to

http://pad.carpentries.org/YYYY-MM-DD-site

where 'YYYY-MM-DD-site' is the identifier for your workshop,
e.g., '2015-06-10-esu'.
{% endcomment %}
{% if page.collaborative_notes %}
<p id="collaborative_notes">
  We will use this <a href="{{page.collaborative_notes}}">collaborative document</a> for chatting, taking notes, and sharing URLs and bits of code.
</p>
{% endif %}

<hr/>

{% comment %}
SYLLABUS

Show what topics will be covered.

1. If your workshop is R rather than Python, remove the comment
around that section and put a comment around the Python section.
2. Some workshops will delete SQL.
3. Please make sure the list of topics is synchronized with what you
intend to teach.
4. You may need to move the div's with class="col-md-6" around inside
the div's with class="row" to balance the multi-column layout.

This is one of the places where people frequently make mistakes, so
please preview your site before committing, and make sure to run
'tools/check' as well.
{% endcomment %}
<h2 id="syllabus">Syllabus</h2>

{% if page.carpentry == "swc" %}
{% include sc/syllabus.html %}
{% elsif page.carpentry == "dc" %}
{% include dc/syllabus.html %}
{% elsif page.carpentry == "lc" %}
{% include lc/syllabus.html %}
{% endif %}

<hr/>

{% comment %}
SETUP

Delete irrelevant sections from the setup instructions.  Each
section is inside a 'div' without any classes to make the beginning
and end easier to find.

This is the other place where people frequently make mistakes, so
please preview your site before committing, and make sure to run
'tools/check' as well.
{% endcomment %}

<h2 id="setup">Setup</h2>

<p>
  To participate in a
  {% if page.carpentry == "swc" %}
  Software Carpentry
  {% elsif page.carpentry == "dc" %}
  Data Carpentry
  {% elsif page.carpentry == "lc" %}
  Library Carpentry
  {% endif %}
  workshop,
  you will need access to the software described below.
  In addition, you will need an up-to-date web browser.
</p>

<div id="r"> {% comment %} Start of 'R' section. {% endcomment %}
<h3>R</h3>

<p>
<a href="https://www.r-project.org">R</a> is a programming language
that is especially powerful for data exploration, visualization, and
statistical analysis. To interact with R, we use
<a href="https://www.rstudio.com/">RStudio</a>.
</p>

<div>
<ul class="nav nav-tabs nav-justified" role="tablist">
<li role="presentation" class="active"><a data-os="windows" href="#rstats-windows" aria-controls="Windows" role="tab" data-toggle="tab">Windows</a></li>
<li role="presentation"><a data-os="macos" href="#rstats-macos" aria-controls="MacOS" role="tab" data-toggle="tab">MacOS</a></li>
<li role="presentation"><a data-os="linux" href="#rstats-linux" aria-controls="Linux" role="tab" data-toggle="tab">Linux</a></li>
</ul>

<div class="tab-content">
<article role="tabpanel" class="tab-pane active" id="rstats-windows">
<a href="https://www.youtube.com/watch?v=q0PjTAylwoU">Video Tutorial</a>
<p>
Install R by downloading and running
<a href="https://cran.r-project.org/bin/windows/base/release.htm">this .exe file</a>
from <a href="https://cran.r-project.org/index.html">CRAN</a>.
Also, please install the
<a href="https://www.rstudio.com/products/rstudio/download/#download">RStudio IDE</a>.
Note that if you have separate user and admin accounts, you should run the
installers as administrator (right-click on .exe file and select "Run as
administrator" instead of double-clicking). Otherwise problems may occur later,
for example when installing R packages.
</p>
</article>
<article role="tabpanel" class="tab-pane active" id="rstats-macos">
<a href="https://www.youtube.com/watch?v=5-ly3kyxwEg">Video Tutorial</a>
<p>
Install R by downloading and running
<a href="https://cran.r-project.org/bin/macosx/R-latest.pkg">this .pkg file</a>
from <a href="https://cran.r-project.org/index.html">CRAN</a>.
Also, please install the
<a href="https://www.rstudio.com/products/rstudio/download/#download">RStudio IDE</a>.
</p>
</article>
<article role="tabpanel" class="tab-pane active" id="rstats-linux">
<p>
You can download the binary files for your distribution
from <a href="https://cran.r-project.org/index.html">CRAN</a>. Or
you can use your package manager (e.g. for Debian/Ubuntu
run <code>sudo apt-get install r-base</code> and for Fedora run
<code>sudo dnf install R</code>).  Also, please install the
<a href="https://www.rstudio.com/products/rstudio/download/#download">RStudio IDE</a>.
</p>
</article>
</div>
</div>
</div> {% comment %} End of 'R' section. {% endcomment %}

## qtl2

The [qtl2](https://github.com/rqtl/qtl2) package contains code for haplotype reconstruction, QTL mapping and plotting.

Option 1: R/qtl2 is not yet available on [CRAN](https://cran.r-project.org), but it can be installed from a mini-CRAN at [rqtl.org](http://www.rqtl.org/). Make sure you have the latest version of [R (3.4.4)](https://cran.r-project.org).

Option 2: Alternatively, you can install R/qtl2 from its source on [GitHub](https://github.com/rqtl).
(But note that compiling the C++ code can be rather slow.)

On _Windows_, you'll need [Rtools](https://cran.r-project.org/bin/windows/Rtools/).

On _Mac OS X_, you'll need the
[command-line developer tools](https://mac-how-to.gadgethacks.com/how-to/install-command-line-developer-tools-without-xcode-0168115/),
as well as [gfortran](https://gcc.gnu.org/wiki/GFortranBinaries#MacOS).

You then need to install the
[devtools](https://github.com/hadley/devtools) package, plus a set of
package dependencies: [yaml](https://cran.r-project.org/package=yaml),
[jsonlite](https://cran.r-project.org/package=jsonlite),
[data.table](https://cran.r-project.org/package=data.table),
and [RcppEigen](https://github.com/RcppCore/RcppEigen).
(Additional, secondary dependencies will also be installed.) Start RStudio, then copy and paste the following code into the R console in RStudio.

~~~
install.packages(c("devtools", "yaml", "jsonlite", "data.table", "RcppEigen", "RSQLite", "qtl"))
~~~
{: .r}

Finally, install R/qtl2 using `devtools::install_github()`. Copy and paste the following code into the R console in RStudio.

~~~
library(devtools)
install_github("rqtl/qtl2")
~~~
{: .r}

## Data files and project organization

1. Make a new folder in your Desktop called `mapping`. Move into this new folder.

2. Create  a `data` folder to hold the data, a `scripts` folder to house your scripts, and a `results` folder to hold results. 

Alternatively, you can use the R console to run the following commands for steps 1 and 2.

~~~
setwd("~/Desktop")
dir.create("./mapping")
setwd("~/Desktop/mapping")
dir.create("./data")
dir.create("./scripts")
dir.create("./results")
~~~
{: .r}

3. Please download the following large files **before the workshop**, and place them in your `data` folder. You can download the files from the URLs below and move the files the same way that you would for downloading and moving any other kind of data.

- [cc_variants.sqlite doi:10.6084/m9.figshare.5280229.v2](https://figshare.com/articles/SQLite_database_of_variants_in_Collaborative_Cross_founder_mouse_strains/5280229/2), variants in the Collaborative Cross founders (3 GB)
- [mouse_genes.sqlite doi:10.6084/m9.figshare.5280238.v4](https://figshare.com/articles/SQLite_database_with_mouse_gene_annotations_from_Mouse_Genome_Informatics_MGI_at_The_Jackson_Laboratory/5280238/4) full set of mouse gene annotations (677 MB)
- [mouse_genes_mgi.sqlite doi:10.6084/m9.figshare.5286019.v5](https://figshare.com/articles/SQLite_database_with_MGI_mouse_gene_annotations_from_Mouse_Genome_Informatics_MGI_at_The_Jackson_Laboratory/5286019/5) just the MGI mouse gene annotations (11 MB)
- [DO QTL data](ftp://ftp.jax.org/dgatti/qtl2_workshop/qtl2_demo.Rdata) Dan's DO data from the benzene study

Alternatively, you can copy and paste the following into the R console to download the data.
~~~
setwd("~/Desktop/mapping")
download.file("https://ndownloader.figshare.com/files/9746485", "./data/cc_variants.sqlite")
download.file("https://ndownloader.figshare.com/files/9746458", "./data/mouse_genes.sqlite")
download.file("https://ndownloader.figshare.com/files/9746452", "./data/mouse_genes_mgi.sqlite")
download.file("ftp://ftp.jax.org/dgatti/qtl2_workshop/qtl2_demo.Rdata", "./data/qtl2_demo.Rdata")
~~~
{: .r}


You will need these for the final lesson episodes on SNP association mapping and QTL analysis in Diversity Outbred mice.


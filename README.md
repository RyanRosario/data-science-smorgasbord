# Data Science Smorgasbord
## *Statistics 404* :neckbeard:
## February 28, 2017
### :palm_tree: Ryan R. Rosario :hibiscus: 

Materials from a three-hour lecture I gave to UCLA Statistics 404 (Professional Masters in Applied Statistics) on Unix command line, Python :snake: and PyData. 

# Raw Data

If you wish to work with the **raw** Reddit comments data, you can download them on a monthly basis from [here](http://files.pushshift.io/reddit/comments/).

As Reddit gets more and more use, the files get larger and larger. As of February 2017, compressed .bz2 files amass upwards of 8GB.

Once you've downloaded a dump file, you can decompress it with

`bunzip2 file.bz2`

This takes a while. As of February 2017, uncompressed files are about 35GB per month, all in one file.

You can concatenate multiple months into one file if you wish, using the cat command.

`cat file_1 file_2 > mybigfile`

Then you can use a tool like [jq](https://stedolan.github.io/jq/) to parse the JSON files without reading it into Python first.

# Processed Data for Lecture

To follow along with the lecture, you don't need to download any raw data. 

The file [`political_comments_sorted.tsv`](http://www.bytemining.com/files/datasets/stats404/political_comments_sorted.tsv) is the file created on slide 60. It can be used for all previous slides as well, but due to space and bandwidth constraints, I only provide one version. The sorted version sorts the file by username.

The files [`goodusers.dat`](http://www.bytemining.com/files/datasets/stats404/goodusers.dat) and [`usernames.dat`](http://www.bytemining.com/files/datasets/stats404/usernames.dat) are intermediate files created on slides 55 and 50 respectively in case you wish to skip the code on those slides.

**The final dataset that does not contain any bots is in the file [`political_comments_clean.tsv`](http://www.bytemining.com/files/datasets/stats404/political_comments_clean.tsv).**

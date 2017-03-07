# Data Science Smorgasbord
## Unix Tools - Python - PyData - Career Advice
## *Statistics 404*
## February 28, 2017

Materials from a three-hour lecture I gave to UCLA Statistics 404 (Professional Masters in Applied Statistics) on Unix command line, Python and PyData. These will be routinely updated.

# Raw Data

If you wish to work with the **raw** Reddit comments data, you can download them on a monthly basis from [http://files.pushshift.io/reddit/comments/].

As Reddit gets more and more use, the files get larger and larger. As of February 2017, compressed .bz2 files amass upwards of 8GB.

Once you've downloaded a dump file, you can decompress it with

`bunzip2 file.bz2`

This takes a while. As of February 2017, uncompressed files are about 35GB per month, all in one file.

You can concatenate multiple months into one file if you wish, using the cat command.

`cat file_1 file_2 > mybigfile`

Then you can use a tool like [jq](https://stedolan.github.io/jq/) to parse the JSON files without reading it into Python first.

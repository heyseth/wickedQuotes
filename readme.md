# wickedQuotes

There aren't any large, public datasets of quotes to be found online. So I decided to create my own by parsing and cleaning up a Wikiquote data dump. This repository contains the script that does that, along with a generated json file of quotes if you just want the data.

## Usage

Download a data dump of wikiquote:

`wget https://dumps.wikimedia.org/enwikiquote/latest/enwikiquote-latest-pages-articles.xml.bz2`

Extract the archive:

`bzip2 -d enwikiquote-latest-pages-articles.xml.bz2`

Then run the program:

`python parse.py enwikiquote-latest-pages-articles.xml`

This will probably take a while (it takes a few minutes on my pc). 

There are two optional parameters. Quote cutoff length, and desired language. The default cutoff is 100 characters, and the default language is English. The language must be specified as an [ISO Language Code](https://www.w3schools.com/tags/ref_language_codes.asp).

For instance, if you wanted quotes only in Chinese, and less than 50 characters in length, you would do the following.

`python parse.py enwikiquote-latest-pages-articles.xml 50 zh-cn`

## License

This project is licensed under the MIT License - see the license.md file for details.

## Acknowledgments
Huge thanks to:
* All the contributors to [Wikiquote](https://en.wikiquote.org/wiki/Main_Page), and the [Wikimedia Foundation](https://wikimediafoundation.org/wiki/Home).

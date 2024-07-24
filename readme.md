# wickedQuotes

There aren't any large, public datasets of quotes to be found online, so I decided to create my own by parsing and cleaning up a Wikiquote data dump.

## Setup

```
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
```

## Usage

Download a data dump of wikiquote:

`wget https://dumps.wikimedia.org/enwikiquote/latest/enwikiquote-latest-pages-articles.xml.bz2`

Extract the archive:

`bzip2 -d enwikiquote-latest-pages-articles.xml.bz2`

Run the program:

`./parse.py enwikiquote-latest-pages-articles.xml`

There are two optional parameters: quote cutoff length, and desired language. The default cutoff length is 100 characters, and the default language is English. The language must be specified as an [ISO Language Code](https://www.w3schools.com/tags/ref_language_codes.asp).

For instance, if you wanted quotes only in Spanish, and less than 50 characters in length, you would enter the following:

`./parse.py enwikiquote-latest-pages-articles.xml 50 es`

Alternatively, if you don't want to specify a language, simply enter "all" (no quotes) for the language parameter. This will massively shorten the time it takes the program to run.

## License

This project is licensed under the MIT License - see the license.md file for details.

## Acknowledgments
Huge thanks to:
* All the contributors to [Wikiquote](https://en.wikiquote.org/wiki/Main_Page), and the [Wikimedia Foundation](https://wikimediafoundation.org/wiki/Home).

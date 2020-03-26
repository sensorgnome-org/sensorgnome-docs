# sensorgnome-docs

documentation generator Sphinx docs for Sensorgnome software and hardware for read the docs.

https://sensorgnome.readthedocs.io/

## Setup

- Optionally, create a [virtualenv](https://docs.python-guide.org/dev/virtualenvs/).
- run `pip install -r requirements.txt`

## Building Docs

To build the documentation locally to test: run `make html` and then open the result from `_build/html`.

## Contributing

If you'd like to contribute to the docs, please fork this repo, make your changes and open a pull request so that we can review and then get your changes into the project.

You can also open an issue if something is unclear, to request missing documentation, etc.

Documentation is written using Restructured Text. A useful cheatsheet: https://thomas-cokelaer.info/tutorials/sphinx/rest_syntax.html

## Notes

Uses [sphinx-contrib/youtube](https://github.com/sphinx-contrib/youtube) to embed YouTube videos in sphinx output.
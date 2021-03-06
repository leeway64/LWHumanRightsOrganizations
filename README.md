# LWHumanRightsOrganizations


![Human rights word cloud](doc/images/human_rights_word_cloud.svg)


LWHumanRightsOrganizations displays a list of NGOs, human rights groups, and other organizations I
support.

Ubuntu Linux is the primary development environment for this project; all commands were tested in Ubuntu 21.10.


## Usage

```
$ git clone https://github.com/leeway64/LWHumanRightsOrganizations.git
$ cd LWHumanRightsOrganizations
$ ghc --make include/Main.hs include/Organizations.hs -o bin/Main
$ ./bin/Main



********************************************************************************
LWOrganizationsISupport is a Haskell program that displays the NGOs and human
rights organizations I support.

As a big believer in the importance of human rights, I want to share the
organizations that I have donated to.

Type "next" to get started!
next

********************************************************************************
Stop Putin
	Stand with Ukraine!
	Support the fight against Russia by visiting stopputin.net and donating to a fund.
	Down with Vladimir Putin and Xi Jinping!

Type "next" to continue.

    ...

```


## Documentation

If you prefer, you can also view LWOrganization's content through Sphinx-generated documentation.

To build the html file, run the following commands:

```
$ python3 -m venv .venv
$ source .venv/bin/activate
$ pip install -r requirements.txt
$ sphinx-build -b html doc/source doc/build
```

Then, under `doc/build`, open the `index.html` file.


## Links

A collected list of all the links can be viewed in the html file, or it can be viewed by running
the `references` Docker container.

```
$ sudo docker build -t references ./include
$ sudo docker run references



Collected here are the references/links mentioned in the Haskell program

Stop Putin
	Down with Vladmir Putin and Xi Jinping!
		stopputin.net

National Bank of Ukraine
	Support the Ukrainian Armed Forces:
		https://bank.gov.ua/en/news/all/natsionalniy-bank-vidkriv-spetsrahunok-dlya-zboru-koshtiv-na-potrebi-armiyi

	Support the humanitarian relief effort:
		https://bank.gov.ua/en/news/all/natsionalniy-bank-vidkriv-rahunok-dlya-gumanitarnoyi-dopomogi-ukrayintsyam-postrajdalim-vid-rosiyskoyi-agresiyi

    ...

```

For more information on how Docker works, refer to [this page](doc/docker/README.md).


## Third-party tools

- [Sphinx](https://github.com/sphinx-doc/sphinx) (BSD license): Documentation generator.
  - [sphinxcontrib-kroki](https://pypi.org/project/sphinxcontrib-kroki/) (MIT License): Allows for
    diagrams to be embedded into Sphinx documentation using Kroki. sphinxcontrib-kroki created the
    Vega word cloud at the start of this document.
  - [furo](https://pypi.org/project/furo/) (MIT License): Sphinx documentation theme.
- [Kroki](https://kroki.io/) (MIT License): Provides a simple way of drawing a variety of
  different types of diagrams (e.g.: PlantUML, BlockDiag).
- [Docker](https://www.docker.com/) (Apache-2.0 License): Packages software into independent containers.


## License

The content of this project is licensed under the the [Creative Commons Attribution 4.0 
International license](https://creativecommons.org/licenses/by/4.0/).

The source code used to format and display the content is licensed under the [MIT License](LICENSE.txt)


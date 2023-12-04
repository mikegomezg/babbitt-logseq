# Babbit Logseq

This project shows how to use [Logseq](https://github.com/logseq/logseq) to organize personal notes and track important information over time. The repository contains demo data based on the 1922 Sinclair Lewis novel _Babbitt_, taking the perspective of the main character George Babbitt. This public domain story provides a shared context for thinking about how to organize personal notes with Logseq.

## See it in Action

Visit the [web version](https://mikegomezg.github.io/babbitt-logseq/) of this notebook to see how Logseq works and what the demo data looks like.

I'm using Logseq's [publish feature](https://docs.logseq.com/#/page/publishing) together with a [GitHub action](https://docs.github.com/en/actions/learn-github-actions/understanding-github-actions) called [Logseq publish-spa](https://github.com/logseq/publish-spa)  and [GitHub Pages](https://docs.github.com/en/pages/quickstart) to automatically update the web version as I add notes.

## About the Notes

Imagine these are George Babbitt's daily notes. It doesn't matter for our purposes that the dates in Logseq don't correspond to the dates in the story; the goal here is to show how we can structure notes in Logseq to track important topics and events in someone's life.

## Install

To work with these notes on your computer using all of Logseq's features, follow these steps:

1. Download Logseq from the [official website](https://logseq.com). The download button on the site will retrieve the latest version, but you can also check the versions directly from Logseq's [GitHub releases page](https://github.com/logseq/logseq/releases).
2. Run the installer. Once Logseq is installed, the program will launch automatically and tell you it has loaded a demo graph.
3. Download this repository. You can download it as a ZIP file using the `Code` button on this page and then extract it, or use Git to fork/clone it.
4. Within the root folder of this repo is a folder called `babbitt`. In Logseq, click `Add a graph` and **select the `babbitt` subfolder**. 
	- It's important not to open the root folder of the repo with Logseq because the data will not load correctly and Logseq will create extra folders. If you open the wrong folder, simply close Logseq, delete the folder and download the repo again.
	- Logseq calls this `babbitt` subfolder a "graph" because the files are linked together. Any folder with markdown files can be a Logseq graph.
	- You can rename this `babbitt` folder if you want before opening it in Logseq, but renaming it will impact publishing if you chose to use that feature later.
	- Logseq reads all the files in the folder and then automatically creates an entry for whichever day it happens to be when you are working with the graph.

## Usage

In the Babbitt Logseq graph, you can:

- **Review Journal Entries:** Try to get a sense of what Babbitt is like by checking a few of his journal entries. You can click the chapter links to see the text of the story that the entries correspond to.
- **Work with the Outlines:** You can click the arrow next to each bullet point to expand the details beneath. If you click one of the links (called a page reference), you can see just those parts of his daily outlines that are relevant to a given topic (called a page).
- **Check the Contents Page:** I setup the Contents page on the right sidebar to show all the pages in the graph. I wrote a check called "Contents Query" to find pages that aren't referenced in the Contents page. Try creating a new page (maybe link to it in one of the journal pages) and then check the query to see if it finds your new page.

## Contributing

Since this project is still in its early stages, please use the public [GitHub discussions page](https://github.com/mikegomezg/babbitt-logseq/discussions) to share your feedback. Let me know if you have any ideas for working with this data to showcase what you've learned and helping others see the power of Logseq.

## License

All notes and documentation in this repository are licensed under the Creative Commons Attribution License 4.0 (CC-BY-4.0).

All code in this repository, including Logseq queries and helper scripts, is licensed under the GNU Affero General Public License v3.0 (AGPL-3.0), the same license that the Logseq codebase uses.

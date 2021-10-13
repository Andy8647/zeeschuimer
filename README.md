# 🏴‍☠️ Zeeschuimer

<p align="center"><img alt="A screenshot of Zeeschuimer's status window" src="images/example_screenshot.png"></p>

Zeeschuimer is a browser extension that monitors internet traffic while you are browsing a social media site, and 
collects data about the items you see in a platform's web interface for later systematic analysis. Its target audience
is researchers who wish to systematically study content on social media platforms that resist conventional scraping or 
API-based data collection.

You can, for example, browse TikTok and later export a list of all posts you saw in the order you saw them in. Data can 
be exported as a JSON file or exported to a [4CAT](https://github.com/digitalmethodsinitiative/4cat) instance for 
analysis and storage. Zeeschuimer is primarily intended as a companion to 4CAT, but you can also integrate its output
into your own analysis pipeline.

Currently, it supports the following platforms:
* TikTok via https://www.tiktok.com
* Instagram via https://www.instagram.com

Platform support requires regular maintenance to keep up with changes to the platforms. If something does not work, we
welcome issues and pull requests.

The extension does not interfere with your normal browsing and never uploads data automatically, only when you 
explicitly ask it to do so.

## Installation
Zeeschuimer is in active development. .xpi files of work-in-progress versions are available on the 
[releases](https://github.com/digitalmethodsinitiative/zeeschuimer/releases) page. These are signed and can be installed 
in any Firefox-based browser. If you want to run the latest development version instead, you can [do so from the Firefox
debugging console](https://www.youtube.com/watch?v=sAM78GU4P34&feature=emb_title).

## How to use
Install the browser extension in a Firefox browser. A button with the Zeeschuimer logo (a white skull on a black 
background) will appear in the browser toolbar. Click it to open the Zeeschuimer interface.

Next, simply browse a supported platform's site. You will see the amount of items detected per platform increase as you 
browse. When you have the items you need, you can export the data as an [ndjson](https://ndjson.org) file, or upload it
to a 4CAT instance where a 4CAT dataset will be created from the uploaded items. You can then run 4CAT's analytical 
processors on the data.

To upload to 4CAT, copy the URL of the website of the 4CAT instance to the "4CAT instance" field at the top of 
Zeeschuimer's interface. You can then use the "to 4CAT" button to create a new 4CAT dataset from the captured data. 
After uploading, Zeeschuimer will show you a link and the ten most recently uploaded datasets are shown at the bottom of
the interface.

Don't forget to reset the data as needed. For example, if you want to create a dataset for a given TikTok hashtag, first
reset the TikTok data in Zeeschuimer, _then_ go to the hashtag's "Explore" page on TikTok, and then upload the dataset
when you've scrolled down enough to be satisfied with the amount of items. 

## Credits & license
Zeeschuimer was developed by Stijn Peeters for the [Digital Methods Initiative](https://digitalmethods.net) and is 
licensed under the Mozilla Public License, 2.0. Refer to the LICENSE file for more information.

Skull icon based on '[Smile Skull Vector Icons](https://www.vecteezy.com/vector-art/93157-smile-skull-vector-icons)' by 
lavarmsg on Vecteezy.

Development is supported by the Dutch [PDI-SSH](https://pdi-ssh.nl/en/) foundation through the [CAT4SMR 
project](https://cat4smr.humanities.uva.nl/).

# india-tenders

This overall theme of this project is to look at any potential corruption related to the national tenders issued by the Indian government. The first step in this project was to look at all the data that the Indian government has made public and summarize it in a sensible way, whilst pointing out any discrepencies or irregularities.

The data can be found at https://eprocure.gov.in/cppp/. When looking through the list of tenders for a given year, the page looks as follows:

<img src="https://github.com/rajkk1/india-tenders/blob/master/readme_images/tenders_main.png" width="500" >

And when clicking on any of the links in the table above, we obtains something that looks like this:

<img src="https://github.com/rajkk1/india-tenders/blob/master/readme_images/tenders_details.png" width="500" >

The india-tenders.ipynb notebook is written to scrape all the available data on issued tenders from 2013 - 2018. When trying to scrape all the data _without_ getting any further details (i.e. without scraping through the information in any of the links for each row), it will at some point error out with the following message:

<img src="https://github.com/rajkk1/india-tenders/blob/master/readme_images/tenders_main_error.png" width="700" >

It seems like the website cannot handle the traffic coming from the script. When trying to scrape the data _with_ the details (i.e. including all the information in the links in each row)  it will at some point give a different error:

<img src="https://github.com/rajkk1/india-tenders/blob/master/readme_images/tenders_details_error.png" width="200" >

Right after this second error, if you try and visit the website on a browser it will come up with captcha question like the one below:

<img src="https://github.com/rajkk1/india-tenders/blob/master/readme_images/tenders_details_captcha.png" width="500" >

So it looks like the website blocks multiple requests to the details.

Currently this is where we are at.

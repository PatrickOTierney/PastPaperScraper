# PastPaperScraper

This code visits the SEC's website (examinations.ie) where Irish state examination papers are hosted and automatically scrapes the past papers and saves images containing a specific search term for ease of studying.

On run, after deleting all files in the output folder, the code will prompt for a number of threads to use and has a default value

It will ask what subject, found in the dropdown on their website, and is case sensitive

It will ask for a (case sensitive) search term, which is how it will choose what to save to the output folder

It will ask for a range of years, which is inputted using the earliest year-latest year, e.g. 2017-2020

It will then open webdrivers on each thread up to the limit you set, go through all the checkmarks on the page, get a link to the pdf and search the pdf for changes containing that search term, then save those pages as a pdf to your computer

### Issues

This code uses multithreading, which may cause Cloudflare's website defence to be triggered if you send too many requests too fast. The code will break if Cloudflare flags you as a robot.

Even with multithreading, it is quite slow, a future update could be to limit the speed of only the web drivers, then handle the computer side file managing using another thread






## Steps to get the Python on Microcontrollers Newsletter from GitHub to Adafruit Daily Wordpress

Anne – September 2, 2019, tweaks March 6, 2023 and June 22 & 28, 2023

1.	Go to the newsletter GitHub site drafts directory https://github.com/adafruit/circuitpython-weekly-newsletter/blob/gh-pages/_drafts/
2.	Rename the old newsletter from adafruit/circuitpython-weekly-newsletter/_drafts to ../_posts
3.	Download the assets for the current week to your PC
4.	Add the asset pictures to the Media section of the Wordpress site for adafruitdaily.com
5.  Ensure Newsletter Date & Title were entered correctly.
6.  Make sure GitHub Actions is green on the markdown text.
7.	Go to https://adafruit.github.io/circuitpython-weekly-newsletter/ and open the latest newsletter
8.	Use browser “view source” and copy all the HTML from the title in h2 tags (just past <!-- main content-wrapping table -->) to and including the paragraph
> The CircuitPython Weekly Newsletter is a CircuitPython community-run newsletter emailed every Tuesday. The complete <a href="https://www.adafruitdaily.com/category/circuitpython/">archives are here</a>. It highlights the latest CircuitPython related news from around the web including Python and MicroPython developments. To contribute, edit next week’s draft <a href="https://github.com/adafruit/circuitpython-weekly-newsletter/tree/gh-pages/_drafts">on GitHub</a> and <a href="https://help.github.com/articles/editing-files-in-your-repository/">submit a pull request</a> with the changes. Join our <a href="https://adafru.it/discord">Discord</a> or <a href="https://forums.adafruit.com/viewforum.php?f=60">post to the forum</a> for any further questions.
7.	The trick is to take that text and replace some strings in it to change the image links from GitHub to Wordpress. For this I use notepad++ but many text editors have a search and replace function.
a.	Find the strings ../assets/20230711 (use the current date) and replace with 
https://cdn-daily-blog.adafruitdaily.com/uploads/2023/07 (07 is the current month)
b.	Replace all instances. There should be the same number of replaces as there are images in the newsletter.
8.	In the adafruitdaily.com wordpress https://www.adafruitdaily.com/wp/wp-admin/edit.php open a new post
9.	Name the post first as the title in the header text of the draft markdown followed by the social media tags: #Python #Adafruit #CircuitPython #PythonHardware @ThePSF @circuitpython @micropython @Adafruit
10.	Use the **Text** tab in the body box which allows entry of HTML rather than the regular text. 
11.	Paste in the HTML from notepad++ or wherever you did the string replace.
12.	Click the **Visual** tab and you should see the formatted newsletter with the pictures.
13.	If you don’t see the images, you have an image upload issue or the search/replace you used had an issue.
14.	Save a draft now
15.	Change the title to Heading 1.
16.	Go through the entire newsletter text doing the following:
a.	Edit any spelling, punctuation, and grammar issues.
b.	Ensure all hyperlinks appear correct
c.	If there is a place where a picture should be but isn’t (you’ll see text that indicates an issue), go into the HTML, look for the image file it wants, then go back into the assets for the newsletter and try to find the file. When found, add to the Media portion of Wordpress.
d.	Changes to check for:
i.	Circuit Python -> CircuitPython
ii.	CircuitPlayground -> Circuit Playground
iii.	Wifi or Wi-Fi -> WiFi
iv.	NeoPixel, DotStar, HalloWing, Bluetooth, etc. Use spellings on Adafruit.com website.
e.	All bulleted items need to have left justify added to the, (highlight and select left justify in the tools). This ensures they are not centered which looks crummy. This applies to the Libraries list. Phil sometimes uses bullets in the articles too.
f.	In the Events section, I usually add the country (and city of needed) to ensure International readers know where the event us. Pasadena, CA -> Pasadena, California, USA
17.	Save a draft again
18.	Change Categories from Uncategorized to Python for Microcontrollers
19.	Add tags: Newsletter, CircuitPython, MicroPython, Python
20.	Use the Preview button, upper right
21.	Read through once more, ensuring pictures, text, etc. all look ok. If there is something out of place, edit the text again.
22.	When done with the second review, save another draft.
23. In the upper right Publish box, click edit next to Publish immediately. Change to publish date (Tuesday for Anne, Monday for Kattni) at 07 00. Double check the date then click Publish.
24.	Copy the newsletter link above the newsletter text, highlight "View this Email" in the first line "View this email in your browser" and make those three words a hyperlink with the newsletter URL. PT added this to make it easier for email readers. Click "Update" button to save that change.
25.	Ok, Newsletter complete.
26.	Get one of the previous emails I’ve sent out. Replace the links with the current links for the weeks’ newsletter.
a.	To circuit@adafruit.com
b.	Subject: Newsletter for September xx, 2023
c.	Here are the links for the Newsletter for September xx, 2023
d.	New link at top of post, the rest is all good.
e.	Wordpress (browser link):  https://www.adafruitdaily.com/wp/wp-admin/post.php?post=12102&action=edit&classic-editor
f.	WordPress Preview (link that Preview takes you to): https://www.adafruitdaily.com/?p=12102&preview=true
g.	The final URL (permalink link): https://www.adafruitdaily.com/2019/08/27/circuitpython-at-micro-center-micropython-takes-flight-with-feather-python-adafruit-circuitpython-pythonhardware-circuitpython-micropython-thepsf-adafruit/
h.	If you notice any issues, please feel free to fix it in Wordpress or email editor 
i.	GitHub: https://github.com/adafruit/circuitpython-weekly-newsletter/blob/gh-pages/_drafts/2019-08-27-draft.md
j.	Send
27.	Go back to the GitHub _drafts folder and copy all the markdown in template.md
28.	Create a new file 2023-mm-dd-draft.md and copy in the template markdown and save.
29.	Copy the link to the new draft newsletter 
30.	BONUS! Create a new assets directory with the name 2023mmdd (you can add a README.md to keep the directory in GitHub. https://github.com/adafruit/circuitpython-weekly-newsletter/tree/gh-pages/assets.

## Concise information Links (June, 2023)

- [Last weeks Stats & Subscribers](https://us10.admin.mailchimp.com/campaigns/show?id=569021) - Mailchimp (login needed)
- [Last Week's Newsletter](https://www.adafruitdaily.com/category/circuitpython/) - adafruitdaily.com
- New CircuitPython Boards: [Microcontrollers](https://circuitpython.org/downloads?sort-by=date-desc) and [Blinka](https://circuitpython.org/blinka?sort-by=date-desc). Compare with [last week](https://www.adafruitdaily.com/category/circuitpython/)
- [Team Updates](https://3.basecamp.com/3732686/buckets/4356693/questions/1994563901) - Basecamp, internal data
- [Weblate latest graphic](https://hosted.weblate.org/widgets/circuitpython/#open) - crop and resize to 550px, name yyddmmweblate.jpg
- Discord Users: Use **/serverinfo** in any channel to get the user count
- For Weblate graphic, go [here](https://hosted.weblate.org/widgets/circuitpython/), click the last one then copy the full size, cut down via photo editor and resize to 550px
- Get Deep Dive info from Adafruit YouTube [Live](https://studio.youtube.com/channel/UCpOlOeQjj7EsVnDh3zuCgsA/videos/live?filter=%5B%5D&sort=%7B%22columnType%22%3A%22date%22%2C%22sortOrder%22%3A%22DESCENDING%22%7D) and CircuitPython Parsec from John Park posting on the [Adafruit Blog](https://blog.adafruit.com/?s=parsec)

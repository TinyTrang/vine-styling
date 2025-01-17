To change vine styles you can install a browser extensions that inject CSS for you automatically every time that a page load.

# PC
A popular one for desktop (PC) on chrome and firefox is called stylebot, but you can use any extension that supports css injection.
Install with the links below depending on your browser:

https://chrome.google.com/webstore/detail/stylebot/oiaejidbmkiecgbjeifoejpgmdaleoha?hl=en-US

https://addons.mozilla.org/en-US/firefox/addon/stylebot-web/

- Open stylebot options and go to the tab "Styles"
- Click at "Add a new style..."
- in the "Enter URL..." field use: ```https://www.amazon.com/vine*```
- in the text area below insert the styles that you desire:
```
@import url(https://raw.githubusercontent.com/Thorvarium/vine-styling/main/desktop/small-items.css);
@import url(https://raw.githubusercontent.com/Thorvarium/vine-styling/main/desktop/remove-header.css);
@import url(https://raw.githubusercontent.com/Thorvarium/vine-styling/main/desktop/remove-footer.css);
@import url(https://raw.githubusercontent.com/Thorvarium/vine-styling/main/desktop/remove-associate-header.css);
@import url(https://raw.githubusercontent.com/Thorvarium/vine-styling/main/desktop/more-description-text.css);
@import url(https://raw.githubusercontent.com/Thorvarium/vine-styling/main/desktop/etv-modal-on-top.css);
@import url(https://raw.githubusercontent.com/Thorvarium/vine-styling/main/desktop/categories-with-emojis.css);
@import url(https://raw.githubusercontent.com/Thorvarium/vine-styling/main/desktop/pagination-on-top.css);
@import url(https://raw.githubusercontent.com/Thorvarium/vine-styling/main/desktop/collapsable-categories.css);
@import url(https://raw.githubusercontent.com/Thorvarium/vine-styling/main/desktop/striped-categories.css);
@import url(https://raw.githubusercontent.com/Thorvarium/vine-styling/main/desktop/ghost-limited-availability.css);
@import url(https://raw.githubusercontent.com/Thorvarium/vine-styling/main/desktop/rfy-afa-ai-tabs.css);

```
Those are the public styles that we created, if you don't want all of them you can remove the line that represents the functionality that you do not want.
For example ```@import url(https://raw.githubusercontent.com/Thorvarium/vine-styling/main/desktop/pagination-on-top.css);``` makes the pagination to be on the top of the page, just don't include this line if you dont want that.

### small-items.css:
- Show more items per row in the page
### remove-header.css:
- Removes the website header
### remove-footer.css:
- Removes the website footer
### remove-associate-header.css:
- Removes the website "Amazon Associates" header, in case you are an "Amazon Associate"
### more-description-text.css:
- Show a smaller font for each product on the grid and display 3 lines of description instead of 2
### etv-modal-on-top.css
- Show the ETV of the product on top of the modal instead of the bottom
### categories-with-emojis.css
- Show emojis on the left side of each category
### pagination-on-top.css
- Show the grid pagination on top instead of bottom
### collapsable-categories.css
- Collapses the categories on the left when not being hovered, good for when your screen is not very big
### striped-categories.css
- Change alignment and background color for the categories to improve readability
### ghost-limited-availability.css
- Change the text "Limited Availability" on the modal to be a ghost icon on the bottom left
### rfy-afa-ai-tabs.css
- Change the product tabs text to RFY | AFA | AI

## Customization
if you want to customize some specific style you can also open the files that you want to customize, copy the part that you want changed and include at the bottom of the stylebot file. This way you can tweak the numbers that you want customized.

Example:

```
@import url(https://raw.githubusercontent.com/Thorvarium/vine-styling/main/desktop/small-items.css);
/* ... all other imports ... */
@import url(https://raw.githubusercontent.com/Thorvarium/vine-styling/main/desktop/collapsable-categories.css);

#vvp-items-grid {
  grid-template-columns: repeat(auto-fill,minmax(75px,auto)) !important;
}

#vvp-items-grid .vvp-item-tile .vvp-item-tile-content {
  width: 75px !important;
}
```
This will make the items even smaller



# Android
For Android, we recommend a browser called "Kiwi Browser", this browser supports extensions. 

(Google chrome does not support extensions on android and firefox only have a limited quantity of extensions)

download: https://play.google.com/store/apps/details?id=com.kiwibrowser.browser&hl=en_US&gl=US

Inside kiwi browser you can install "Stylebot" as well

- Download the file https://raw.githubusercontent.com/TinyTrang/vine-styling/main/mobile/import-android.json here from the github (you can hold your finger on the link and click "Download Link")
- Open stylebot options and go to the tab "Sync" (Tab Styles does not work very well on mobile, not sure why)
- Click on "Import" and select the downloaded file


# iPhone
For iPhone, we recommend a browser called "Insight Browser", this browser supports extensions. 

download: https://apps.apple.com/us/app/insight-browser/id1531407280

(Safari does support extensions, but it also have a limited quantity)

Inside Insight Browser, go to settings and click on:
  - See all Extensions
  - Add a extension
  - Give it any name
  - Change the "IF" condition to: "url matches regex"
  - give it the value: ```^https:\/\/www.amazon.com\/vine```
  - change the "then" condition to "inject Css from URL"
  - use the url: ```https://raw.githubusercontent.com/Thorvarium/vine-styling/main/mobile/mobile.css```

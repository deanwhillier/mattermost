# Adding Icons

**NOTE: These docs need to be updated**

Simple steps to adding new icons to the Compass Icons font

## Icon Font Source Repository

Currently the font is being manually managed and lives in

[Google Drive / Shared Drives / Product Design / Compass Design System / Compass Icons](https://drive.google.com/open?id=1PbbhRVmXOI5BzC305qa42OjMtaVlLEYM&authuser=michael.gamble%40mattermost.com&usp=drive_fs)

In the mid-term this will be moved into a github repository, replacing this manual process with an automated build process.

## Adding Material Design Icons

#### Locate your icon

-   Go to https://materialdesignicons.com/ and search for the icon you want to add (stick to outline icon styles as per our [iconography](https://zeroheight.com/29be2c109/p/19c648-iconography) guide)
-   Download the icon as ".SVG Optimized"

![img](https://zeroheight.com/uploads/Lt4jIpNUur-Ru3LDReBQhw.png)

#### **Determine the Character code**

-   Locate the hexadecimal character code of the icon you just downloaded in the materialdesignicons.com [cheat sheet](https://cdn.materialdesignicons.com/5.3.45/) (use chromes find in page)

## Adding Custom Icons

#### **Create your icon**

-   Follow the design guide outlined under [Foundations / Iconography](https://zeroheight.com/29be2c109/p/19c648-iconography)
-   Once the icon is ready illustrator, be sure the shape is a single compound path, no extra layers or groups

![img](https://zeroheight.com/uploads/s2mNAoqq3dRjfDSH4pdpXQ.png)

#### Save and optimize your SVG

-   Choose to "Save As" an "SVG", ensuring to set the "Decimal Places" field is set to a value of "3" (This ensures your shapes are saved out with an accurate level of detail)

![img](https://zeroheight.com/uploads/ItnKCaKYUIaZI6yivtfBPQ.png)

-   Click the "SVG Code..." button
-   Copy the entire <path> tag

![img](https://lh3.googleusercontent.com/u7r8Pg2mTEVF-RpRMRT-1ujof1I38imiwDiw4gmXZHFqmw6IwwgOYFRalqVnB-qqBYTK1aMbo-BDJkyQ7utPVBc9k8Jh_uCD2vsH84ux6KqBsKaMpWeUIRMAHh3LwQASXZ7rX36i)

-   Open the optimized ["SVG Template.svg"](https://drive.google.com/open?id=1mZ1J-jL7WpSCUqTf7Mkd7OmhY--iFARS&authuser=michael.gamble%40mattermost.com&usp=drive_fs) located in the root of the repository in a text editor of your choice
-   Paste the <path> in your clipboard over the path in the template file and save as

![img](https://lh4.googleusercontent.com/8ueiY8uHIo9M-dP31EwqD1otnMKEtP6fRQ27bJRz-eh2knOf8iOrqDKBgvXOz-EAgbX8ApwlJbd4l0DVYgKmH2Bo3enXBSJ6Awz_aYbqxwUy6wHRdi9x_7NfFME0qzdbAx5meEdN)

#### **Naming your custom SVG**

-   Try to match the naming conventions used in the material design icon open source [cheetsheet](https://cdn.materialdesignicons.com/5.3.45/)
-   if the icon is the same concept then consider it a replacement and reuse the name (minus the mdi prefix)
-   if its something new, do your best to try and match for example "someconcept-outline.svg" as it would likely follow the outline style

#### Choosing the character code

-   In the same way as the naming, try to reuse the hexadecimal codes in the [cheetsheet](https://cdn.materialdesignicons.com/5.3.45/) if its a replacement icon
-   For anything new we have manually started using the "E800" block of hexadecimal numbers
-   You'll have to open the [demo.html](https://drive.google.com/open?id=1fEKMDa3hdaAunc7g8-inVKxH50PGYymO&authuser=michael.gamble%40mattermost.com&usp=drive_fs) from the repository root and click on the "show codes" checkbox to determine which is the next available in the sequence

![img](https://zeroheight.com/uploads/GARvZikyhx4OzBDKhsqtrw.png)

-   As you can see in the example above "E814" is the last icon in that "E800" block, so your icons character code should be "E815"

## **Adding Jumbo Icons**

#### **Create your icon**

-   Follow the design guide outlined under [Foundations / Iconography](https://zeroheight.com/29be2c109/p/19c648-iconography) (As of writing this Jumbo Icon design guides do not exist but will be included in future iterations - in the interim please consult with the UX Design Team)

#### **Naming your jumbo SVG**

-   Prefix your file name with "jumbo-" such as "jumbo-attachment-code"

#### **Choosing the character code**

-   Similar to the custom icons, we have designated the "E900" block of hexadecimal character codes for the jumbo icons.
-   If you open up the demo.html from the repository root and click on "show codes" you'll be able to look through the "E900" block to determine the next available code in the sequence.

![img](https://zeroheight.com/uploads/75p43oewkYy99-9-aA6KAw.png)

-   As you can see in the example above "E90B" is the last icon in that "E900" block, so your icons character code should be "E90C"

## **Move and rename**

-   Move the downloaded or optimized svg file into the "svgs" folder in the repository location (google drive location linked above)
-   Append the identified hexadecimal character code to the filename after a pipe character e.g. "account-outline|F0013.svg"

## Import into Fontello

#### **Load Fontello config file**

-   Go to http://fontello.com/
-   Drag and drop "config.json" from the repository location to the "Custom Icons" section in Fontello

![img](https://zeroheight.com/uploads/LlBXGzpDKUk436WAfY9osw.png)

-   The latest version of the compass icon font will load into Fontello

#### **Add your new icon to the font**

-   Drag and drop your new icon into Fontello's "Custom Icons" area
-   Click on the new icon in the grid, selecting it with a red circle ensuring it will be included in the export

![img](https://zeroheight.com/uploads/WIOwW5rhyEcJhAavH-AYfg.png)

-   Click the pencil icon to open the "Glyph options"
-   Move the hexadecimal code from the "Default (css) name" to the "Default code (hex), mapping the glyph to the appropriate character code in the font

![img](https://zeroheight.com/uploads/KYy0kP1IboazlvNgTPHmgg.png)

## Update The Repository

-   Once you're done adding new icons, click on the "Download webfont" button in Fontello

![img](https://zeroheight.com/uploads/ghjfoUdkE7_oSVaq77bKoQ.png)

-   Cut, paste and overwrite the contents of the archive into [the repository](https://zeroheight.com/29be2c109/p/22cae9-adding-icons/t/163ebe) (google drive folder mentioned above)
-   Once the repository is updated, make a post in the Mattermost "[Compass Design System](https://community-daily.mattermost.com/core/channels/compass-design-system)" channel mentioning the "@uxteam" asking for the font to be updated in Figma

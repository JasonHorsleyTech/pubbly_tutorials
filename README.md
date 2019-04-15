# Pubbly Tutorials

This repository will step you through the creation of a Pubbly program, through the use of the many open sourced tools. This tutorial relies on the following tools,

* Pubbly Design Tools. [Repository]() see section Installation
* Pubbly Console. [Repository]() see section Installation
* Cordova CLI. [Offsite link]() see section Installation

## Program overview.

Our program will used some of the open sourced assets from TeamCCI's Xprize submission. You are free to use these in any way you'd like, according to the Apache 2.0 license.

Our program will have a custom HTML5 front end, and some other fucking shit idk.

Keep in mind, these tutorials are created to teach content creators how to use the pubbly system. As such, the content is placehold, and of little educational value

## Authoring a Design Tools export.

> Prerequisites: Installation of the Pubbly Design Tools

* Run the Pubbly Design tools
* Download and extract [this asset folder]()

One of the methods Pubbly used to teach reading was by phonetic syllable. Since Swahili is a very regular language (each syllable is only ever pronounced one way), we though it would be good to teach every syllable's sound, then how syllables fit together to form words. We're going to make a simple 2 page export. The first page will show a syllable (Be) and pronounce it. The second page will show that syllable in a known word (Bega), a picture of that word, and prompt readers to DragDrop the syllable to a partial word to complete it.

#### First page: Structure

* From Pubbly Design, create a new book.
    * File -> New
* Name it "Words by Syllables", and select "Single Page"
* Add image "background_marsh.png"
    * Add -> Images or Video -> Choose background_marsh.jpg
> You can also add images with "Control + I"
* Right click the image and select "Page size to image size"
* When prompted to make "Background image", select yes
> Background images are permanently Top Left, and cannot be moved.
* Add a new image "Be_syllable.png"
    * Add -> Images or Video -> Choose Be_syllable.png
> Pubbly accepts png, jpg, jpeg, gif, mp4 and avi image/video types
* Center it on the page
    * Click and drag an image to move it
* Draw a new Rectangular Link around it
    * At the top right of your Tools page, select the Rectangle tool
    * Choose "Link"
    * Draw a rectangle around "Be"
* Rename your Link "Syllable"
    * At the top middle of the Tools page, find the blue word "Object"
    * Click that word to cycle through the Tools tab.
    * Stop at "Links" tab.
    * Double click "Link 1", first column
    * Enter the new name "Syllable", and press enter
* Add a new Audio target, which plays the syllable's sound
    * Right click row "Link 1" column "Target"
    * Select "Audio -> Audio"
    * Select "Be_syllable.wav"
> Pubbly accepts mp3, ogg and wav audio types
> You can also add images with "Control + I"
* Preview that Target
    * Left click the Target "play audio Be_syllable"
    * In the top right, select the "Play" icon
    * You should hear "Be_syllable.wav"

#### First page: Animation

Although functional, this book is a little boring. Lets add an animation on the Syllable.

* Select the Polygonal tool (Tools window, top right icon)
* Select "Animation"
* Click the DARK area of the "be" image (This will start an animation at the center XY of the image)
* Double click somewhere else on screen to end the animation


* Open the Animations specs window
    * Tools window -> Anim -> Anim specs
* "Be_syllable - Animation_1" should already be selected

* Cycle through the Tabs "Click Blue tab titles" until you're on the "Animation" tab
* Select your animation 
    * Anim -> Be_syllable -> Animation_1
* Preview this animation by clicking the "Play" icon (Tools window, top right)

While the animations tab is open, the preview button plays your selected animation. The syllable image will move from it's X,Y to where ever you ended the animation. The two rows in the Tools window represent the two legs of that animation.

* Reset your page
    * Go -> Reload page -OR- Control + R
* Manually edit your animation
    * Set the second row's top left to the same as the first row's top left
    * Set the first row's height to "0%"
    * Set the first row's width to "0%"
    * Set the first row's Rotate to 1
    * Replay your animation
    * You should see your image grow from 0% to full size in a quarter of a second
> The Design Tools preview mode is an _estimation_ of what things will look like. Due to startup limitations, more effort was placed on _works_ than _pretty_. While things can lag in the Design Tools, only you the author will see it. The browser based runtime environment is a smooth end user experience.
* Rename this animation "transition_spinGrow"
    * Tools window -> Anim -> Anim Specs
    * Rename

Create a few new transition animations, such as a slide from top to middle, a fade in, or a spin in. Get creative. (For the purposes of this tutorial, make at least one more)

* Go to your links tab
* Add a new Target to your Syllable link
    * Right click Target column
    * Select "Object - Single"
    * Select object "Be_syllable"
    * Select animation "transition_fadeIn"
    * Click "Add Randomality
    * Select ALL of your animations
    * Select Add
    * Select OK
* Preview your link
> Although you can preview individual targets with the top right "Play" icon, a Link must be triggered from preview mode
* Tools window -> Go -> Preview -OR- Control + P
* Left click your link
    
You should see one of the animations you drew, and hear the audio for "Be". Re-clicking this link (enough) should randomly select a different animation

#### First Page: Conditional links

This book is functional and somewhat fun, but requires user input. Lets add some more functionality, specifically, lets make this book start on it's own

* Add a new Open Page link
    * Tools window -> Add -> Conditional Links -> Open Page
> A conditional link is a link triggered by certain conditions being met (NOT by direct user input)
* Add a new target to your conditional link (Right click empty target column) of Object Single
* In the Select drop down, choose "Links -> Syllable"
* Click the box "Send" choose "Click" and select "OK"
* Enter preview mode (Control + P)

> When the page opens, your Syllable will get a simulated "Click" from the Open Page's first target. Note, after the sequence of events finishes, you can "reclick" the "Syllable" link yourself.

Now your book opens and runs all by itself!

#### Second page: Structure

Lets add a second page, that shows how the "Be" syllable fits into a word.

* Tools window -> Add -> Blank Page
> Your blank page will have the same dimensions as the last... Changing page dimensions effects ALL pages.
* Add the marsh image, and set as a background.
* Add the "Bega_picture" and "Be_partial" images.
* Add a new "Open Page" link
* Add a new target of "Play audio 'Be_picture'

> 

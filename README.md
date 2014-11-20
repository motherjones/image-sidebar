Clean image sidebar and inline horizontal sidebar
=============
Sometimes you need a clean image-driven sidebar, or a horizonatal sidebar. They're handy. Let's take a look at the vertical image sidebar:

<p align="center">
  <img width="50%" src="https://github.com/motherjones/image-sidebar/blob/master/img/Screen%20Shot%202014-11-20%20at%2012.56.16%20PM.png" alt="screenshot"/>
</p>

## Examples in the wild (vertical)

[Want to Find Out Where Your Fruit Was Grown? Good Luck]
(http://www.motherjones.com/environment/2014/09/fruit-veggies-produce-origins-trade-secret)

## How it works

*MoJo users:* Before you get started, following [these instructions](https://github.com/motherjones/story-tools#starting-a-new-project).

The vertical sidebar is essentially just a list with images in it. Gather your images, gather your text, and you've got a list. You'll need to upload your images somewhere that will give them unique URLs (MoJo staffers, use S3) and then you'll be good to go. 

### Modify the index.html file

By now you should have this entire repo downloaded locally. In the index.html file, look at the HTML starting at line 55: 

```html
    <li>
        <img class="list-pic" src="YOUR IMAGE URL GOES HERE" alt="IMAGE OF SOMETHING">
          <p>
              <span>TITLE OF LIST ITEM HERE:</span> Short sentence here or something like that. Keep it pithy.
          </p>
    </li>
  ```
You can add as many < li >  < /li > items as you want. You could have one or a gagillion. Up to you. Just grab the opening and closing tags. The index.html file shuld also have all the styling you need, and can be adjusted there. Some CMSs might require you to copy that out and put it in a CSS field (ours does) but that's simple.

Voiala! You have a vertical image side bar. Now let's take a look at the horizontal image bar:

<p align="center">
  <img width="50%" src="https://github.com/motherjones/image-sidebar/blob/master/img/Screen%20Shot%202014-11-20%20at%202.44.12%20PM.png" alt="screenshot"/>
</p>

## Examples in the wild (horizontal)

[Chart: As Top Tax Rates Dropped, Top Incomes Soared](http://www.motherjones.com/mojo/2014/09/income-inequality-tax-rates-income)

## How it works

Again, all we're really talking about here is a a series of divs that have a thumbnail image and some text that can be linked out. Pretty straightforward. The styling contained within the index.html file should take care of lining it all up for you. 

### Modify the index.html file (horizontal)

Again, you should have all of these files locally at this point. Make sure you're grabbing the index.html file from the horizontal directory in the repo. The HTML is a bit different. In that file, look for the div that begins at line 55: 
```html
<div class="row">
    <a href="LINK TO ANOTHER PAGE GOES HERE" target="_blank"><div class="col-xs-3">
      <h5 class="caption">Back to the Future</h5
        <a href="#" class="thumbnail">
        <img src="YOUR IMAGE URL GOES HERE" alt="WORD FOR IMAGE">
    </a>
</div></a>
```
Again, each of your images will need to be uploaded somewhere and have a unique URL. That goes in the middle there next to the "img src=". For MoJo, our shell is 630 px wide, so we've found that four images at 125px x 125px seems to work best. Your shell might be different. Do the math accordingly, size your image, and drop those URLs in. If you want more than one row, look for the div that starts with <div class="row" and just keep adding them. We're all on our own journey.

Once you've added in your images, save your index.html file and upload that to your server. The best way to do this is to iframe the whole thing. It's pretty straighforward [(here's how to make an iframe)](http://www.w3schools.com/tags/tag_iframe.asp). This is what ours looked like for this project: 

```html
<iframe frameborder="0" height="198" scrolling="no" src="YOUR INDEX.HTML URL GOES HERE" width="WIDTH YOU WANT"></iframe>
```
That should do it! You've made internet!

## Questions?

Hit us up by email, or Twitter: [@jaeahjlee](https://twitter.com/jaeahjlee) or [@tasneemraja](https://twitter.com/tasneemraja)

## License
Copyright (c) 2012 Mother Jones

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
You can add as many <li></li> items as you want. You could have one or a gagillion. Up to you. Just grab the opening <li> tag and the closing </li> tag.

[Horizontal sidebar example](http://www.motherjones.com/mojo/2014/09/income-inequality-tax-rates-income)

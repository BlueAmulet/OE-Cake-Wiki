`   `<img src="/images/Helper.png" title="fig:Helper.png" width="400" alt="Helper.png" />

**OE-Cake Recipe Helper** is a Windows application developed with the aim of making testing and analyzing OE-Cake [recipes](/recipes.md "recipes") easier. <s>It can be downloaded from [here](http://code.google.com/p/oecake-recipe-helper/)</s>.

The original download no longer works. [This recompiled version](https://drive.google.com/uc?id=11aoZ14yKTquotgVhK8eKW2v50dRGlelb) works as of 2020-10-05. ([Mirror download](https://lbda.net/NVSl.zip))

## Guide to usage

### Analyzing recipes

`   Enter any recipe in the top-left hand textbox and click 'Analyze!'. The recipe's constituent materials will be listed in the box below, and any other unusual properties in the larger box to the right. Note: The properties are predictions, and may not be accurate, especially in extreme combinations! The 'Condensed form' of the recipe is the essential code needed to mix all the constituent materials, without any duplicated (and thus nullified) or irrelevant characters.`

### Sending recipes to OE-Cake

`   Make sure that OE-Cake is running, then click the 'Send to OECake' button. The recipe currently loaded is sent, ready to be drawn, without having to faff about with {ESC}code{ESC}. This function will only work if the recipe has been 'analyzed', as it is only the 'condensed' or essence form of the recipe that is sent to OE-Cake.`

### Recipe databases

`   *`  
`       Clicking 'Add current recipe' will add the info about the currently analyzed recipe to the listbox in the lower half of the window. The comment is (logically) taken from the 'Comment' textbox.`

`   *`  
`       Tags can be added to the recipe, each separated by a comma. These are useful when filtering recipes (see below).`

`   *`  
`       'Save'/'Load' allow you to save the listbox to a database file on your computer.`

`   *`  
`       'DL from wiki' fills the listbox with the data from the 'Recipes' page here, thus allowing you to test out all the recipes from the wiki without having to tap them in manually!`

### Filtering

`   *`  
`       Check the checkboxes corresponding to the elements you want the filtered recipes to contain.`

`   *`  
`       Enter the tags you want the filtered recipes to have, again each separated by a comma.`

`   *`  
`       Either one of the above filters is optional, but obviously leaving both blank will result in an error!`

`   *`  
`       Note: When you save the database, only the set of recipes (incl. comments, tags, etc.) is saved, not the filter. Saving filters will be 'coming soon' in v0.4!`

## Uploading to the wiki

`   `<img src="/images/Uploadtoweb.png" title="fig:The upload dialog box" width="350" alt="The upload dialog box" />

As of v0.3, Recipe Helper supports uploading recipes to the wiki's [Recipes](/Recipes.md "Recipes") list. Please use this feature responsibly.

`   *`  
`       Have the recipe you want to upload in the top sections, either by entering it and clicking 'Analyze!', or double-clicking it in a database.`

`   *`  
`       Click 'Send to wiki', and the dialog box shown to the right will appear.`

`   *`  
`       Selecting 'Full recipe' will upload the uncondensed, full form, selecting 'condensed' will upload only the 'essence' form.`

`   *`  
`       Feel free to add/edit the comment you want next to the recipe.`

`   *`  
`       Select the section you wish to add the recipe to, then click 'Send to wiki'. A dialog box should pop up in a few seconds telling you that the operation has been successful!`

`   *`  
`       Note: The recipe will be added using the `[`special`` ``user`` ``account`](/UserOECake%20Recipe%20Helper.md "User:OECake Recipe Helper")` designed for this purpose.`

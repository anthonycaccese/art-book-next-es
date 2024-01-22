# Art Book Next for EmulationStation
A simple theme for the version of EmulationStation used in [Batocera](https://batocera.org/).
Based on the style of a coffee table book.

This version of the theme works with all distributions that leverage the Batocera fork of EmulationStation.  This includes [Batocera](https://batocera.org/) and [RetroBat](https://www.retrobat.org/)

## Preview
| ![system view](https://github.com/anthonycaccese/art-book-next-es/assets/1454947/c0252388-2268-444c-ae3d-07f15b87a98c) | ![menu](https://github.com/anthonycaccese/art-book-next-es/assets/1454947/39653703-f6e8-4940-98fc-66ce1c5af271) |
| -- | -- |
| ![gamelist-view-1](https://github.com/anthonycaccese/art-book-next-es/assets/1454947/e8251f3c-f033-43ed-8b55-f3a93c28131a) | ![gamelist-view-2](https://github.com/anthonycaccese/art-book-next-es/assets/1454947/fadfba3e-54a4-48e2-a11c-39c52797dc56) |


## Theme Configuration

The following options can be changed directly from the main menu under `UI Settings > Theme Configuration`

| Setting | Description | Options |
| -- | -- | -- |
| Distribution | Used to define which folder to look in for Theme Customization files. | `Batocera`, `RetroBat` |
| Aspect Ratio | Enables you to select the correct aspect ratio for your screen.  This will automatically set itself so you should not need to change it but if the theme layout looks odd or spacing looks incorrect you can use this setting to make sure the aspect ratio matches your screen. | `16:9`, `16:10`, `4:3`, `3:2`, `5:3`, `1:1` |
| Color Scheme | Sets the color scheme that is used for the theme.  There is a set of prebuilt color schemes that you can select and an option to supply your custom color scheme (selected by choosing `custom`).  You can see details on customizations below under [Theme Customizations](#theme-customizations). | `Art Book Next`, `Art Book`, `Steam OS`, `SNES`, `Famicom`, `Black`, `Grayscale`, `Custom` |
| Font Size | When this is set to custom it allows you to define custom font sizes for the gamelist.  You can see details on customizations below under [Theme Customizations](#theme-customizations). | `Default`, `Custom` |
| System View Style | Defines the layout/design used for the System View | `Multi Artwork`, `Centered Artwork (Multiple Logos)`, `Centered Artwork (Single Logo)`, `No Artwork`, `Custom` |
| Gamelist View Style | Defines the layout/design used for the Gamelist View | `Metadata On`, `Metadata On (Immersive)`, `Metadata Off`, `Metadata Off (Immersive)` |

## Theme Customizations

Art Book Next allows customizations to artwork, colors and fonts without the need to edit the source XML.  This enables you to change the look of the theme and still retain any changes when your OS is updated.

### Start Here
- Make sure the `Distribution` setting is set to the correct value for your current OS (e.g. Batocera, JELOS or RetroBat)
- This value determines the folder where you will add your customizations
    - Batocera = `userdata/theme-customizations/art-book-next/`
    - Retrobat = `C:\RetroBat\emulationstation\.emulationstation\theme-customizations\art-book-next\`
- Create the folders that match your distribution and then move on to the options below...

### Background Art

The artwork used on the system view can be customized with your own images.  You can create either `centered` or `full screen` variations.

- Create a folder in the path you created above called `backgrounds`
- Upload your custom background images to that folder
- They can be named:
    - _default.jpg
    - _default.png
    - ${system.theme}.jpg
    - ${system.theme}.png
- The theme will look them them up in that order.  If a given image is not found in your folder then the the images from the theme will be used as a fallback.  This allows you to customize only the images you want and still have images displayed for all systems.
- `_default.jpg/png` can be used for creating a single image that is used for all systems OR a fallback for systems that you did not create a custom image for (if you don't want to use the fallback that already exists in the theme)
- `${system.theme}.jpg/png` should be named for the system you are looking to override.  For example if you wanted to override the artwork for `snes` you would create an image called `snes.jpg` or `snes.png` in the backgrounds folder
- once your images are in place you turn on custom images by changing the System View Style to either...
    - Centered Artwork (Custom)
    - Multi Artwork (Custom)
    - Fullscreen Artwork (Custom)
    - *I added these options so you could switch off custom artwork without needing to delete your customizations*

To create `centered` artwork that matches the mask used in the theme you can use the `system-art-mask` files I supply in the theme's resources directory [here](https://github.com/anthonycaccese/art-book-next-es/tree/main/resources/customizations).  I have tried to include a mask that should work in each major editing program.

If you create a set of images that you would like to share with the community please let me know about it [here](https://retropie.org.uk/forum/topic/33010/theme-art-book-next)

### Color Schemes

You can create your own custom color scheme to use for the theme

- Download this template: https://github.com/anthonycaccese/art-book-next-es/blob/main/resources/customizations/colors.xml
- Upload it in the path you created above and make sure its called `colors.xml`
- Change any values in the template to the colors you prefer.
- I tried to make the values as self explanatory as possible but if you have questions regarding which property does what please don't hesitate to ask.
- After your colors are defined; in theme configuration change `Color Scheme` to `Custom`

### Logos

The logos used on the system and gamelist views can be customized with your own images.

- Create a folder in the path you created above called `logos`
- Upload your custom logo images to that folder
- They can be named:
    - ${system.theme}.svg
    - ${system.theme}.png
- The theme will look them them up in that order.  I recommend SVGs as they scale better on different resolutions.
- `${system.theme}.svg/png` should be named for the system you are looking to override.  For example if you wanted to override the artwork for `snes` you would create an image called `snes.svg` or `snes.png` in the logos folder
- Once your images are in place you turn on custom logos by changing the Color Scheme to `Custom`

### Fonts

You can modify the font size used to display gamelists

- Download this template: https://github.com/anthonycaccese/art-book-next-es/blob/main/resources/customizations/fonts.xml
- Upload it in the path you created above and make sure its called `fonts.xml`
- Change any values in the above template to the sizes you like.
- After your sizes are defined; in theme configuration change `Font Size` to `Custom`

## **Additional Notes**

### Versions for other ES forks:
* If you use Retropie... then check out the version [here](https://github.com/anthonycaccese/art-book-next-retropie).  The Retropie version has all the same base features but you have to change them through the XML directly (as Retropie's theme engine does not have a menu for changing theme options)
* If you use ES-DE... then the ES-DE version [here](https://github.com/anthonycaccese/art-book-next-es-de) will work out of the box with that distribution.  When used with ES-DE the theme comes with additional support for navigation sound sets.
* If you use JELOS... then the version [here](https://github.com/anthonycaccese/art-book-next-jelos) will work out of the box with that distribution.

### **Acknowledgments**
* Most system logos were sourced and modified from the excellent work done by Dan Patrick [here](https://archive.org/details/console-logos-professionally-redrawn-plus-official-versions).  I modified each to be compatible with EmulationStation's current SVG support.
* ChangaOne font is by [Eduardo Tunni](https://www.fontsquirrel.com/fonts/changa)
* Oxygen font is by [Vernon Adams](https://www.fontsquirrel.com/fonts/oxygen)
* Auto-Collection Genre background art created by [@nautipuss](https://github.com/nautipuss)

## **License**
Creative Commons CC-BY-NC-SA - https://creativecommons.org/licenses/by-nc-sa/2.0/
You are free to share and adapt this theme as long as you provide attribution back to me (and the above credits) as well share any updates you make under the same license terms.

Thank you for taking a look at this 😄

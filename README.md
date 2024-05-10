# Art Book Next for EmulationStation
A simple theme for the version of EmulationStation used in [Batocera (v39 and above)](https://batocera.org/).
Based on the style of a coffee table book.

This version of the theme only works with distributions that use the latest Batocera (v39 and above) fork of EmulationStation.  Specifically [Batocera](https://batocera.org/), [Knulli](https://www.knulli.org/) and [RetroBat](https://www.retrobat.org/)

## Preview
| ![system view](https://github.com/anthonycaccese/art-book-next-es/assets/1454947/c0252388-2268-444c-ae3d-07f15b87a98c) | ![menu](https://github.com/anthonycaccese/art-book-next-es/assets/1454947/39653703-f6e8-4940-98fc-66ce1c5af271) |
| -- | -- |
| ![gamelist-view-1](https://github.com/anthonycaccese/art-book-next-es/assets/1454947/e8251f3c-f033-43ed-8b55-f3a93c28131a) | ![gamelist-view-2](https://github.com/anthonycaccese/art-book-next-es/assets/1454947/fadfba3e-54a4-48e2-a11c-39c52797dc56) |

## Theme Configuration

The following options can be changed directly from the main menu under `UI Settings > Theme Configuration`

| Setting | Description | Options |
| -- | -- | -- |
| Distribution | Used to define which folder to look in for Theme Customization files. | `Batocera/Knulli`, `RetroBat` |
| Aspect Ratio | Enables you to select the correct aspect ratio for your screen.  This will automatically set itself so you should not need to change it but if the theme layout looks odd or spacing looks incorrect you can use this setting to make sure the aspect ratio matches your screen. | `16:9`, `16:10`, `4:3`, `3:2`, `1:1` |
| System Artwork | Defines the set of artwork that is displayed on the system view | `Default`, `Noir`, `Custom` |
| Game Artwork | Defines the type of artwork used to represent a game. These are sourced from the the selections you make in the scraper menu. Image will display the image you selected to scrape for `Image Source`.  Image (Cropped) will display that same image zoomed in to fill the screen.  Boxart will display the image you selected to scrape for `Box Source` | `Image`, `Image (Cropped)`, `Boxart` |
| Game Metadata | Sets if metadata (e.g. description, release date, etc...) should be displayed for a game | `On`, `Off` |
| Font Size | Set the size for text elements throughout the theme. | `Default`, `Small`, `Large` |
| Color Scheme | Sets the color scheme that is used for the theme.  There is a set of prebuilt color schemes that you can select and an option to supply your custom color scheme (selected by choosing `custom`). You can see details on customizations below under [Theme Customizations](#theme-customizations). | `Default`, `Light`, `Steam OS`, `SNES`, `Famicom`, `DMG`, `OLED`, `Custom` |

## Theme Customizations

Art Book Next allows customizations to system artwork and color schemes without the need to edit the source XML.  This enables you to change the look of the theme and still retain your changes when the theme is updated.

### Start Here
- Make sure the `Distribution` setting is set to the correct value for your current OS (e.g. Batocera/Knulli or RetroBat)
- This value determines the folder where you will add your customizations
    - Batocera/Knulli = `/userdata/theme-customizations/art-book-next/`
    - Retrobat = `C:\RetroBat\emulationstation\.emulationstation\theme-customizations\art-book-next\`
- Create the folders that match your distribution and then move on to the options below...

### Background Art

The artwork used on the system view can be customized with your own images.

- Create your custom artwork using one of the masks i've supplied in this theme's resources directory [here](https://github.com/anthonycaccese/art-book-next-es/tree/main/resources/customizations). I have tried to include a mask that should work in all major image editing programs.
- Export each custom image as a transparent png.
- Create a folder in the path you created above called `artwork`
- Upload your custom images to that folder
- They can be named:
    - _default.png
    - ${system.theme}.png
- The theme will look them them up in that order. If a given image is not found in your folder then the the images from the theme will be used as a fallback.  This allows you to customize only the images you want and still have images displayed for all systems.
- `_default.png` can be used for creating a single image that is used for all systems OR a fallback for systems that you did not create a custom image for (if you don't want to use the fallback that already exists in the theme)
- `${system.theme}.png` should be named for the system you are looking to override. For example if you wanted to override the artwork for `snes` you would create an image called `snes.png` in the artwork folder.
- Once your images are in place you turn on custom images by changing the `System Artwork` setting to `Custom`

If you create a set of images that you would like to share with the community please let me know about it [here](https://retropie.org.uk/forum/topic/33010/theme-art-book-next)

### Color Schemes

You can create your own custom color scheme to use for the theme

- Download this template: https://github.com/anthonycaccese/art-book-next-es/blob/main/resources/customizations/colors.xml
- Upload it in the path you created above and make sure its called `colors.xml`
- Change any values in the template to the colors you prefer.
- I tried to make the values as self explanatory as possible but if you have questions regarding which property does what please don't hesitate to ask.
- After your colors are defined; in theme configuration change `Color Scheme` to `Custom`

## **Additional Notes**

### Versions for other ES forks:
* If you use Retropie... then check out the version [here](https://github.com/anthonycaccese/art-book-next-retropie).  The Retropie version has all the same base features but you have to change them through the XML directly (as Retropie's theme engine does not have a menu for changing theme options)
* If you use ES-DE... then the ES-DE version [here](https://github.com/anthonycaccese/art-book-next-es-de) will work out of the box with that distribution.  When used with ES-DE the theme comes with additional support for navigation sound sets.
* If you use JELOS... then the version [here](https://github.com/anthonycaccese/art-book-next-jelos) will work out of the box with that distribution.

### **Acknowledgments**
* Most system logos were sourced and modified from the excellent work done by Dan Patrick [here](https://archive.org/details/console-logos-professionally-redrawn-plus-official-versions).  I modified each to be compatible with EmulationStation's current SVG support.
* ChangaOne font is by [Eduardo Tunni](https://www.fontsquirrel.com/fonts/changa)
* Auto-Collection Genre background art created by [@nautipuss](https://github.com/nautipuss)
* Metadata Icons sourced from [FontAwesome](https://fontawesome.com/search?o=r&m=free)
* The `Noir` System Artwork set was created and provided by [tenlevels](https://www.reddit.com/user/tenlevels/) with help from f8less and inspired by the artwork from the Epic Noir theme by chicuelo
* Thank you to [GenoCL](https://genocl.carrd.co/) for the idea of the multi-artwork system view.  It got me to think about ES themes in a different way when building it out and it came out awesome.

## **License**
Creative Commons CC-BY-NC-SA - https://creativecommons.org/licenses/by-nc-sa/2.0/
You are free to share and adapt this theme as long as you provide attribution back to me (and the above credits) as well share any updates you make under the same license terms.

Thank you for taking a look at this 😄
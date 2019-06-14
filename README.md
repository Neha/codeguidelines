# Front-End Code Guidelines
## A short code guidelines' guide for every front-end developer

Hello Folks!! Working in Front-end domain from few years I know how important is to have a single source for the code guidelines. Here is some guidelines I learned over years. This is still work in progress. If you have any suggestion, questions or feedback reach me.

[Website](https://www.codeguidelines.com/)

## Agenda
- [CSS](#agenda)
- [SCSS](#scss)
- [HTML](#html)
- [JAVASCRIPT](#javascript)
- [IMAGES](#images)
- [TOOLS](#tools)

## CSS
- **Code division** : divide the code into moduls and write CSS accrodingly. Keep the Global , base, and reset CSS on top always.
- **Grouping** : Group the same style and modules together
- Use CSS3 variables and write them on the top.
- Do not turn off outline and focus property. They are important for accessibility
- Use pre-processor such as SCSS, LESS. To have Modular CSS
- Aviod using @import in CSS. As it do HTTP request.
- Class Name Methodology : use BEM, SMACS or you can have your own Methodology too. The underline message is to have pattern to write the css.
- Either use _ or - or camelCase. Do not merge all three way together. Which is the best? Depends on the methodology you are going to follow.
- No space between the key and colon and 1 space after the colon.
- Do not forget to put ;.
- Class names should start with smaller case and avoid starting the name with numerals.
- Multiple properties always come in multiple line.
- No measurement unit after 0.
- `font-weight : bold` should be in numeric rather than 'bold', 'normal'. Reason is th web engine convert normal to 800. Basicailly convert string to numeric.
- Color values should be in lowercase.
- RGBa is faster than hexa.
- While implemting the colors in CSS. Use the chrome tools to test the contrast ratio for accessibility.
- Do not control content from CSS such as uppercase, lowercase.Until it is important.
- Avoid adding !important
- Identify the critical CSS of the your pages and place it on the head
- Class names should be very clear. But longer classname will affect the size of bundle.So, choose them wisely.
- Classname should be self explanatory such as: .header-title , .header-body
- If the style is going to be used globally do not bind it with the any module. Instead of writing .header-title-error write .error and so on.
- Use the build packages to minify the css files.
- Put comments only when and where it is required.
- Use single-quotes when targeting attributes input[‘required’]
- Use inbuild attributes over making classes.
- Avoid more than 3 nesting as specifity will be slow. CSS read from right to left #id – faster .classname – fast Tagname – fast Div span ul li .text – slow
- Complier arrange the css properties alphabetical. If you can also do same good.
- Short-hand properties vs writing explicit property padding:0 10px; padding-top:0; padding-bottom:0; vs padding-left:10px; padding-right: 10px;
- Avoid styling HTML tags unless you are sure it will be like that
- Typography: always have fall back font-family
- Use rem for text, px for spacing, % for widths
- Responsive – use media queries.
- Polyfills for auto-prefixer
- Use single-quotes
- Calc() function
- Use CSS3 features such as flex, css grids, @support
- Use css3 gradients etc over gradient-images.
- CSS Animations over JS animations.
- To avoid the opacity issues cross browser use colors.
- Focus on progressive enhancement.

## SCSS
- Do not write scss in one file
- Use the modular file approach.
- Create the SCSS files for - Base, varibales, components, typography , layout etc.
- Unless and until you don't have the requirement to have sepreate CSS files. Import all the SCSS files into one SCSS file.
- SCSS is very popular because it support nested css. This helps in writing better organzied code avoid nesting exceed more than 3 level
- Use & whereever you can
- Use SCSS functions to make the colors dark, light etc
- Use SCSS mixins. They are super helpful to have consisitency in your code.
- Use placeholder,/span> for re-use and inheritance but be careful with placeholders. It can bloat css.
- While using SCSS variables write default values.
- Do not forget to use SCSS varabiles. Though now CSS3 also provide varaibles but to have cross-browser support. Use SCSS variables.
- If the value will be used with calc() do not make the scss varaibles
- Use SCSS functions.
- Keep eye on bloating css generation

## HTML
- Use HTML5
- Use **semantic code**
- **Validate** your HTML.
- Use right tag for right thing.If there is a redirectionanchor if there is an action button. Cart??
- when there is clear understanding about the what is section and div is for division of the page.
- Avoid inline css & javascript.
- Always have mobile first approach. Use viewport meta tag.
- Do not put block elements into the inline elements.
- Use p tag for content.
- Keep your HTML clean. Do not add extra tags and classes
- Do not add unnecessary IDs or classes
- Always have a wrapper of your HTML page.
- While creating a module which is not supported in HTML. Add role=””.
- Follow the Heading hierarchy.
- Put defer and async with blocking scripts
- While writing footer text or legal text , use small tags
- Avoid using the bold and italic from markup. These can be handle by css classes.
- If you are sure about the HTML structure then avoid adding css classes at every level. You can write the style by targeting the parent level only
- Doctype is important. Do not avoid them.
- With Forms use legend.
- In input fields Use placeholder property but use label too for accessibility.
- Hiding text from the page is not good practice.
- Add move to top functionality if your website has longer scroll.
- Do not just relay on icons add the label, alt, and title tag to make them accessible.

## Javascript
- Always use a Javascript pattern to write your code.
- Use ES6+ syntax.
- Where ever you need this context use fat-arrow or Lambda functions.
- Constructor should have all the initial setup values
- In your JS you should have minimal DOM manipulation.
- Avoid hardcoding the values in Javascript.
- Values that are not going to change should be declared with const such as API Keysand the name should be always in uppercase.
- Should have a constant file in your project.
- All the API Keys and config key(s) should be in config files
- In Javascript world, do not forget semi-colon
- Use indentation for code readbility.
- Add comments only when required
- For performance, cache the length of the arrays and objects. Espically if your code require iteratation on it.
- variables and results,Use data-types such as arrays and objects wisely.
- Identify which data-type would be better in which operation. Eg: deleteing elements from array could be expensive as compare to the objects.
- While creating the method or variables name. Use same pattern througout your code.
- Avoid using many loops. Loops are expensive. Look into data and understand if for() , for..in(), for—each() or while could be better
- Write error handling code.
- Use build tools – webpack, parcel etc
- Use babel/Typescript , when you are using ES6+.
- While doing the build always change the version number in your package.json
- Avoid adding/deleting style from Javascript.Instead use class names to add / remove styles.
- Javascript can also lead to security issues. While writing your code especially if you are creating APIs keep the security testing in mind.
- Write reusable code.
- Avoid polluting Global scope
- For block level scope always use /const.
- Use shothand syntaxs only when necessary. Code readability is important too
- use strict mode. If not using ES6+ or Typescript.
- Use literals declaration where ever you can.
- Use functional programming.
- Clean the console.log() and alert() before the deployment.
- Make use of Tree shaking and chunk-loading by using build tool like Webpack to break the long code file.
- Use modulas import/export to write modular javascript.
- As Javascript don't have strict garbage collection, you need to be careful about what all is getting into the memory unused. Use weakmap or weakset.
- Use strict equal signs while comparing the values.=== instead of ==
- Always use Prettier or ESLint to format your code.

## Images
- Use SVG over png, jpeg etc
- If the image is the part of the content. Do not make it the part of the JS and CSS. Keep it on markup.
- Image should have the alt and title tags.
- Use a library like font-awesome for icons
- Use image sprite for the small images.
- Take advantage of lazy-loading while working on the site with heavy images.
- Use correct tags figure, img.
- Add captions , when required.

## Tools
- (Lighthouse)[https://developers.google.com/web/tools/lighthouse/]
- (caniuse.com)[https://caniuse.com/]
- (contrastratio)[https://webaim.org/resources/contrastchecker/]
- (Webpagetest)[https://www.webpagetest.org/]

## Reactsjs
Coming soon

## UX
Coming soon

## SEO
Coming soon

## Accessibility
Coming soon

## :heart: Contributions
Please raise the PR to contribute.

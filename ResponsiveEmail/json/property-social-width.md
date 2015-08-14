# Property `width`

Inside a social block, you can optionally specify the width of all of the social media image icons (general width)
or the width of each one separately (custom width). The general width is property in the social block 
and the custom width is subproperty of each platform.
If you change the general width, then the width of all social media icons will be set.
On the other hand, if you change the custom width of a selected platform,
then the width only of the parent platform will be set. 
Have in mind, that the custom width of each platform is with greater priority then the general width of all platforms, 
which means that if you change the general width and after that you change the custom width of a social platform, this
social platform will have the custom width value set, and not the general, but all other social platforms, which have no 
custom width, will have the general width value set.

The way Responsive library processes the width property and subproperty is the same as the [image width property](copernica-docs:ResponsiveEmail/json/property-image-width).

Note: For now a default image icon is used for each social media. That is why the default width, which is auto, is set to 32px
for every icon.

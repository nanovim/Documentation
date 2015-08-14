# Property `height`

Inside a social block, you can optionally specify the height of all of the social media image icons (general height)
or the height of each one separately (custom height). The general height is property in the social block 
and the custom height is subproperty of each platform.
If you change the general height, then the height of all social media icons will be set.
On the other hand, if you change the custom height of a selected platform,
then the height only of the parent platform will be set. 
Have in mind, that the custom height of each platform is height greater priority then the general height of all platforms, 
which means that if you change the general height and after that you change the custom height of a social platform, this
social platform will have the custom height value set, and not the general, but all other social platforms, which have no 
custom height, will have the general height value set.

The way Responsive library processes the height property and subproperty is the same as the [image height property](copernica-docs:ResponsiveEmail/json/property-image-height).

Note: For now a default image icon is used for each social media. That is why the default height, which is auto, is set to 32px
for every icon.

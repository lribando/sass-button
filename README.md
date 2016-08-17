# sass-button
This is a simple, reusable button template with states for active and disabled.

__Active State-__ a bright button with pointer to show it is clickable

**Disabled State-** the button fades in color when in the disabled state and will show an animated "stop sign" icon on hover

**Global Variables-** this template sets the font type and color assuming a consistent style guide. It can be modifed in the global variables, however it is recommended to keep the font color white if using a dark colored background for the button

**Enabled Animation-** the button will fade in to full brightness to show users it is clickable as opposed to faded out

**Disabled Animation-** the button is faded out when disabled and upon hover/interaction in disabled state, a user will see a red, "stop sign" icon

**Using the button theme mixin:**


1) Include btn-theme and specify the color of the button, font-size, width, and height. The color can take any value supported by CSS: string, hexvalue or RGB. As this is to mainly illustrate animation and DRY CSS, it is not responsive yet and it is recommended to use pixel dimensions for height and width:

```@include btn-theme (blue, 16px, 190px, 45px);```

2) Optionally, you can include a radius in your button class:

```@include radius(6px);```

3) Stop Sign Animation- A "stop sign" icon will appear on hover in the disabled state*

*Include the stop animation by adding an inline element to your page after the button tag and assigning it a class of "tip":

```<span class="tip"></span>```

Then call the mixin in your scss with a parameter for height set in pixels to match the height of your button:

```.tip {@include tip-generator(45px);}```


**Notes:**

1) This is a simple design to show Sass capabilities for DRY CSS

2) Animations are kept to basic transitions for full browser support and can be built upon if used in an actual project where CSS3 animations would be considered

3) As this is a practice example, proper Sass folder structure is not taken into consideration and recommended with use in a real project


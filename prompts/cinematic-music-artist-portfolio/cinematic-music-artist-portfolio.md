Create a cinematic portfolio website for a music artist inspired by atmospheric artist sites.

Important design direction:

The landing page must have a FULLSCREEN background image that covers the entire viewport.

The artist stands in the center of the frame and the UI elements float above the image.

The style should feel:

cinematic
moody
minimal
dark
nature inspired
slow and immersive

Do not create a bright modern UI. The design must feel calm and cinematic.

Tech stack:
HTML
CSS
Vanilla JavaScript

No frameworks.

Project files:
index.html
style.css
script.js

--------------------------------

HERO SECTION

The hero section must fill the entire screen.

height: 100vh

Background image:
A large cinematic portrait of the artist in nature.

The image should cover the screen using:

background-size: cover
background-position: center

Add a subtle dark gradient overlay to improve text readability.

--------------------------------

NAVIGATION

Top right navigation:

MUSIC
LIVE
VIDEO
ABOUT
FOLLOW
CONTACT

Navigation should be minimal with uppercase text.

--------------------------------

ARTIST NAME

Top left corner show the artist name in bold typography.

Example:

SIVERT
HØYEM

Large stacked typography.

--------------------------------

LEFT SIDE SOCIAL PANEL

Below the name add:

Listen:
Apple Music icon
Spotify icon

Follow:
Facebook
Instagram
Twitter

Icons should be simple white icons.

--------------------------------

HERO IMAGE TREATMENT

Add a cinematic dark overlay:

linear-gradient(
rgba(0,0,0,0.35),
rgba(0,0,0,0.6)
)

This helps the text stand out.

--------------------------------

SUBTLE ANIMATION

Add slow movement to the background image:

parallax effect on scroll.

When the user scrolls the background should slightly move.

--------------------------------

SECTION BELOW HERO

The next section must continue the same vibe.

Background color:

very dark green / black.

Example:
#0e1411

--------------------------------

LATEST MUSIC SECTION

Large album cover cards.

Each card shows:

album art
song title
play icon

Hover effect:

image slowly zooms
dark overlay fades

--------------------------------

LIVE TOUR SECTION

Minimal list of tour dates.

CITY
VENUE
DATE
TICKETS BUTTON

--------------------------------

VIDEO SECTION

Large cinematic music video embed.

--------------------------------

PHOTO GALLERY

Grid of large atmospheric photos.

Hover effect:

slow zoom
fade overlay

--------------------------------

FOOTER

Dark minimal footer with:

Spotify
YouTube
Instagram

--------------------------------

ANIMATION STYLE

Animations must be slow and smooth.

Use:

fade in
slow zoom
parallax scroll

Avoid flashy effects.

--------------------------------

FINAL RESULT

The site should feel like a cinematic artist landing page where the image dominates the design and the UI is minimal.






Splash Effect:
Fix the splash reveal position and size.

The splash must originate from the CENTER of the hero section and expand larger.

1. CENTER THE MASK

Update the splash SVG circles so their origin is centered.

Change the mask coordinates to:

cx="50%"
cy="50%"

Example:

<circle class="splash s1" cx="50%" cy="50%" r="40" fill="white"/>
<circle class="splash s2" cx="55%" cy="48%" r="25" fill="white"/>
<circle class="splash s3" cx="45%" cy="55%" r="30" fill="white"/>
<circle class="splash s4" cx="60%" cy="52%" r="20" fill="white"/>


2. INCREASE SPLASH SIZE

Increase the animation scale so the splash expands more.

.splash{
  transform-origin:center;
  transform:scale(0);
  transition:transform 0.8s cubic-bezier(.2,.8,.2,1);
}

.artist-container:hover .s1{
  transform:scale(18);
}

.artist-container:hover .s2{
  transform:scale(14);
  transition-delay:0.05s;
}

.artist-container:hover .s3{
  transform:scale(16);
  transition-delay:0.1s;
}

.artist-container:hover .s4{
  transform:scale(13);
  transition-delay:0.15s;
}


3. CENTER THE HERO CONTAINER

Make sure the mask aligns with the hero container:

.artist-container{
  position:relative;
  width:100%;
  height:100vh;
  display:flex;
  justify-content:center;
  align-items:center;
  overflow:hidden;
}
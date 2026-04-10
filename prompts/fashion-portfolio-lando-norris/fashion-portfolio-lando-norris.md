Build a fully responsive fashion portfolio landing page inspired by the attached reference design.

Important:
- Keep the overall layout structure, section order, spacing rhythm, and editorial fashion feel very close to the reference image.
- Do NOT copy Landonorris.com exactly.
- Create a similar premium interactive reveal effect, but instead of a helmet appearing, the main hero portrait should transition from black-and-white to full color on hover.
- The hover interaction must affect the entire hero subject only:
  - her face
  - hair
  - clothing/head wrap/bow
- Before hover, the whole landing page should feel mostly black and white / monochrome.
- On hover over the main girl in the hero section, she becomes fully colorful, including the bow on her head.
- The rest of the layout should stay mostly monochrome so the hover reveal feels dramatic.

Tech requirements:
- Use HTML, CSS, and JavaScript only.
- No frameworks.
- Make it smooth, premium, modern, and lightweight.
- Code should be organized into:
  - index.html
  - style.css
  - script.js
- Use semantic HTML.
- Make it easy to replace images later.
- Add comments in the code for important sections.

Overall visual direction:
- High-end fashion portfolio
- Editorial, premium, minimal, artistic
- Strong black / white contrast
- Soft beige / muted warm accent colors can appear only inside the revealed images and small UI details
- Large bold typography
- Rounded corners on image cards
- Spacious composition
- Slight luxury-magazine vibe

Page structure:
1. Full hero section
2. About me section
3. Fashion skills & expertise section
4. Creations/gallery slider section
5. Circular text statement section
6. Testimonials section
7. Footer / thank you section

Detailed layout instructions:

1. HERO SECTION
- Full-width dark hero section with rounded outer container corners.
- Top navigation inside the hero:
  - small logo/name on left
  - nav links centered or slightly right: HOME, WHO DIS?, MY VIBES, HIT ME UP
  - small rounded button on right
- Large oversized word behind the portrait, something like “DESIGNER”, in bold distressed or textured style.
- Main girl portrait centered and overlapping the large text.
- The portrait should initially appear entirely grayscale.
- Build the hover effect like this:
  - when cursor moves over the hero portrait area, reveal the full-color version of the same image
  - reveal should feel interactive and premium, not a simple instant swap
  - use a masked radial reveal or soft brush-like reveal tied to cursor position
  - keep it smooth with easing
  - the effect should only apply to the subject image, not the whole section
- The bow/head wrap must also change from grayscale to color during hover.
- Add subtle supporting hero text on left and a small circular badge/stamp on right.
- Include a small subtitle like “Styled to perfection”.

Implementation idea for hero image effect:
- Stack two versions of the same portrait:
  - bottom layer = grayscale image
  - top layer = full-color image
- Reveal the top layer using a circular or soft blob mask that follows cursor position
- On mouse leave, the color layer fades back out smoothly
- The reveal should feel elegant, soft, and artistic, not playful or gimmicky

2. ABOUT ME SECTION
- Bright/light section background
- Small heading on left: ABOUT ME
- Small editorial paragraph on right
- Huge bold centered heading:
  “THE GIFTED HANDS THAT SHAPE FASHION”
- Below it, staggered fashion image cards in different sizes
- Rounded corners
- Slight offset layout like the reference

3. FASHION SKILLS & EXPERTISE SECTION
- Dark background again
- Section heading at top left
- Decorative horizontal skill indicator made of flower-like shapes or abstract blobs connected by a line
- Large percentage text on left, e.g. “60%”
- Skill title on right:
  “STYLING & LOOKBUILDING”
- Small subtext underneath

4. CREATIONS / GALLERY SECTION
- Light background
- Small left-aligned intro text
- Large centered heading:
  “OUR CREATIONS”
- Horizontal gallery cards beneath
- Cards should look like a premium carousel
- Add two minimal arrow buttons below
- Use JavaScript to make the slider functional
- Smooth transitions
- Keep it touch-friendly on mobile

5. CIRCULAR TEXT STATEMENT SECTION
- Dark background
- Centered portrait/image
- Around the portrait, add circular curved text in uppercase, similar to editorial art direction
- Example phrase:
  “WHERE ELEGANCE AND FASHION BECOMES ART”
- The circular text should wrap around the portrait
- Keep the portrait mostly grayscale, but allow one strong accent color detail like a flower for visual drama

6. TESTIMONIALS SECTION
- Light background
- Giant bold heading:
  “TESTIMONIALS”
- Testimonial cards shaped like soft flowers/petals
- Mix white and pale blush pink cards
- Include small star ratings, short text, and names
- Place them asymmetrically like the reference

7. FOOTER SECTION
- Dark background
- Big “THANK YOU” on left and “FOR VIEWING” on right
- Center portrait/image near the bottom
- Oversized large word behind everything again, like “DESIGNER”
- Small nav links on right
- Social icons beneath
- Footer should feel like a strong closing fashion poster

Interaction and animation rules:
- Keep animations subtle and premium.
- Add smooth fade/slide reveal on scroll for sections.
- Use gentle parallax or micro-motion only where helpful.
- Do not over-animate.
- The hero image hover reveal is the main special effect and should be the focus.
- Add hover states for buttons, nav, and cards.
- Use CSS transitions and minimal JS.

Typography:
- Use a bold condensed sans-serif for big headings
- Use a clean sans-serif for body text
- Strong contrast in scale
- Large editorial headlines should dominate

Responsive behavior:
- Must work well on desktop, tablet, and mobile.
- Preserve the same visual hierarchy on mobile.
- Stack content cleanly.
- Hero portrait and large background typography should scale nicely.
- Gallery should become swipeable or scrollable on smaller screens.

Assets:
- Use placeholder image paths so I can replace them later:
  - images/hero-bw.jpg
  - images/hero-color.jpg
  - images/about-1.jpg
  - images/about-2.jpg
  - images/about-3.jpg
  - images/about-4.jpg
  - images/creation-1.jpg
  - images/creation-2.jpg
  - images/creation-3.jpg
  - images/creation-4.jpg
  - images/circle-portrait.jpg
  - images/footer-portrait.jpg

Color palette:
- Background dark: near-black
- Light sections: off-white
- Text dark: almost black
- Accent blush: soft dusty pink
- Accent warm beige only in photos or tiny UI elements
- Do not make the full page colorful — the color reveal must feel selective and intentional

Deliverables:
- Complete working code
- Clean folder structure
- All HTML/CSS/JS included
- Use placeholder content matching the fashion/editorial tone
- Make the page look polished even with placeholder images




Adding Image prompt:
Fix the hero image and interaction.

1. HERO IMAGE POSITION
- The main portrait must be perfectly centered like the reference.
- The head should overlap the large background text (DESIGNER).
- Anchor the portrait to the bottom center of the hero.
- The image should be large and dominant, not small.
- Use a container like:

.hero-image {
  position: absolute;
  bottom: 0;
  left: 50%;
  transform: translateX(-50%);
  height: 85%;
}

2. BLACK & WHITE → COLOR BRUSH REVEAL EFFECT

Use two identical images stacked:

- bottom layer → grayscale image
- top layer → full color image

Example structure:

<div class="hero-reveal">
   <img src="hero-bw.png" class="bw">
   <img src="hero-color.png" class="color">
   <canvas class="reveal-mask"></canvas>
</div>

3. IMAGE STYLING

.hero-reveal {
  position: relative;
  width: 520px;
  margin: 0 auto;
}

.hero-reveal img {
  width: 100%;
  display: block;
}

.bw {
  filter: grayscale(100%);
}

.color {
  position: absolute;
  top: 0;
  left: 0;
  clip-path: circle(0px at 50% 50%);
}

4. BRUSH REVEAL EFFECT (IMPORTANT)

When the mouse moves over the image:
- reveal the color image only where the cursor moves
- it should feel like a soft brush painting color
- use a circular mask that follows the cursor

Example JS logic:

const reveal = document.querySelector(".color");
const container = document.querySelector(".hero-reveal");

container.addEventListener("mousemove", (e) => {
  const rect = container.getBoundingClientRect();
  const x = e.clientX - rect.left;
  const y = e.clientY - rect.top;

  reveal.style.clipPath = `circle(120px at ${x}px ${y}px)`;
});

container.addEventListener("mouseleave", () => {
  reveal.style.clipPath = "circle(0px at 50% 50%)";
});

5. BRUSH STYLE

- brush radius ≈ 120px
- add smooth transition
- use a soft feathered look so it feels like paint

transition: clip-path 0.15s ease-out;

6. FINAL RESULT

When the page loads:
- portrait is completely black & white

When the user moves the cursor on the image:
- color appears only under the cursor
- it follows the mouse like a brush
- the bow/headwrap becomes colorful where revealed
- moving away returns to grayscale

Brush reveal hover effect:
Improve the hero hover reveal so it feels like a paint brush revealing the color image instead of a spotlight.

Problems to fix:
- The reveal circle is offset from the cursor
- The reveal looks like a hard spotlight
- It should feel like a soft brush stroke

1. HTML STRUCTURE

<div class="hero-image">
  <img src="images/hero-bw.png" class="hero-bw">
  <img src="images/hero-color.png" class="hero-color">
</div>


2. CSS

.hero-image{
  position:absolute;
  bottom:0;
  left:50%;
  transform:translateX(-50%);
  height:90vh;
  width:auto;
}

.hero-image img{
  position:absolute;
  bottom:0;
  left:50%;
  transform:translateX(-50%);
  height:100%;
  width:auto;
}

.hero-bw{
  filter:grayscale(100%);
}

.hero-color{
  pointer-events:none;
  mask-repeat:no-repeat;
  mask-size:100% 100%;
}


3. JAVASCRIPT BRUSH FOLLOW

const hero = document.querySelector(".hero-image");
const colorImg = document.querySelector(".hero-color");

hero.addEventListener("mousemove", (e)=>{

  const rect = hero.getBoundingClientRect();

  const x = e.clientX - rect.left;
  const y = e.clientY - rect.top;

  colorImg.style.maskImage = `
  radial-gradient(
    circle 160px at ${x}px ${y}px,
    rgba(255,255,255,1) 20%,
    rgba(255,255,255,0.8) 40%,
    rgba(255,255,255,0.4) 60%,
    rgba(255,255,255,0) 80%
  )`;

});


hero.addEventListener("mouseleave", ()=>{

  colorImg.style.maskImage =
  "radial-gradient(circle 0px at 50% 50%, white 0%, transparent 100%)";

});
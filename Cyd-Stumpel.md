# Who is Cyd Stumpel

Cyd is a creative developer. During her CMD study in 2014, she wasn't very good at Javascript, but she managed. In 2017 she did the minor for webdev. She said that during the minor you're basically learning "the basics". During her internship is where she learned the "real work"

At first she worked somewhere named something like "Matiz" but in 2020 they quit. Since then she's been a freelancer. She also works as an Awwwards jury. She even won an award herself for her portfolio. You can send in your own work to Awwwards and win awards with your own website.

She also works for FDND (Frontend Design & Development) for a day or 2 in the week.

She also worked for Talpa, made a website for Sallali.

For most of her work that she showed during the presentation, she used Flip and GSAP.

# Why are there so many websites, that win awards, inaccesible?

These are some reasons that she thinks why this is:

1. Alot of devs are "self-thaught" and they simply don't know of accesibility.
2. Does that mean that the jury sucks at grading them? The short answer is: yes, she long answer is: no.
   This is because accesibility is just 1/6 of the whole "grade", so accesibility isn't the biggest problem.

## What did she show us?

She showed us how the jury graded the websites. She also showed us websites she couldn't control with the keyboard and websites that were graded well on responsiveness, but weren't responsive at all.

## Common mistakes in creative websites

1. Removing ability to select text
2. Removing focus styles with no replacement
3. Removing native scrolling functionality
4. Omitting alternative text in buttons/images/etc.
5. Not adding a text alternative to letter animations
6. Not responding prefers-reduced-motion

# The curse of bad defaults

Bad defaults are referred to for example outlines or user-select: none, these are bad, because you remove the accesibility for a user by doing this.

Lenis works good for smooth scroll, because it will go to the right position. They're working with position sticky and to make scroll snap working in it.

# Tips

There are a few tips that Cyd Stumpel has given us when making your website:

1. Rethink your defaults, your resets, your go-to code snippets
2. Add text alternatives to letter/word/line animations
3. Consider native functionality in virtual scrolling libraries
4. Respect user settings with animations

- She follows greensock on twitter to keep updated (GSAP)
- She also recommends to look at awwwards, for inspiration and maybe also what not to do

# Live Coding

Ze gebruikte GSAP en SplitText om de text te splitten. Verde

aria-hidden="true" - text wordt niet voorgelezen voor screenreaders

`add.()"prefers-reduce-motion`

`stagger`: amount = hoelang een animatie duurt

alle letters astaan in losse spannetjes: command find gebruiken: split.revert na de hele animatie

# hoe zet je dan wel text alternative to letter animations?

# Live Coding notes

She basically showed us a bit of her work and how she made the presentation. She told us that she used GSAP and SplitText (to split the text). She also used `aria-hidden="true"`, so that the split up text wouldn't be read to screenreaders, otherwise they will read the text split up (which makes sense when using SplitText). She also used `add.()"prefers-reduce-motion"` so that people who have reduce motion enabled, it gets applied to the website too. This makes your website just more accesible. She also used `stagger`. She took a long time finding out about this, but you can basically decide on how long your animation is playing witht his. Other than that she also told us that every character is put into separate `span` elements. To make sure that you can use the `find` command in the browser, you need to make sure to apply `split.revert` afterwards, otherwise it won't recognize that the text is one whole thing, but rather separate characters, so it would be unable to find any word for you.

# Reflection

I thought this presentation was quite interesting but also shocking, as I wasn't aware of the fact that accesiblity seems to be QUITE the issue with certain websites. I was also shocked that the best websites (awarded with Awwwards) are mostly not accesible, then again, it makes sense because it's not a big part of the grading. This was shocking to me, because I do think it's quite important, than it gets graded.

> > > > > > > 5c26ede228daf45d66f8d43f1f2f98ecb1ed74d5

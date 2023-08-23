---
title: "Making a million $ saas from scratch - (1/n)"
datePublished: Wed Aug 23 2023 03:12:12 GMT+0000 (Coordinated Universal Time)
cuid: clln5sns3000a09m8gtuabdea
slug: making-a-million-saas-from-scratch-1n
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1692760307701/72c4d571-2c25-4064-b098-425bdc1b3f2f.png
tags: saas, svelte, prisma, tailwind-css

---

## The idea and the design ✨

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1692756534927/cef88686-a19f-450c-8702-22551364ecb5.png align="center")

About two weeks back I got into [Buildspace's](https://buildspace.so/) Nights and Weekends, which is a six-week-long program to work on any idea you are passionate about and turn it into a reality. The idea can be anything, art, music, robots, ai, youtube but it must be something you really wanna build.

My idea was pretty simple, a platform for developers to find side hustles, more specifically [moonlighting](https://dictionary.cambridge.org/dictionary/english/moonlighting) opportunities. Kind of like Upwork but for long-term, part-time, contract-based work with stable and consistent income. I named this platform moonlightdevs.

After buying a relevant domain, I decided to work on a landing page, which will have a waitlist for devs and orgs. I prefer minimalistic design so that's what I wanted for my page as well.

Here is what I came up with (initially),

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1692756354382/78d9a220-4819-4294-9300-6d523e1105bc.png align="center")

The idea was to make these planets revolve around the orbit, I was quite satisfied with the initial design so I decided to start developing it.

# The Stack for the Landing Page 👨‍💻

I wanted to try something I have never worked with to learn something new, so I decided to go with [SvelteKit](https://kit.svelte.dev/) as a meta framework to handle both my frontend and the backend. Coupled with Tailwind CSS it was a solid stack.

To save the waitlist emails, I decided to go with PlanetScale as my database platform and [Prisma](https://www.prisma.io/) as an ORM.

After binging some Svelte videos on YT, I was ready to build 🛠️

PS: A huge shoutout to [Huntabyte](https://www.youtube.com/@Huntabyte) and [Joy of Code](https://www.youtube.com/@JoyofCodeDev) for creating awesome content around Svelte on YouTube.

## Developing

Working with Svelte is awesome, it's fairly simple.

Look at this snippet below:

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1692757583440/f9d30d38-1e8d-4aa8-88c1-058c48256b5a.png align="center")

Looks like a vanilla HTML JavaScript code! You write your reactive logic in `<script>` tag, while styling goes in `<style>` rest is HTML.

Here is the initial website I developed:

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1692757973007/fe08e999-dcdd-4370-b701-827670e6024f.png align="center")

I know, the background was supposed to be a bit lighter, but I liked the black-and-white look and decided to make the entire website using these two as my primary colours.

The revolving planets didn't look good on the website so I decided to add a huge moon at the bottom-centre of the website. Here are the results:

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1692758311426/ca54bed6-8e4a-475e-916e-028f65268566.png align="center")

If the texture of the moon looks familiar to you, then you are the best. It's from [PopOs's](https://pop.system76.com/) open-sourced landing page.

After adding a Features and Waitlist form, it was time to connect to the database with Prisma. Again, Prisma is something I used for the first time and it made my life so much easier!

This small snippet was everything that was needed to connect to the database!

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1692758617426/11ca1703-d981-412f-be22-285b20e22864.png align="center")

And to write to the database:

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1692758899998/fc7917b1-2d87-4b5a-91a1-476782866a16.png align="center")

MIND BLOWN!!

After working on the functionality of the waitlist, I wanted to make this landing page appealing to clients or organizations that want to hire as well.

You may have already noticed the swap icon on the top right corner of the navbar, that button was made so that users can switch modes between "developer" and "organisation". I also wanted a cool animation to play when the user clicks the button.

To handle this I coded a global store to track the mode of the website, and making these global stores is so much easier in Svelte. Look at this:

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1692759361268/e238a4a7-7d91-4bbd-8a13-bd4fb526217e.png align="center")

Now, you can import these stores anywhere in your components and modify them as per your requirements.

Finally, for the animation, I used Svelte-Typewriter package.

Here are the results:

%[https://youtu.be/TknS6pL4Yqk] 

Thank you so much for reading till now, if you are interested, you can join the waitlist here: [moonlightdevs.xyz](https://moonlightdevs.xyz)

I have also kept the code open source, so if you want to take a look, you can check it out here: [https://github.com/rakshit087/moonlightdev](https://github.com/rakshit087/moonlightdev)

Million $ or not, I am thoroughly enjoying building it and sharing my progress in public. See you in the next update :))

PS: I usually don't write blogs so any kind of feedback is appreciated.
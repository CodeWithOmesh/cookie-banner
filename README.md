# 🍪 Cookie Banner You Have to Eat

Cookie banner, but you have to eat it. Every tap takes a crunchy bite out of the cookie. Finish it and the cookies are accepted. "Reject all"? Nice try.

**Live demo:** https://codewithomesh.github.io/cookie-banner/

**Watch the video:** https://www.youtube.com/@CodeWithOmesh

## Features

- Bites appear exactly where you tap, with tooth-mark edges (an SVG mask)
- Crunch, buzz and "yum" sounds made with the Web Audio API, no audio files
- Falling crumbs on every bite
- Measures how much is eaten and accepts at 80%
- "Reject all" button that refuses to cooperate
- "Take a bite" button for keyboard users
- One file, no libraries, no build step

## Run it

Download `index.html` and open it in any browser.

## How the bites work

```js
function bite(x, y) {
  bites.push([x, y]);
  crunch();
  crumbs(x, y, 10);
  if (eatenAmount() > 0.8) finish();
}
```

Each bite adds black circles to an SVG `<mask>`, which cuts that shape out of the cookie.

## Note

This is a joke. Real cookie banners must let people reject cookies as easily as they accept them. Please don't ship this one.

---

Made by **Code with Omesh** · Follow for more satisfying things built with code.

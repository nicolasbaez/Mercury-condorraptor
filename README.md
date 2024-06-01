# Mercury-condorraptor
Shup up and dance

![buh](https://github.com/nicolasbaez/Mercury-condorraptor/blob/main/xp036.gif)
```javascript
// noprotect
setup = (_) => createCanvas((w = 500), w, WEBGL);
draw = (_) => {
  clear();
  rotateX(sin(w));
  rotateY(tan(w / 8));
  stroke(w / 2);
  for (i = 0; i <= PI; i += 0.6 + sin(w / 2) * 0.3) {
    for (j = 0; j < 2 * PI; j += 0.9 + cos(w / 4) * 0.3) {
      r = w * 0.3;
      push();
      translate(r * sin(i) * cos(j), r * sin(i) * sin(j), r * cos(i));
      sphere(9, 3);
      pop();
    }
  }
  w -= 0.05;
};
keyPressed = (_) => {
  if (key === "s") {
    saveGif("xp036.gif", 502, { delay: 0, units: "frames" });
  }
};

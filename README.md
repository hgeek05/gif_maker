# gif_maker
 
🖼️ Create a GIF from Images using Python
In this project tutorial, I’ll show you how to turn multiple images into an animated GIF using only a few lines of Python! We’ll use a simple for loop, a list to store our images, and a powerful library called imageio. This is a beginner-friendly way to explore basic image processing in Python fun and practical!
Absolutely! Here’s your updated and cleaner version of the **README.md**, using **your actual code** and with clear, beginner-friendly explanations. I've also simplified the language and removed most emojis to keep it professional and readable.

### What You'll Learn

* How to read images using Python
* How to store image data in a list
* How to create an animated GIF using the `imageio` library

### Tools Used

* Python 3
* [`imageio`](https://imageio.readthedocs.io/en/stable/) library
* PNG images (example: `pic1.png`, `pic2.png`)

### How It Works

```python
import imageio.v3 as iio

filenames = ['pic1.png', 'pic2.png']
images = []

for filename in filenames:
    images.append(iio.imread(filename))

iio.imwrite('team.gif', images, duration=500, loop=0)
```

---

### Code Explanation

* `import imageio.v3 as iio`
  Loads the imageio version 3 module and gives it the name `iio` for short. This module handles reading and writing images and GIFs.

* `filenames = ['pic1.png', 'pic2.png']`
  A list containing the names of the image files you want to include in the GIF.

* `images = []`
  An empty list that will be used to store the image data.

* `for filename in filenames:`
  Loops through each image name in the list.

* `images.append(iio.imread(filename))`
  Reads the image file and appends the image data to the list.

* `iio.imwrite('team.gif', images, duration=500, loop=0)`
  Creates and saves a GIF file named `team.gif`.

  * `duration=500` sets each frame to last 500 milliseconds.
  * `loop=0` means the GIF will loop forever.

---

### Requirements

You need to have the `imageio` library installed. You can install it using:

```bash
pip install imageio
```

---

### Output

After running the script, you’ll get a new file named `team.gif` in your project folder. It contains an animated version of your input images.

---

### Tips

* Add as many images as you want to the `filenames` list
* You can change the frame duration by adjusting the `duration` value
* This kind of GIF is useful for team introductions, before/after comparisons, or visual summaries

---

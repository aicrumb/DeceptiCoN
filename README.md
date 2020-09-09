# DeceptiCoN

#### Anti-GAN Architecture

by Spruce Reams

---

A Discriminatory Collaborative Network (DeceptiCoN, yes I know it's a stretch I just wanted it to sound cool, like every other idiot here) is a discriminatory network comprised of two smaller networks collaborating to find an answer.

![](/content/imgs/explaination.png)

They both work take a picture, and a weight of 0.5 (uncertain) to begin with. They then take the same picture, and the weight of the respected partner's output. Repeat that step, take the average of the new outputs (blend* them), and you get the result.

 In this case, the networks take a 1-Dimensional array containing every row of the picture, and a row filled with the previous weight stacked, as an input. After going through three 1D-Convolutional layers, they output one value (which will then go on to be what the collaborator's bottom row will be filled with).

I like to call this an Anti-GAN because instead of having an adversary to try and trick, these do the opposite and collaborate.

The inspiration for this project came when I was just about to go to sleep and had too much caffeine, I was clearly **not** thinking straight.

All the code should be in the IPYNB notebook, a suggestion would be to open it in Google Colab.

(add [this file](https://drive.google.com/file/d/1Z7StVmvW8Y65_DOafnTQY2LE_crk_40Z/view?usp=sharing) to your drive, and create a new folder called `test` to put images in to, well, test in the end)

### Results:

![](/content/imgs/cat_right.png)

![](/content/imgs/dog_right.png)

As you can see it works fine, generally, though with further testing I've noticed that it's not the best, but still can get higher accuracy than just a vanilla network with the same parameters. Do I have the numbers to back that up? No because I was too stupid to add `wandb` to my project and I'm too lazy to do it now. Yes this is "bad science" and no I don't care. I made it within six hours or so, most of which was spent sleeping.

-side note

You may have to change file locations depending on how you set up the notebook, but it should be intuitive enough. I'm not *t h a t* bad at programming.



-side note part 2

This could probably give better results if you actually had clean data but I just scraped the first 400(?) pictures for `cat` and `dog` on [flickr](https://flickr.com) and used a custom script to augment them.

---

[@Spronkoid](https://twitter.com/spronkoid)

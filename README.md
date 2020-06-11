# Project Title

DSC160 Data Science and the Arts - Final Project - Generative Arts - Spring 2020

Project Team Members: 
- Cameron Brody, crbrody@ucsd.edu
- Brian Cheng, brc042@ucsd.edu
- Richard Duong, r3duong@ucsd.edu
- Thomas Evans-Barton, tevansba@ucsd.edu

## Abstract

(10 points) 

The first part of our generative art project is a computationally-generated inspired work of Andy Warhol's Shot Marilyns (1964). Andy Warhol's Shot Marilyns is a collection of multiple Marilyn Monroes. They are all the exact same images of Marilyn Monroe except that each one has a different color filter. Instead of creating each of the different color filters through hand, we will be using the algorithm of style transfer. Style transfer is a concept introduced in 2015. The data we will need will be the subject we will eventually choose and other artworks with the styles we want to base the subject off. After running the algorithm multiple times with different style sources, we should be able to replicate something similar to Shot Marilyns. Since it's a digital generated work, we are fine with it just being presentable through digital means. There is the fear that this algorithm will be very difficult to understand, but there are many resources online so we hope we will be able to manage it.

The second part of our project is to use style transfer in a different way, namely to take the style of a painting, and transfer it on to a real world recreation of that painting. Recently, there has been a very popular challenge going around known as the 'Getty Image Challenge', in which people attempt to recreate famous works of art using whatever household items are available to them. What we wanted to do was take each of those recreations, and make them look even more like their historical counterparts, and in doing so see what types of paintings/recreations tended to style transfer over well, and which did not.

Style transfer is a concept introduced in class. We are expanding it by using it to replicate a popular pop art. We want to do this because we want to see if we can recreate modern art with modern technology.


## Data and Model

(10 points) 

What style transfer is is that it uses a GAN to make a subject image in the style of a styled image.

https://www.tensorflow.org/tutorials/generative/style_transfer#build_the_model

Marilyn image sources:

Original Marilyn: https://www.moma.org/learn/moma_learning/_assets/www.moma.org/wp/moma_learning/wp-content/uploads/2012/07/Marilyn-PhotoPortrait-332x395.jpg

Spiderverse reference: https://m.media-amazon.com/images/M/MV5BMTU4NjYwNzAxN15BMl5BanBnXkFtZTgwMDkyODI4NjM@._V1_SX1777_CR0,0,1777,744_AL_.jpg

Matrix reference: https://m.media-amazon.com/images/M/MV5BMGM1NTk4YjMtNWNkNi00MzY3LWI3OTUtNTdmZGI3NmU2MGI0XkEyXkFqcGdeQXVyOTY2MDM3MjM@._V1_SX1777_CR0,0,1777,728_AL_.jpg

Frozen reference: https://m.media-amazon.com/images/M/MV5BYTk2MzNmZDAtODg5NC00OGYwLWE5MGMtNzc2NTM4ODQzYWZiXkEyXkFqcGdeQXVyNjQ4ODE4MzQ@._V1_SX1777_CR0,0,1777,740_AL_.jpg

Grand Budapest Hotel reference: https://m.media-amazon.com/images/M/MV5BN2M0ODJjZTgtYWNhYi00OTc3LWJiZWQtOWRjMWQyMzk3MDRkXkEyXkFqcGdeQXVyMjMzMDI4MjQ@._V1_SY1000_CR0,0,1330,1000_AL_.jpg

The referenced styles are screenshots of the respected movies from IMDb.com.

For the Marilyn part, we did both Tensorflow Hub's fast style transfer and also building a VGG19 from scratch. Our sequence of training epochs 1-10 was from the VGG19 model while the final output is from Tensorflow's fast style transfer.

Getty image sources:

All images:
https://blogs.getty.edu/iris/getty-artworks-recreated-with-household-items-by-creative-geniuses-the-world-over/

For the Getty Images Challenge, we used the same methodology as above.

## Code

(20 points)

Code: https://github.com/ucsd-dsc-arts/dsc160-final-group17_final/blob/master/code/4%20Marilyns.ipynb

Will need tensorflow installed.

For the Marilyn section, we load the subject and styled images then input them into Tensorflow's fast style transfer to receive our transferred results. We also built a VGG19 model from scratch, and trained on the Spiderverse style. We also print out the output for every training epoch.


## Results

(30 points) 

### Marilyn

Marilyn original

![alt text](https://www.moma.org/learn/moma_learning/_assets/www.moma.org/wp/moma_learning/wp-content/uploads/2012/07/Marilyn-PhotoPortrait-332x395.jpg)

The referenced styles (Spiderverse, Matrix, Frozen, Grand Budapest Hotel)

![alt text](https://github.com/ucsd-dsc-arts/dsc160-final-group17_final/blob/master/images/Marilyn%20Referenced%20Styles.png?raw=true)

Final transferred result

![alt text](https://github.com/ucsd-dsc-arts/dsc160-final-group17_final/blob/master/images/Marilyn%20Final.png?raw=true)

Training epoch steps 1-10 for our custom model

![alt text](https://github.com/ucsd-dsc-arts/dsc160-final-group17_final/blob/master/images/Marilyn%20Training%20Epochs.png?raw=true)

Using the referenced styles of various movies, we transferred the styles of them to the original image of Marilyn using Tensorflow's fast style transfer. The 10-step training sequence is using the VGG19 model on the style of Spiderverse.

### Getty Image Challenge

The Laughing Fool original:

![alt text](https://github.com/ucsd-dsc-arts/dsc160-final-group17_final/blob/master/images/image1_a.png)

The Laughing Fool recreation:

![alt text](https://github.com/ucsd-dsc-arts/dsc160-final-group17_final/blob/master/images/image1_b.png)

The Laughing Fool combination:

![alt text](https://github.com/ucsd-dsc-arts/dsc160-final-group17_final/blob/master/images/combined_1.png)

The Astronomer original:

![alt text](https://github.com/ucsd-dsc-arts/dsc160-final-group17_final/blob/master/images/image2_a.png)

The Astronomer recreation:

![alt text](https://github.com/ucsd-dsc-arts/dsc160-final-group17_final/blob/master/images/image2_b.png)

The Astronomer combination:

![alt text](https://github.com/ucsd-dsc-arts/dsc160-final-group17_final/blob/master/images/combined_2.png)

Self-Portrait, Yawning original:

![alt text](https://github.com/ucsd-dsc-arts/dsc160-final-group17_final/blob/master/images/image3_a.png)

Self-Portrait, Yawning recreation:

![alt text](https://github.com/ucsd-dsc-arts/dsc160-final-group17_final/blob/master/images/image3_b.png)

Self-Portrait, Yawning combination:

![alt text](https://github.com/ucsd-dsc-arts/dsc160-final-group17_final/blob/master/images/combined_3.png)

Male Harp Player of the Early Spedos Type original:

![alt text](https://github.com/ucsd-dsc-arts/dsc160-final-group17_final/blob/master/images/image4_a.png)

Male Harp Player of the Early Spedos Type recreation:

![alt text](https://github.com/ucsd-dsc-arts/dsc160-final-group17_final/blob/master/images/image4_b.png)

Male Harp Player of the Early Spedos Type combination:

![alt text](https://github.com/ucsd-dsc-arts/dsc160-final-group17_final/blob/master/images/combined_4.png)


## Discussion

(30 points, three to five paragraphs)

Since we had two semi-independent projects under the same general idea of style transfer, we have two sets of results. The first set is the results of applying various styles to the image of Marilyn Monroe, similar to Andy Warhol's Pop Art. We were able to find four stylistically different films and successfully apply their style to our image of Marilyn, resulting in a new version of Andy Warhol's Shot Marilyns. Our second set of results is from the Getty Images Challenge, where we applied the style of a painting to a real-life recreation of the painting. We found much success with certain items, but some had troubling results due to a few factors. Overall, we were very happy with both results, as we were able to replicate both of our inspirations and push them further than their original interpretation.

For the Marilyn part, the Tensorflow Hub fast style transfer produced more aesthetically pleasing images and they were done within a second. The VGG19 model requires a lot more time to train. Our sequence of training epochs 1-10 was from the VGG19 model. The Spiderverse-styled Marilyn took 44 minutes to train from the VGG19 model. Due to the training time, we only did it on the Spiderverse style and the final Marilyn products were compiled with fast style transfer products. According the Tensorflow's article, the VGG19 model is the very original style transfer model. There are lots of artifacts produced from it even from the long transfer time.

The Marilyn part is culturally innovative because we are re-creating modern art with modern technology. Instead of spending days creating artworks of different styles, we can create such in a matter of minutes. One far-off possibility of expansion for this project is we can print out our output in physical form. A new model can then be trained to create the physical textures of the different styled artworks.

For the Getty Image Challenge, for the most part, the combinations of the recreations and their original paintings turned out quite well! We had exceptional success in recreations for both The Laughing Fool by Jacob Cornelisz van Oostsanen, as well as The Astronomer by Johannes Vermeer. Self-Portrait, Yawning by Joseph Ducreux was not as good of a combination, possibly due to the shadows in the background of the recreation; it seems that the style transfer was slightly unsure of what to do with these patches, and made them very light in comparison to their original shade. Additionally, on the final instance, we attempted to style transfer a picture of the statue that the individual was trying to recreate, to see how a more physical medium might be style transferred over. This was very experimental, and unfortunately did not quite work, but it was still an interesting thing to try.

Ultimately, generative art in these two manners were both very successful in their own ways, and show the incredible potential that style transfer has to create great and hitherto unimagined art in the future.


## Team Roles

Cameron Brody: Project idea creation, writing

Brian Cheng: Project idea creation, creation of Marilyn modeling network, writing

Richard Duong: Project idea creation, writing

Thomas Evans-Barton: Project idea creation, creation of Getty modeling network, writing

## Technical Notes and Dependencies

The code will require Tensorflow to be installed.

## Reference

Shot Marilyns (1964) https://en.wikipedia.org/wiki/Shot_Marilyns

Original style transfer paper (2015) https://arxiv.org/abs/1508.06576

A tutorial on how to style transfer https://www.pyimagesearch.com/2018/08/27/neural-style-transfer-with-opencv/

Source for Getty Images https://blogs.getty.edu/iris/getty-artworks-recreated-with-household-items-by-creative-geniuses-the-world-over/

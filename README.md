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

The second part of our project is

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

For the Marilyn part, we did both Tensorflow Hub's fast style transfer and also building a VGG19 from scratch. The Tensorflow Hub fast style transfer produced more aesthetically pleasing images and they were done within a second. The VGG19 model requires a lot of time to train. Our sequence of training epochs 1-10 was from the VGG19 model. The Spiderverse-styled Marilyn took 44 minutes to train from the VGG19 model. Due to the training time, we only did it on the Spiderverse style and the final Marilyn products were compiled with fast style transfer products.

Getty image sources

In the final submission, this section will describe both the data you use for this project and any pre-existing models/neural nets. For each you should provide the name, a textual description, and a link. If there is a paper (for neural net) link that as well.
- Such and such Neural Net. The short description of this neural net. 
  - [link to code]().
  - [Title of Paper with Link](). 
- Training data. Short description of training data including bibliographic info. [link to data]().

## Code

(20 points)

Code: https://github.com/ucsd-dsc-arts/dsc160-final-group17_final/blob/master/code/4%20Marilyns.ipynb

Will need tensorflow installed.

This section will link to the various code for your project (stored within this repository). Your code should be executable on datahub, should we choose to replicate your result. This includes code for: 

- code for data acquisition/scraping
- code for preprocessing
- training code (if appropriate)
- generative methods

Link each of these items to your .ipynb or .py files within this seection, and provide a brief explanation of what the code does. Reading this section we should have a sense of how to run your code.

## Results

(30 points) 

This section should summarize your results and will embed links to documentation to significant outputs. This should document both process and show artistic results. This can include figures, sound files, videos, bitmaps, as appropriate to your generative art idea. Each result should include a brief textual description, and all should be listed below: 

- image files (`.jpg`, `.png` or whatever else is appropriate)
- audio files (`.wav`, `.mp3`)
- written text as `.pdf`

## Discussion

(30 points, three to five paragraphs)

The first paragraph should be a short summary describing your results.

The subsequent paragraphs could address questions including:
- Why is this culturally innovative?
- How does your generative computational approach differ from traditional art/music/cultural production? 
- How do your results relate to broader social, cultural, economic political, etc., issues? 
- What are the ethical concerns for this form of generative art? 
- In what future directions could you expand this work?

Since we had two semi-independent projects under the same general idea of style transfer, we have two sets of results. The first set is the results of applying various styles to the image of Marilyn Monroe, similar to Andy Warhol's Pop Art. We were able to find four stylistically different films and successfully apply their style to our image of Marilyn, resulting in a new version of Andy Warhol's Shot Marilyns. Our second set of results is from the Getty Images Challenge, where we applied the style of a painting to a real-life recreation of the painting. We found much success with certain items, but some had troubling results due to a few factors. Overall, we were very happy with both results, as we were able to replicate both of our inspirations and push them further than their original interpretation.


## Team Roles

Cameron Brody: Project idea creation, writing
Brian Cheng: Project idea creation, creation of Marilyn modeling network, writing
Richard Duong: Project idea creation, writing
Thomas Evans-Barton: Project idea creation, creation of Getty modeling network, writing

## Technical Notes and Dependencies

Any implementation details or notes we need to repeat your work. 
- Additional libraries you are using for this project
- Does this code require other pip packages, software, etc?
- Does this code need to run on some other (non-datahub) platform? (CoLab, etc.)

## Reference

Shot Marilyns (1964) https://en.wikipedia.org/wiki/Shot_Marilyns
Original style transfer paper (2015) https://arxiv.org/abs/1508.06576
A tutorial on how to style transfer https://www.pyimagesearch.com/2018/08/27/neural-style-transfer-with-opencv/

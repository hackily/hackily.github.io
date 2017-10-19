---
title: "Rashional"
excerpt: "Gain insight on your rash with the help of a neural network!."
header:
  image: /assets/images/rashional/banner.jpg
  teaser: /assets/images/rashional/logo.png
sidebar:
  - title: ""
    image: /assets/images/rashional/logo.png
    image_alt: "Rashional"
    text: "Take control of your skin health"
gallery:
  - url: /assets/images/rashional/chart.png
    image_path: assets/images/rashional/chart.png
    alt: "Results after uploading picture of rash"
  - url: /assets/images/rashional/clinics.png
    image_path: assets/images/rashional/clinics.png
    alt: "Locations of nearby clinics"
---

Rashional is a website client to a convolutional neural network hosted in AWS. I use the clarifai AI as a service platform, feeding it hundreds of pictures of various skin conditions, and their respective classifications.

Rashional is not meant to be used as a diagnostic tool, but as an aid to stress how important it is to go see a doctor. To that extent, we use the user's geolocation data to find clinics nearby, as well as their contact information, if applicable. We want to be the tipping point that sends a user to seek professional medical help.

{% include gallery caption="Images of the application in use" %}


## Inspiration

A friend of mine went hiking and was bitten by an insect. He thought nothing of it, nor the rash that appeared in a completely different location on his body from where he was bitten.

Later that week, he started complaining about headaches and muscle aches. He assumed he was tired. He was not. He had contracted Lyme disease.

The rash that appeared on his skin didn't have the characteristic bulls-eye shape that Lyme disease is known for. But what if we could identify different dangerous rashes, based of an image? Enter, machine learning.

## What it does

The app asks the user to take a photo or select a photo from the gallery on their smartphone, or somewhere on their computer. Rashional will then provide a confidence level for our four trained concepts. Regardless of outcome, we will strongly suggest that the user visit a real health practioner - and we provide the contact information and addresses of nearby free medical clinics.

## Brief Technical Overview

I used a chrome plugin to scrape the internet for hundreds of photos of various skin conditions, and focused on training our model for several dangerous skin conditions that are easily overlooked: Lyme Disease, Ringworm, Shingles, and Rocky Mountain Spotted Fever.

Not all photos are of equal quality. Photos that are clearly unsuitable and unrepresentative of the disease condition were removed.

I also found several hundred pictures of various other skin conditions, to use as negative reinforcement examples. These conditions included: Acne, warts, calluses, moles, mosquito bites, pimples, freckles, healthy skin, and more.

We used react.js to create a smooth and dynamic front end application that interfaces with our backend MongoDB Database and Machine Learning Software to provide the user with a seamless easy-to-use application.

User uploads are saved to MongoDb, and we take care to not save any information that would let us identify the user.
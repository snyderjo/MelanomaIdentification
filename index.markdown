---
layout: page
title: "Melanoma Identification"
background: "/img/lesions.png"
---


## The Issue

1. Utah has the highest rate of skin cancer in the country [citation needed].
2. If it's caugt early, melanoma, is no big deal; however, [if the disease progresses or spreads, the prognosis is notably worse](https://www.aad.org/media/stats-skin-cancer#:~:text=The%20five%2Dyear%20survival%20rate,the%20lymph%20nodes%20is%2099%25.&text=The%20five%2Dyear%20survival%20rate%20for%20melanoma%20that%20spreads%20to,and%20other%20organs%20is%2030%25.).  Consequently, prompt screenings are vital for the timely.
3.  Who is well positioned to identify melanoma?  Dermatologists.

The problem being, getting a derm appointment is an everloving pain.

#### Anecdote
Several years ago, I looked for a derm appointment at a nearby clinic, only to learn that none of the dermatologists were accepting new patients.  I inquired at the next closest clinic, and schduled an appointment for *two months later*.

***Dermatologists are in low supply and high demand.***

These circumstances do not lend themselves to prompt screening of potentially malignant lesions.

## Background

In the early 2020's, I worked with a surgeon at [Intermountain Healthcare](https://intermountainhealthcare.org/) to develop a curriculum for non-dermatologists to identify malignant melanoma lesions in collaboration with a professor from BYU.  My role in the project was origially limited to stripping metadata from images sourced by Intermountain Healthcare, and sharing them via SFTP.

This project was supplemental and complementarty to that project.

## Structural Issues
There are entirely too many barriers to increasing the supply of physicians, much less dermatologists.

Urban-rural distribution of specialists futher exacerbate the issue in a large western state such as Utah.

## Potential Solution
General practitioners or family physicians could use an appropriately trained convolutional neural network to refer patients to dermatologists expiditiously.  GP's and family doctors are unfortunately the target of most high-level initiatives--they are the doctors most likely to receive missives from... most everyone.

> "See more patients in the same number of hours!"

> "Encourage high-risk patients to get screenings."

> etc.

This is designed to provide a means of identifying patients with high-risk lesions and potentially referring them to dermatologists promptly.

### Data
This project is designed to accept an in image of a skin lesion, i.e. a mole, and return a probability of that lesion being malignant.
The data was sourced from [kaggle](https://www.kaggle.com/competitions/siim-isic-melanoma-classification/overview).
Computing resources were provided by [Google Colab](https://colab.research.google.com/).

### The Model

[link](https://snyderjo.github.io/documents/Kaggle_Melanoma_CNN.html)

I made use of EfficientNetB0 for the purposes of transfer learning, trained the model, and briefly explored fine-tuning.  There's some evidence of the model effectiveness, but the heavy imbalance creates issues in evaluation.


### Is this all?

That is to say, is the project complete?
No.

If you examine the images, you'll notice that:
* the images are remarkably well centered,
* most are well-lit, and
* most are on caucasian skin

If one wants to pass any random photo of a skin lesion, and have it evaluated accurately, a [YOLO algorithm](https://en.wikipedia.org/wiki/YOLO_(algorithm)) could help ameliorate the first issue.  Similarly, [anomaly detection](https://en.wikipedia.org/wiki/Anomaly_detection) might be able to help identify photos with poor lighting.  What about non-caucasian skin?--I don't have a good answer short of futher data collection.


## Tools I used

<table style="padding:30px;font-size:16px;">
<tr>
    <td align="center">
        <div>
            <img src="img/lesions.png" alt="1" height="120px" width="120px">
        </div>
    </td>
    <td  align="center">
        <div>
            <img src="img/lesions.png" alt="2" height="120px" width="120px">
        </div>
    </td>
    <td  align="center">
        <div>
            <img src="img/lesions.png" alt="3" height="120px" width="120px">
        </div>
    </td>
</tr>
<tr>
    <td>
        <div>
            <p style="text-align:center">tensorflow.</p>
        </div>
    </td>
    <td >
        <div>
            <p style="text-align:center">google colabs</p>
        </div>
    </td>
    <td >
        <div>
            <p style="text-align:center">kaggle? matplotlib?</a>.</p>
        </div>
    </td>
</tr>
</table>

<br>


## Conclusion
There is some promise to the approach, but I expect any further work will be dictated by the necessities of the work.
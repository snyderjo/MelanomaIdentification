
# Melanoma Identification
In the early 2020's, I worked with a surgeon at [Intermountain Healthcare](https://intermountainhealthcare.org/) to develop a curriculum for non-dermatologists to identify malignant melanoma lesions in collaboration with a professor from BYU.  My role in the project was origially limited to stripping metadata from images sourced by Intermountain Healthcare, and sharing them via SFTP.

This project was supplemental and complementarty to that project.

## The Issue
Utah has the highest rate of skin cancer in the country [citation needed].
Melanoma, when caught early, is no big deal; however, [if the disease progresses or spreads, the prognosis is notably worse](https://www.aad.org/media/stats-skin-cancer#:~:text=The%20five%2Dyear%20survival%20rate,the%20lymph%20nodes%20is%2099%25.&text=The%20five%2Dyear%20survival%20rate%20for%20melanoma%20that%20spreads%20to,and%20other%20organs%20is%2030%25.).
Consequently, prompt screenings are vital for the timely

## Motivation
Who is best prepared to diagnose whether a given skin lesion is malignant?
*Dermatologists*

#### Anecdote
Several years ago, I looked for a derm appointment at a nearby clinic, only to learn that all the dermatologists were not accepting new patients.  I inquired at the next closest clinic, and schduled an appointment two months later.

***Dermatologists are in low supply and high demand.***

These circumstances do not lend themselves to prompt screening of potentially malignant lesions.

## Structural Issues
There are entirely too many barriers to increasing the supply of physicians, much less dermatologists.

Urban-rural distribution of specialists futher exacerbate the issue in a large western state such as Utah.

## Potential Solution
General practitioners or family physicians could use an appropriately trained convolutional neural network to refer patients to dermatologists expiditiously.  GP's and family doctors are unfortunately the target of most high-level initiatives--they are the doctors most likely to receive missives from... most everyone.

> "See more patients in the same number of hours!"
> "Encourage high-risk patients to get screenings."
> etc.

This is designed to provide a means of identifying patients for referral to specialists, i.e. dermatologists.

### Data
This project is designed to accept an in image of a skin lesion, i.e. a mole, and return a probability of that lesion being malignant.
The data was sourced from [kaggle](https://www.kaggle.com/competitions/siim-isic-melanoma-classification/overview).
Computing resources were provided by [Google Colab](https://colab.research.google.com/).

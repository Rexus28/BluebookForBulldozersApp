[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/Rexus28/BluebookForBulldozersApp/HEAD?urlpath=%2Fvoila%2Frender%2Fbfb_app.ipynb)

## Bluebook for Bulldozers Notebook App
This Bluebook For Bulldozers app is based on the 
[Kaggle competition](https://www.kaggle.com/c/bluebook-for-bulldozers/overview)
of the same name. The goal was to predict auction price of heavy constructuion
equipment based on function, size, model, and configuration described in a
dataset of 53 fields.

However, the goal of this app is to create a simplified user interface with
only 8 inputs to predict an accurate price. Even with so few inputs, a random
forest model was trained and achieved a validation root mean squared log error
(RMSLE) of 0.240, which would place it just inside the top 20 of the competitions
[final results](https://www.kaggle.com/c/bluebook-for-bulldozers/leaderboard).
Not bad for a model using only about a seventh of the original dataset.

To use the app, make selections from the dropdowns below. Because the dataset
is from 2012, that is the latest year that can be selected for year made, and
all prices are predicted for a sale year of 2012 as well. That means it's
predicted 2012 prices of the equipment. This is important becaues random
forests are not good at extrapolating outside of the domain of the data.

Enter the general type the equipment in the class field, and a more specific
physical description in the descriptor field. The full model name is split
into three distinct parts: the base model, secondary description, and model
description. So a "D3G XL" would be entered as "D3" for the base model, "G"
for the secondary description, and "XL" for the model description. Secondary
and model description options are dependent on the base model selected.

When the price is predicted a waterfall chart is plotted below that describes
how each option contributes to the final prediction. The base price is the
average price of all pieces of equipment, and from this starting point the
plot shows how much each field adds or substracts to reach the final price. A
year field (not just the year made) is included in the price prediction
because this was a key feature in the model, but it is fixed at 2012 to
predict prices at a time relevant to the dataset.

#References
@book{howard2020deep,
title={Deep Learning for Coders with Fastai and Pytorch: AI Applications Without a PhD},
author={Howard, J. and Gugger, S.},
isbn={9781492045526},
url={https://books.google.no/books?id=xd6LxgEACAAJ},
year={2020},
publisher={O'Reilly Media, Incorporated}
}

Fast Iron. (2013, January). Blue Book for Bulldozers. Retrieved June 28, 2021
from https://www.kaggle.com/c/bluebook-for-bulldozers/data.

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/Rexus28/BluebookForBulldozersApp/HEAD?urlpath=%2Fvoila%2Frender%2Fbfb_app.ipynb)

# Hackathon-Code-Approch 
Hackathon from Analytics Vidhya Sept 2021

## Supplement Sales Prediction
Your Client WOMart is a leading nutrition and supplement retail chain that offers a comprehensive range of products for all your wellness and fitness needs.

WOMart follows a multi-channel distribution strategy with 350+ retail stores spread across 100+ cities.

Effective forecasting for store sales gives essential insight into upcoming cash flow, meaning WOMart can more accurately plan the cashflow at the store level.

Sales data for 18 months from 365 stores of WOMart is available along with information on Store Type, Location Type for each store, Region Code for every store, Discount provided by the store on every day, Number of Orders everyday etc.

Your task is to predict the store sales for each store in the test set for the next two months.

### Gotcha
* Noticed nearly the same ups and downs in all 365 store’s sales plot and all plot looks similar.
* Holidays are the same for all stores in train data and test data.
* Still, holiday configuration will require in the model.
* Facebook Prophet will do better in the configuration of special days as holidays, so here I am using Facebook
Prophet.
### Preprocessing
* No preprocessing at beginning
* For all 365 stores give store_id in each forecast data frame, so it can be merged in the test data frame.
* At the end collect all 365 data frames and concatenate them to a single data frame as the final forecast.
* Join two data frames Df_test and final forecast by merge method.
### Model
* Finally Forecast for each of 365 stores by Facebook Prophet Separately, with holidays configuration.

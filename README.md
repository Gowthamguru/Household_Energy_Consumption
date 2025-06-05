# Household Energy Consumption
## Dataset Information
<p><b>Additional Information</b><br/>
This archive contains 2075259 measurements gathered in a house located in Sceaux (7km of Paris, France) between December 2006 and November 2010 (47 months).</p>

## Variable Details

<table>
  <tr>
  <th>Variable Name</th>
    <th>Type</th>
  </tr>
  <tr>
        <td>Date</td>
    <td>Date</td>
  </tr>
   <tr>
        <td>Time</td>
    <td>Categorial</td>
  </tr>
     <tr>
        <td>Global_active_power</td>
    <td>Continuos</td>
  </tr>
     <tr>
        <td>Global_reactive_power</td>
    <td>Continuos</td>
  </tr>
     <tr>
        <td>Voltage</td>
    <td>Continuos</td>
  </tr>
     <tr>
        <td>Global_intensity</td>
    <td>Continuos</td>
  </tr>
     <tr>
        <td>Sub_metering_1</td>
    <td>Continuos</td>
  </tr>
     <tr>
        <td>Sub_metering_2</td>
    <td>Continuos</td>
  </tr>
     <tr>
        <td>Sub_metering_3</td>
    <td>Continuos</td>
  </tr>
</table>

## Data Approach
### Data Understanding and Exploration
<p>1. To perform the Application Development, import the important libraries and packages</p>
<p>2. The data provided in the text file with delimiter <b>;</b> and file in the CSV format</p>
<p>3. Read the data using pandas libraries and stored the data into dataframe</p>

## Data Processing 
<p>1. Validated the null values </p>
<p>2. In the provided data we are having the null characters in the column sub_metering_3</p>
<p>3. Verified the sub_metering_3 column data against null records with <b>?</b> mark</p>
<p>4. The data is not relavant and can't able to utilize to our ML optimization </p>
<p>5. The null data cleared from the dataframe</p>
<p>6. Verfied the duplicate records and there is no duplicate in the provided data</p>

## Feature Engineering
<p>1. We already have the date column with data type is date</p>
<p>2. For the validation purpose split the date field as Day,Month & Year</p>
<p>3. The Time field as object and convert the field as time and split the time as Hour and Minutes column</p>
<p>4. The data type of all the numerical column as object</p>
<p>5. Converted the object column to float for the feature engineering purpose</p>
<p>6. Based on the updated dataframe able to find the Day Aveage , Rolling Average and Peak hours</p>
<p><b>Day Aveage</b> </p>
<p>6.1 Resample the data Group by based on the Global Active Power </p>
<p>6.2 Calculate the mean value from the above series</p>
<p>6.3 We got the data as a series and converted the series to dataframe </p>
<p>6.4 Update the column details and plot the changes in the Line plot</p>
<p><b>Rolling Aveage - </b> A technique used to analyze time series data by calculating the average of a specific number of recent data points </p>
<p><b>Peak Hours - </b>We are consider From 6 PM to 10 PM as peak hours</p>
<p>6.5 Define the new field Rolling_avg_power and consider every 3 hours average and maintain in the field  </p>
<p>6.6 We consider from 6 PM to 10 PM as peak hours</p>
<p>6.7 Create the new column is_peak_hour and update the flag between 18 to 22 (6PM to 10PM) </p>
<p>6.8 Draw the Rolling average information in the line plot</p>
<p>6.9 Draw the Peak hours using boxplot and identifiy the outliers of the data</p>
<p>6.10 In the box plot we are consider both off-peak and peak hours</p>

## Model Selection and Training
<p>1. Split the dataset into a training and a testing set</p>
<p>2. Perform the Standard scaling </p>
<p>3. Perform the train and testing split using the sklearn train_test_split package</p>
<p>4. Initialize the <b>Linear Regression Model</b></p>
<p>5. Based on the data prediction from the model </p>
<p>6. Applied RSME,MAE and R2 Square Evaluation metrics</p>
<p>7. From the above evaluation metrics, we can see the difference is less than 1%, and we consider this as an optimal mode</p>
<p>8. Draw the scatter plot based on the output</p>
<p>9. The Same method applies for RandomForestRegressor and GradientBoostingRegressor</p>
<p>10. In the Randomforest Regressor applied the RandomizedSearchCV hyperparameter optimization</p>

## Neural Network
<p>1. Using Tensorflow and keras performed the operation </p>
<p>2. In the neural network the following steps were followed </p>
<p><b>Define the model</b></p>
<p><b>Compile the model</b></p>
<p><b>Train the model</b></p>
<p><b>Evaluate the model</b></p>
<p><b>Based on evaluation matrics additionally plot the charts</b></p>
<p>3. Additionally performed the dropout and Early stopping method</p>

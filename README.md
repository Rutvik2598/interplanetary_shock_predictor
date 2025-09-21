# CME–IPS Duration Prediction  

This project predicts the time difference (in hours) between **Coronal Mass Ejections (CMEs)** and their corresponding **Interplanetary Shocks (IPS)** using observed CME speeds.  

## Workflow  
1. **Data Linking**  
   - Build a lookup table of CMEs with their speeds and start times.  
   - Link each IPS event to its corresponding CME using `activityID`.  
   - Compute the IPS–CME time difference in hours.  

2. **Data Preparation**  
   - Save the linked CME–IPS dataset as a CSV.  
   - Load the dataset into a pandas DataFrame for analysis.  

3. **Modeling**  
   - Fit a **nonlinear power-law model** of the form:  
     \[
     y = a \cdot x^b
     \]  
   - Split the dataset into **train and test sets**.  
   - Train the model on training data and evaluate on test data.  

4. **Evaluation**  
   - Metrics: **MAE, RMSE, R²**.  
   - Compute and visualize **residuals** to check model performance.  
   - Generate predictions for new CME speeds.  

5. **Visualization**  
   - Scatter plots of CME speed vs IPS duration.  
   - Fitted nonlinear regression curve.  
   - Residual plots for error analysis.  

## Files  
- `cme_ips_data.csv` → Dataset.
- Notebook contains csv creation, preprocessing, modeling, evaluation, and plots.  

## Requirements  
- Python 3  
- pandas  
- numpy  
- matplotlib  
- seaborn  
- scipy  
- scikit-learn  

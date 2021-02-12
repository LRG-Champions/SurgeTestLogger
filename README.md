# SurgeTestLogger
Prerequisites:
- Microsoft 365 subscription including PowerApps e.g. E3 Licence.  
- Access to a SharePoint Online site where you can create a new List
- Access to your LLPG to export properties to be targeted for Surge Testing

Implementation:
1. Create a SharePoint Online List called “Surge Testing”
2. The list should have the below columns:

		COLUMN				DATA TYPE
		UPRN*				Single line of text	
		Recorded By			Single line of text	
		Activity			Single line of text	
		Resident Flag			Single line of text	
		Age Checked			Single line of text	
		Barcode				Single line of text	
		Test Kit Received Date		Single line of text	
		Test Kit Received		Single line of text

	*Note this column was the default ‘Title’ column which has been renamed to UPRN.

3. Create a excel file containing export a list of properties you want to target for your Surge Testing in an Excel file.
	   You can find a template for this \LLPG Extract\LLPGExtract_SampleFile.xlsx
	   You should note if you are importing more than 15,000 properties you will need to split the data into tables of 15,000,
	   the sample file has 3 preloaded tables. 
4. Import the PowerApp zip file into your Microsoft 365 PowerApps environment (\PowerApp\ SurgeTestLogger.zip)
5. Open the PowerApp in Edit Mode and open the _Admin screen. Follow instructions outlined on screen to import the Static 
	   dataset and connect to your SharePoint list you create in Step 1. 
6. Publish App and grant users access. 

Reporting:
	You should be able to use a BI tool such as QlikSense or Power BI to interrogate the data saved from the app to give 
	intelligence on properties which have not had their tests collected or volume of properties which have refused / accepted 
	tests etc. You will want to make use of the Created column which will be the created date time for each entry in the list. 
	If you do not have a BI tool, you could create Views on the SP List to displace counts and properties based on filters but 
	remember some of these features may not work when your list goes over 5000 rows of data so a BI Tool is recommended here. 

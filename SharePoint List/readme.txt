You must create a SharePoint Online List with the below column names and data types:

COLUMN				DATA TYPE
UPRN*				Single line of text	
Recorded By			Single line of text	
Activity			Single line of text	
Resident Flag			Single line of text	
Age Checked			Multiple lines of text	
Barcode				Single line of text	
Test Kit Received Date		Single line of text	
Test Kit Received		Single line of text

*Note this column was the default Title column which has been renamed to UPRN.


I also reccomended you create two indexes on the below columns:
- UPRN
- Barcode


All users of your PowerApp will need read/write access to this SharePoint list
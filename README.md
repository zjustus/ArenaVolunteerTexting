<h1>Arena Volutneer Texting</h1>
<p>These stored procedures allow Arena to send Confirmation text messages to schedjuled volunteers.
Due to the nature of the resources being used, this module must only exist through stored procedures making the setup more complicated than a normal module
</p>
<h2>Requirements</h2>
<p>These Stored procedures require the KFS twilio texting module to be installed.</p>
<h2>Instalation</h2>
<ol>
<li>Modify the VolunteerServiceView.ascx file to include the service ID <br> Add this code inside the script tag <br> <code>var serviceID = "<%= Session["_serviceID"] %>";</code></li>
<li>next run the installer script to add the required stored procedures to the database</li>
<li>make a new page in arena and add a "HTML from stored procedure" module to the page with the stored procedure "cust_luminte_HTML_sp_VolunteerSMSpage" and give it the paramaters @serviceID</li>
<li>Add another "HTML from stored" module to Volunteer Service Page with the stored procedure "cust_luminate_HTML_sp_VolunteerSMSbutton" and give the paramater @pageID of the page you created in the previous step</li>
</ol>
<h2>procedures List</h2>
<p>a list of the stored procedures this installs</p>
<ul>
<li>cust_luminate_HTML_sp_VoluntterSMSpage</li>
<li>cust_luminate_HTML_sp_VoluntterSMSbutton</li>
<li>cust_luminate_SMS_sp_VoluntterSMSyes</li>
<li>cust_luminate_SMS_sp_VoluntterSMSno</li>
</ul>

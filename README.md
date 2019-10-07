<h1>Arena Volutneer Texting - not ready yet - checkback later</h1>
<p>These stored procedures allow Arena to send Confirmation text messages to schedjuled volunteers.
Due to the nature of the resources being used, this module must only exist through stored procedures making the setup more complicated than a normal module
</p>
<h2>Requirements</h2>
<p>These Stored procedures require the KFS twilio texting module to be installed.</p>
<h2>Instalation</h2>
<ol>
<li>Modify the VolunteerServiceView.ascx file to include the service ID <br> Add this code inside the script tag <br> <code>var serviceID = "<%= Session["_serviceID"] %>";</code></li>
<li>next run the installer script to add the required stored procedures to the database</li>
<li>make a new page in arena and add a "HTML from stored procedure" module to the page with the stored procedure "cust_luminte_HTML_sp_VolunteerSMSpage" and give it the paramaters "@service_id=" and "@redirect_page=3326" setting redirect to any page you want the user to end up at after sending the text</li>
<li>Add another "HTML from stored" module to Volunteer Service View Page with the stored procedure "cust_luminate_HTML_sp_VolunteerSMSbutton" and give the paramater @target_page of the page you created in the previous step</li>
<li>lastly to allow your volunteers to respond and text back add the keywords yes and no to your list of texting keywords and point them to the cust_luminate_sms_sp_yes and cust_luminate_sms_sp_no stored procedures</li>
</ol>
<h2>procedures List</h2>
<p>a list of the stored procedures this installs</p>
<ul>
<li>cust_luminate_VolunteerTexting_sp_HTML</li>
<li>cust_luminate_VolunteerTexting_sp_button</li>
<li>cust_luminate_sms_sp_yes</li>
<li>cust_luminate_sms_sp_no</li>
</ul>

# Email Spam Classifier 
- In this Project we have used Dataset from Apache Spam Assassin's public dataset.

- First We have loaded the Dataset in the notebook using the Python Library email.  
- Next we find the structures of the email and the Frequency of the email associated with them . We get
   - [('text/plain', 2408),  
   ('multipart(text/plain, application/pgp-signature)', 66),  
   ('multipart(text/plain, text/html)', 8),  
   ('multipart(text/plain, text/plain)', 4),  
   ('multipart(text/plain)', 3),  
   ('multipart(text/plain, application/octet-stream)', 2),  
   ('multipart(text/plain, text/enriched)', 1),  
   ('multipart(text/plain, application/ms-tnef, text/plain)', 1),  
   ('multipart(multipart(text/plain, text/plain, text/plain), application/pgp-signature)',  
    1),   
   ('multipart(text/plain, video/mng)', 1),  
   ('multipart(text/plain, multipart(text/plain))', 1),  
   ('multipart(text/plain, application/x-pkcs7-signature)', 1),  
   ('multipart(text/plain, multipart(text/plain, text/plain), text/rfc822-headers)',  
    1),  
   ('multipart(text/plain, multipart(text/plain, text/plain), multipart(multipart(text/plain, application/x-pkcs7-signature)))',  
    1),  
   ('multipart(text/plain, application/x-java-applet)', 1)]

- `Then we Preprocessed the data By`
-  - removing html tags header et.
   - Using the Regular expression  library of python re
   - So from This
   - - ``<HTML><HEAD><TITLE></TITLE><META http-equiv="Content-Type" content="text/html; charset=windows-1252"><STYLE>A:link {TEX-DECORATION: none}A:active {TEXT-DECORATION: none}A:visited {TEXT-DECORATION: none}A:hover {COLOR: #0033ff; TEXT-DECORATION: underline}</STYLE><META content="MSHTML 6.00.2713.1100" name="GENERATOR"></HEAD>``
``<BODY text="#000000" vLink="#0033ff" link="#0033ff" bgColor="#CCCC99"><TABLE borderColor="#660000" cellSpacing="0" cellPadding="0" border="0" width="100%"><TR><TD bgColor="#CCCC99" valign="top" colspan="2" height="27">``
``<font size="6" face="Arial, Helvetica, sans-serif" color="#660000">``
``<b>OTC</b></font></TD></TR><TR><TD height="2" bgcolor="#6a694f">``
``<font size="5" face="Times New Roman, Times, serif" color="#FFFFFF">``
``<b>&nbsp;Newsletter</b></font></TD><TD height="2" bgcolor="#6a694f"><div align="right"><font color="#FFFFFF">``
``<b>Discover Tomorrow's Winners&nbsp;</b></font></div></TD></TR><TR><TD height="25" colspan="2" bgcolor="#CCCC99"><table width="100%" border="0" ''' ``
                                                                                                                   
- - we got this:
  - - ``OTC``  
 ``Newsletter``  
``Discover Tomorrow's Winners ``  
``For Immediate Release``  
``Cal-Bay (Stock Symbol: CBYI)``  
``Watch for analyst "Strong Buy Recommendations" and several advisory newsletters picking CBYI.  CBYI has filed to be traded on the OTCBB, share prices historically INCREASE when companies get listed on this larger trading exchange. CBYI is trading around 25 cents and should skyrocket to $2.66 - $3.25 a share in the near future.``  
``Put CBYI on your watch list, acquire a position TODAY.``  
``REASONS TO INVEST IN CBYI``  
``A profitable company and is on track to beat ALL earnings estimates!``  
``One of the FASTEST growing distributors in environmental & safety equipment instruments.``  
``Excellent management team, several EXCLUSIVE contracts.  IMPRESSIVE client list including the U.S. Air Force, Anheuser-Busch, Chevron Refining and Mitsubishi Heavy Industries, GE-Energy & Environmental Research.``  
``RAPIDLY GROWING INDUSTRY``  
``Industry revenues exceed $900 million, estimates indicate that there could be as much as $25 billi ``  

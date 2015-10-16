# Python Script to send sms messages through way2sms #
A python script to automate  way2sms free sms service. Anybody with a way2sms  username & password can  use this script to send automated sms  messages. You can use this script with open source monitoring tools like nagios to send out alerts.

```
4.2.24$ python sendsms2.py -h
Usage: sendsms2.py -m [number] -t [text]

Options:
  --version             show program's version number and exit
  -h, --help            show this help message and exit
  -m NUMBER, --number=NUMBER
                        Mobile number to send sms
  -t TEXT, --text=TEXT  Text to send
4.2.24$
```

## Sample ##
```
4.2.24$ python sendsms2.py -m 8277123456 -t "this is a test message"
>>> initializing..
>>> Debug: ON
>>> connecting to way2sms...
>>> http://site3.way2sms.com/entry.jsp/HTTP: 200
------------------------------
Free SMS, Send Free SMS, Send Free SMS to india, Free email alerts, email2SMS, SMS Alerts,Bill Reminders, EMI Reminders, Loan Reminders, TV Shows Reminders, Future SMS, Mobile Bill Reminders
------------------------------
>>> http://site1.way2sms.com/Login1.action/HTTP: 200
>>> Received Token: AF35798AE4A8ABD5C47830E370AB327D.w801
>>> sending message...
>>> Opening http://site1.way2sms.com/jsp/SingleSMS.jsp?Token=AF35798AE4A8ABD5C47830E370AB327D.w801
>>> http://site1.way2sms.com/jsp/SingleSMS.jsp/HTTP: 200
>>> Setting InstantSMS form readonly: False.
>>> ID1: tcBcAjBf, ID2: RZYChnN, TKN:aUwnZi
>>> Filling up form details..
>>> submitting...
>>> http://site1.way2sms.com/jsp/stp2p.action/HTTP: 200
>>> Waiting...8 sec/POST wait.
>>> http://site1.way2sms.com/generalconfirm.action?SentMessage=Message+has+been+submitted+successfully&Mnumber=8277200849&Mmess=this+is+a+test+message&Token=AF35798AE4A8ABD5C47830E370AB327D.w801/HTTP: 200
>>> Closing session..
>>> Done.
```
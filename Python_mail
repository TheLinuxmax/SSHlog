# send e-mail with python
import smtplib
from email.mime.multipart import MIMEMultipart
from email.mime.text import MIMEText
from email.mime.image import MIMEImage

# create the email content
msg = MIMEMultipart()
msg['Subject'] = 'Extern IP'
msg['From'] = 'FROMEMAIL'
msg['To'] = 'TOEMAIL'
msg.preamble = 'external ip.'
#Create the email contect

message = """This is the new external ip"""
msg.attach(MIMEText(message))
msg.attach(MIMEText(file("ipnew.txt").read()))

# send the email via Gmail server
username = 'PUTEMAILHERE'
password = 'PUTPASSWORDHERE'
server = smtplib.SMTP('smtp.gmail.com:587') # Gmail rewriting port 25 to port 5$
server.starttls() # Support SMPT AUTH
server.login(username,password)
server.sendmail(msg['From'], msg['To'], msg.as_string())
server.quit()

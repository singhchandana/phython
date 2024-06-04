# phython


steps
Generate OTP --- using random module
Send OTP to user's email adress--- SMTPlib Module
import random
import smtplib
server=smtplib.SMTP('smtp.gmail.com',587)
#adding TLS security 
server.starttls()
#get your app password of gmail ----as directed in the video
password='*************'
server.login(email,password)
#generate OTP using random.randint() function
otp=''.join([str(random.randint(0,9)) for i in range(4)])
msg='Hello, Your OTP is '+str(otp)
sender=''  #write email id of sender
receiver='' #write email of receiver
#sendi
server.sendmail(sender,receiver,msg)
server.quit()

jola
====
# -*- coding: utf-8 -*-



from email.mime import multipart, text



#Tworzenie maila

mail = multipart.MIMEMultipart()

html = u'<h1>Nagłówek</h1><p>Treść</p>'

#Tworzenie części html

msg = text.MIMEText(html.encode('UTF-8'), 'html', 'UTF-8')

#Dołączenie treści html do maila

mail.attach(msg)

#Dołączenie Nagłówków

mail['From'] = u'Imię Nazwisko<mail@example.com>'

mail['Subject'] = u'Temat wiadomości'

#Stworzona wiadomość

print mail.as_string()

--%s--
""" %(filename, filename, encodedcontent, marker)
message = part1 + part2 + part3

try:
   smtpObj = smtplib.SMTP('localhost')
   smtpObj.sendmail(sender, reciever, message)
   print "Successfully sent email"
except Exception:
   print "Error: unable to send email"



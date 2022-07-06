## How contact forms can be exploited to conduct large-scale phishing activity?

A contact form for customer inquiries is one of the most common features present on the websites of most companies. It provides an easy way for prospective customers to get in touch with the company.

WordPress plugins are available that can help you create such functionality in a simple way. Some companies go beyond and acknowledge the message received from the customers. 
### But how can this be leveraged to conduct phishing activity?
During the application security assessment for one of our clients, we came across a Contact Us form that looked like the following image:
![f317a3cebbeb4ce144c63693828565a5.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1657117149412/U6ZhqwY3H.png align="left")
At first glance, the form seems pretty standard and harmless, but just out of curiosity, we entered data and sent our query. We entered the data in the fields. Almost instantly after this, we received a reply from the company, as depicted in the image below:
![screenshot-wesecureapp.com-2022.07.06-19_56_02.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1657117333322/f87w3bJL_.png align="left")
- We then checked if there was any system in place to verify whether the user entering the details actually owns the email ID entered. Turns out, there wasn’t.

On further investigation, it was found that the number of emails that can be sent wasn’t limited to. A POC for how this can be exploited by an attacker is shown in the image below:
![screenshot-wesecureapp.com-2022.07.06-19_57_44.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1657117446265/w_AnhVM4W.png align="left")
From the above email, it can be seen that without any restrictions, the attacker can redirect the user to any vulnerable link.

Furthermore, the attackers also don’t have to set up their own phishing infrastructure. They also don’t have to spend effort on account takeover of legit emails that is normally done in the email reply chain. 

Since the email is coming from the domain of a company that already has a reputation and proper records in place, the chances of the email landing in SPAM also turn out to be very low. With careful planning regarding the timing and crafting of highly enticing content, a large-scale phishing campaign can be conducted with the help of this form with a high degree of decisiveness. 
### This can lead to several impacts on the organization:
- Exhausting the email supply of the domain.
- Defaming the company by sending false advertisements to multiple people.
- Sending multiple emails to downgrade the reputation of the domain so that even legit emails start landing in spam.
- Attacking and disrupting the businesses of existing customers of the company by sharing misleading information through this email
### Now, how to mitigate phishing activity?
The perfect solution to this will be not to send the message entered in the Contact Form as an acknowledgment. If it is a really highly desired feature, a more extensive message can be included at the beginning of the reply mail. Also, a link for reporting suspicious emails can be set up to detect an attack, and it should be included in the main content of the message rather than the Disclaimer.
For example, instead of
![screenshot-wesecureapp.com-2022.07.06-20_02_43.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1657117768277/vfwzzK-2H.png align="left")
The reply email can contain a message with much more clarity:
![screenshot-wesecureapp.com-2022.07.06-20_02_56.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1657117789340/idF70aGtO.png align="left")
- The user control over the email content and the body should be removed completely if sending only an acknowledgment is required. 
A simple message like the following can be sent for acknowledgment:
![screenshot-wesecureapp.com-2022.07.06-20_03_10.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1657117828085/r-l3N-MD2.png align="left")
To prevent the misuse of the form by someone sending too many emails, captchas can be implemented.
In addition to this, rate-limiting mechanisms should be implemented to limit the number of requests.
Along with this, proper monitoring systems should be in place to check how many emails are being sent from your organization’s account. If there is a heightened activity that is different from the normal rate of sending, an alert system should be in place so that proper corrective action can be taken.


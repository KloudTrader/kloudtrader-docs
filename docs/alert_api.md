---
id: alert_api
title: Alerts
sidebar_label: Alerts
---
## With libkloudtrader, you can create customized alerts for both SMS and Email. Never miss out on what's your algorithm is upto.


# Module

#### <code>libkloudtrader.alert_me</code>
*** 

### SMS alerts 
<code>sms(number,message)</code>

| Paramters     | Required/Optional | Description                        | Type |
|--------------|-------------------|-------------------------------------|------|
| number       | required          | Number you want to receive alert on | str  |
| message      | required          | Message for the alert               | str  |


#### Example
<!--DOCUSAURUS_CODE_TABS-->
<!--Python 🐍 -->

``` python

from libkloudtrader.alert_me import sms

if certain_condition is met:
    message="{} is met".format(certain_condition)
    sms('+16xxxxxxxxx',message)
```
```python
return type: Bool

Thursday, August 29, 2019 04:51:34 PM INFO: Alert Created for +16xxxxxxxxx
```
<!--END_DOCUSAURUS_CODE_TABS-->

*** 
### Email alerts 
<code>email(email_id,message)</code>
| Paramters    | Required/Optional | Description                           | Type |
|--------------|-------------------|---------------------------------------|------|
| email_id     | required          | Email Id you want to receive alert on | str  |
| message      | required          | Message for the alert               | str  |

#### Example

<!--DOCUSAURUS_CODE_TABS-->
<!--Python 🐍 -->

```python 

from libkloudtrader.alert_me import email

if particular_condition is met:
    message="{} is met".format(particular_condition)
    email('123@abc.com',message)
```

```python
return type: Bool

Thursday, August 29, 2019 04:51:36 PM INFO: Alert Created for 123@abc.com
```
<!--END_DOCUSAURUS_CODE_TABS-->

*** 
### Both sms and email alerts
<code>sms_and_email(number,email_id,message)</code> 
| Paramters    | Required/Optional | Description                           | Type |
|--------------|-------------------|---------------------------------------|------|
| number       | required          | Number you want to receive alert on   | str  |
| email_id     | required          | Email Id you want to receive alert on | str  |
| message      | required          | Message for the alert                       | str  |

#### Example

<!--DOCUSAURUS_CODE_TABS-->
<!--Python 🐍 -->

```python 

from libkloudtrader.alert_me import sms_and_email

if some_condition is met:
    message="{} is met".format(some_condition)
    sms_and_email('+16xxxxxxxxx','123@abc.com',message)
```

```python
return type: Bool

Thursday, August 29, 2019 04:51:44 PM INFO: Alert Created for +16xxxxxxxxx
Thursday, August 29, 2019 04:51:46 PM INFO: Alert Created for 123@abc.com
```
<!--END_DOCUSAURUS_CODE_TABS-->
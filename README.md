# Cockpit CMS Registration API

## Configuration

#### (1) Add SMTP config to `config/config.yaml` file

```
## Cockpit settings

mailer: 
      from : noreply@mailtrap.io
      from_name : My Company
      transport : smtp
      host : smtp.mailtrap.io
      user : username123
      password : password1234
      port : 465
      auth : true
      encryption: ssl
```

#### (2) Create a group called `user`
It's ok to create directly in `config.yaml` or with [this Groups Addon](https://github.com/serjoscha87/cockpit_GROUPS)

> Note: If you're in Cockpit CMS v2, it's not neccessary to create a **group**. You only have to create a **role** named "user".

--------------------------

## Installation

#### Download this repo, pick one folder that match your Cockpit CMS version. 
> E.g I'm using Cockpit CMS v2, so I copy only `cockpit-register-v2` folder into Cockpit's `addons` folder. 

---------------------------

## Register via API

#### Route

```
/api/register
```

#### Payload Example [post method]

```javascript
{
  "user":{
      "name":"Tester",
      "user":"tester",
      "email":"youremail@gmail.com",
      "password":"123456"
  }
}
```

----------

![Screenshot from 2022-09-14 22-51-18](https://user-images.githubusercontent.com/33022876/190211204-abededa3-89c0-4035-8781-aca7cea8192e.jpeg)

-------------

> Firstly, it will register as an inactive account and will send a confirmation email, after user click on confirmation button it will activate the account and he/she will be able to login.

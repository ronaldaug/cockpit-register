# Cockpit Registration API

## Configuration

#### (1) Add SMTP config to `config/config.yaml` file

```
# Cockpit settings

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

#### (2) Create a user group with [Groups Addon](https://github.com/serjoscha87/cockpit_GROUPS)

--------------------------

## Installation

#### Download this repo, rename the folder as `register` and add it in `addons` folder of cockpit cms.

---------------------------

## Register via API

#### Route

```
/api/register
```

#### Payload Example

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

> Firstly, it will register as an inactive account and will send a confirmation email, after user click on confirmation button it will activate the account and he/she will be able to login.
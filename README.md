# SendGrid Mail Action

This actions send a mail using the SendGrid API to the defined mails

## Inputs

### `sendgrid-token`

**Required** The token of the SendGrid that will be used.

### `mail`

**Required** The mail/mails at which the mails will be send. Can be one or more. For example
```
  mail: a.mail@mail.to,b.mail@mail.to
``` 
where "," can be anything as it can be defined at the splitterator.

### `from`

**Optional** The mail that will be shown as the sender. Default : "sendgridmailaction@github.com"

### `subject`

**Optional** The subject of the mail. Default: GitHub action notification

### `individual`

**Optional**  Defines if it should be one email with multiple address or multiple emails with a single address
      
### `text`

**Optional** The subject of the mail. Variables $EVENT$, $ISSUE$, $ACTION$'. Default: The following action $ACTION$ produced an event $EVENT$ 

### `splitterator`

**Optional** The splitterator used for the mail list. Default: ',' 


## Example usage
```
- name: SendGrid Action
  uses: mmichailidis/sendgrid-mail-action@v1.0
  with:
    sendgrid-token: 'sample'
    mail: 'a.mail@mail.to'
```

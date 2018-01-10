## Registration
### /login

#### Request
_Either `familyName` or `familyId` is required.  If `familyId` is provided `familyName`, if provided, is ignored._
```json
{
  "action" : "register",
  "email" : "mamabird@mamabird.biz",
  "password" : "********",
  "familyName" : "The MamaBird Family",
  "familyId" : "abcd-1234-effe-5678-dcba"
}
```

#### Response
_The `familyId` of the family.  If this is a new family, the id is generated and returned._
```json
{
  "familyId" : "abcd-1234-effe-5678-dcba"
}
```

## Login
### /login

#### Request
```json
{
  "action" : "login",
  "email" : "mamabird@mamabird.biz",
  "password" : "********",
}
```

#### Response
_The `familyId` of the family of the user.  If this is a new family, the id is generated and returned._
```json
{
  "familyId" : "abcd-1234-effe-5678-dcba"
}
```

## Password Recovery
### /login

#### Request
```json
{
  "action" : "recoverPassword",
  "email" : "mamabird@mamabird.biz"
}
```

#### Response
```json
{}
```

## Change Password
### /login

#### Request
```json
{
  "action" : "changePassword",
  "email" : "mamabird@mamabird.biz",
  "authenticationToken" : "******************",
  "password" : "new password"
}
```

#### Response
```json
{
  "familyId" : "abcd-1234-effe-5678-dcba"
}
```

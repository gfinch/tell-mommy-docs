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


## Add Child
### /family

#### Request

```json
{
  "action" : "addChild",
  "familyId" : "abcd-1234-effe-5678-dcba",
  "name" : "Peter"
}
```

#### Response
```json
{
  "familyId" : "abcd-1234-effe-5678-dcba",
  "childId" : "dcba-1234-effe-5678-abcd"
}
```

## List Children
### /family

#### Request

```json
{
  "action" : "listChildren",
  "familyId" : "abcd-1234-effe-5678-dcba"
}
```

#### Response
```json
{
  "familyId" : "abcd-1234-effe-5678-dcba",
  "children" : [
    {"name" : "Peter", "childId": "dcba...", "nicknames" : ["Pete", "Peter the Magnificent"], "pronunciation" : "ˈpi.tɚ"},
    {"name" : "Susan", "childId": "abcd...", "nicknames" : ["Sue", "Susan the Gentle"], "avatar" : "datauri://bytes"},
    {"name" : "Edmund", "childId": "1234...", "nicknames" : ["Ed", "Edumund the Just"]},
    {"name" : "Lucy", "childId": "9876...", "nicknames" : ["Lucy the Valient"]}
  ]
}
```

## Edit Child
### /family

#### Request
```json
{
  "action" : "editChild",
  "childId" : "dcba-1234-effe-5678-abcd",
  "name" : "Peter",
  "nicknames" : ["Pete"],
  "avatarData" : "base64encoded bytes",
  "pronunciation" : "ˈpi.tɚ"
}
```

#### Response
```json
{
  "familyId" : "abcd-1234-effe-5678-dcba",
  "childId" : "dcba-1234-effe-5678-abcd",
  "name" : "Peter",
  "nicknames" : ["Pete", "Peter the Magnificent"],
  "avatarData" : "base64encoded bytes",
  "pronunciation" : "ˈpi.tɚ"
}
```

## Remove Child
### /family

#### Request

```json
{
  "action" : "removeChild",
  "familyId" : "abcd-1234-effe-5678-dcba",
  "childId" : "dcba-1234-effe-5678-abcd"
}
```

#### Response
```json
{}
```

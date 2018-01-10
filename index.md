## Registration
### /login

### Request
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

### Response
_The `familyId` of the family.  If this is a new family, the id is generated and returned._
```json
{
  "familyId" : "abcd-1234-effe-5678-dcba"
}
```

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/gfinch/tell-mommy-docs/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.

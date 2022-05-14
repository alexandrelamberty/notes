---
author: 
title: NestJS 
description: | Framework for building efficient, scalable Node.js web
applications 
category: Framework
tags: [framework,typescript]
created: 2021-10-23T20:38:59+02:00
updated: 2021-10-23T20:38:59+02:00
---

# NestJS

## FileInterceptor

```typescript
UseInterceptors(
  FileInterceptor('companyLogo', {
    storage: diskStorage({
      destination: (req, file, cb) => {
        cb(null, './uploads/companies')
      },
      filename: (req, file, cb) => {
        cb(null, `${file.originalname}`)
      },
    }),
    fileFilter: (req, file, cb) => {
      let ext = extname(file.originalname)
      if (
        ext !== '.png' &&
        ext !== '.jpg' &&
        ext !== '.gif' &&
        ext !== '.jpeg'
      ) {
        return cb(
          new HttpException('Only images are allowed!', HttpStatus.BAD_REQUEST),
          null
        )
      }
      cb(null, true)
    },
    limits: { fileSize: 1024 * 1024 },
  })
)
```

## References

- [NestJS](https://nestjs.com/)
- [Documentation - NestJS](https://docs.nestjs.com/)

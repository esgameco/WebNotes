# JWT Implementation

[Docs](https://www.npmjs.com/package/jsonwebtoken)

## Basic Usage

```typescript
import { sign, verify } from 'jsonwebtoken';

const token: string = sign({payload}, {secretKey});
const payload: boolean = verify(token, {secretKey}); 
```
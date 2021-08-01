# Default Way

## Set Header

### Next.js

```typescript
import type { NextApiRequest, NextApiResponse } from 'next'

const handler = (req: NextApiRequest, res: NextApiResponse<Data>) => {
    res.setHeader('Set-Cookie', 'test=true; path=/');
};

export default handler;
```

## Read Header

### Next.js

```typescript
import type { NextApiRequest, NextApiResponse } from 'next'
import assert from 'assert';
import cookie from 'cookie';

const handler = (req: NextApiRequest, res: NextApiResponse<Data>) => {
    const {test} = cookie.parse(req.headers.cookie);
    assert(test === 'true');
};

export default handler;
```
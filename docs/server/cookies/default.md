# Default Way

## Set Header

### Next.js

```typescript
import type { NextApiRequest, NextApiResponse } from 'next'

const handler = (req: NextApiRequest, res: NextApiResponse<Data>) => {
    res.setHeader('Set-Cookie', 'test=true');
};

export default handler;
```
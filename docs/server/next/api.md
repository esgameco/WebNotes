# Next.js API

## Directory

The api lies at 'pages/api'.

## Api Handling

To handle an api request, a handler function with req and res params is required.  
The res param must have a specific type as defined by the user.  

```typescript
import type { NextApiRequest, NextApiResponse } from 'next'

type Data = {
}

const handler = (req: NextApiRequest, res: NextApiResponse<Data>) => {
}

export default handler;
```
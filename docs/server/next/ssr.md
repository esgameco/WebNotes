# Next.js Rendering

## Props

### Static Page Generation

In order to interact with data from an api, one must use a special function called getStaticProps.  
The react component is passed the return value of getStaticProps within the same file.

```typescript
import { GetStaticProps, GetStaticPropsContext } from 'next';
import axios, { AxiosResponse } from 'axios';

type IP = {
    ip: string;
};

// Ran at build time
export const getStaticProps: GetStaticProps = async (context: GetStaticPropsContext) => {
    const res: AxiosResponse = await axios.get('http://www.httpbin.org/ip');
    return res.data;
};

const Page = ({ip}: IP) => {
    return (
        <p>{ip}</p>
    );
};

export default Page;
```

### Dynamic Page Generation

Server-Side Rendering uses the same technique as generation but uses getServerSideProps instead.

```typescript
import { GetServerSideProps, GetServerSidePropsContext } from 'next';
import axios, { AxiosResponse } from 'axios';

type IP = {
    ip: string;
};

export const getServerSideProps: GetServerSideProps = async (context: GetServerSidePropsContext) => {
    const res: AxiosResponse = await axios.get('http://www.httpbin.org/ip');
    return res.data;
};

const Page = ({ip}: IP) => {
    return (
        <p>{ip}</p>
    );
};

export default Page;
```


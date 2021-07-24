# Connect to Database

Postgres

```typescript
import { Sequelize } from 'sequelize';

const sequelize = new Sequelize({database}, {username}, {password}, {
    host: {host},
    dialect: 'postgres',
    port: {port}
});
```
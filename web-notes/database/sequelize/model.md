# Model in Sequelize

<!-- TODO: Test if it works -->
Basic model

<!-- TODO: Understand what everything does -->
```typescript
import {
    Model
} from 'sequelize';

interface UserAttributes {
    id: number,
    name: string
}

class User extends Model<UserAttributes> implements UserAttributes {
    public id!: number;
    public name!: string;

    public readonly createdAt!: Date;
    public readonly updatedAt!: Date;
}
```
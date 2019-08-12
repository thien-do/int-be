This is a mock back end for [InterNations' Front End challenge](https://github.com/dvkndn/int-fe/blob/master/TASK.pdf). It uses [JSON Server](https://github.com/typicode/json-server) and deployed to https://int-be.herokuapp.com/.

For the front end implementation, please see http://github.com/dvkndn/int-fe.

**Models**

For the challenge, the mock back end serves 2 simple models:

```ts
interface Group {
  id: string;
  name: string;
  /* ... */
}

interface User {
  id: string;
  email: string;
  /* ... */
}
```

For detail structure and implementation, please see [db.js].

To represent the concept that a user may belong to several groups, and a group may have several users, the back end also implemented a simple many-to-many model:

```ts
interface Link {
  id: string;
  groupId: string;
  userId: string;
}
```

Thanks to the versatility of JSON Server, the 3 models should be enough to server most, if not all, cases of the challenge.
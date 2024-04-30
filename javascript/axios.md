---
title: Ajax using axios
description: Fetch
date: 2020-01-12
duration: ~20 mins
layout: layouts/post.njk
---

#### Axios Library

- https://www.npmjs.com/package/axios ( ~ 18M Weekly Downloads)

- CDN
  - https://cdnjs.com/libraries/axios

  ```js
  <script src="https://cdnjs.cloudflare.com/ajax/libs/axios/0.21.1/axios.min.js" integrity="sha512-bZS47S7sPOxkjU/4Bt0zrhEtWx0y0CRkhEp8IckzK+ltifIIE9EMIMTuT/mEzoIMewUINruDBIR/jJnbguonqQ==" crossorigin="anonymous" referrerpolicy="no-referrer"></script>
  ```

#####  REST API

- List all users  (GET)
- List all users for the given role (GET)
- Get user by id (GET)
- Add User Detail (POST)
- Update user details (PUT)
- Update Password (PATCH)
- Delete user by id (DELETE)

###### 1. Get all Users Details

- GET API

```js
    const url = "http://localhost:8080/api/v1/users";
    axios.get(url).then(res=>{
      const users = res.data;
      console.table(users);
    });
```

###### 2. Get all Users Details for the given role

- GET API with Query Params
- Query Param:role=USER

```js
    const url = "http://localhost:8080/api/v1/users?role=USER";
    axios.get(url).then(res=>{
      const users = res.data;
      console.table(users);
    });
```

###### 3. Get User Detail for the given id

- GET API with Path Variable
- Path Variable : id

```js
    const id = 1;
    const url = "http://localhost:8080/api/v1/users/"+ id ;
    axios.get(url).then(res=>{
      const user = res.data;
      console.log(user);
    });
```

###### 4. Add User Detail

- POST

```js
    const userDetail = { name: "Naresh", email:"n@gmail.com" , password:"pass123", role:"USER"};

    const url = "http://localhost:8080/api/v1/users";
    axios.post(url, userDetail).then(res=>{
      let result = res.data;
      console.log(result);
    });
```

###### 5. Update User Detail

- PUT
- Path Variable : id

```js
    const userDetail = { id: 1, name: "Naresh Kumar", email:"n1@gmail.com" , password:"pass1234", role:"USER"};

    const url = "http://localhost:8080/api/v1/users/" + userDetail.id;
    axios.put(url, userDetail).then(res=>{
      let result = res.data;
      console.log(result);
    });
```

###### 6. Change Password

- Patch - Partial Update
- Path Variable : id

```js
    const userDetail = { id: 1, password:"pass1234"};

    const url = "http://localhost:8080/api/v1/users/" + userDetail.id;
    axios.patch(url, userDetail).then(res=>{
      let result = res.data;
      console.log(result);
    });
```


###### 6. Delete User detail by id

- DELETE with path variable
- Path Variable : id

```js
    const id = 1;
    const url = "http://localhost:8080/api/v1/users/" + userDetail.id;
    axios.delete(url).then(res=>{
      let result = res.data;
      console.log(result);
    });
```


##### Exception Handling

- add catch block

```js
  axios.get(url).then(res=>{
    console.log(res.data);
  }).catch(err=>{
    console.log(err?.response?.data);
  });
```

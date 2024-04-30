---
title: Interceptor - axios
description: 
date: 2022-11-03
day: 10
duration: ~10 mins
tags:
  - nextjs
layout: layouts/post.njk
---

### Interceptor - Axios

* .env
```bash
  NEXT_PUBLIC_BACKEND_BASE_URL=http://localhost:8080
  NEXT_PUBLIC_FRONTEND_APP_HOST_DOMAIN_URL=http://localhost:3000
```

```tsx
  
  import axios from "axios";
  import toast from "react-hot-toast";

  const axiosInstance = axios.create();

  axiosInstance.interceptors.request.use((config) => {
    config.withCredentials = true;
    config.baseURL = process.env.NEXT_PUBLIC_BACKEND_BASE_URL;
    return config;
  });

  axiosInstance.interceptors.response.use(
    (response) => {
      return response;
    },
    async (error) => {
      if (error.response && error.response.status === 401) {
        console.log("Unauthorized request:", error.response);

        toast.error("Unauthorized Access")
        window.location.href = `${process.env.NEXT_PUBLIC_FRONTEND_APP_HOST_DOMAIN_URL}/login`;
        return;
        
      }
      return Promise.reject(error);
    }
  );

  export { axiosInstance };


```
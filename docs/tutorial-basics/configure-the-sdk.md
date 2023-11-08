---
sidebar_position: 1
---



# Configure the SDK

## React Example

### Add CSS to your application
```jsx title="src/App.js"
import '@neio/chat/dist/index.css'
```


```jsx title="src/App.js"
import Neio from '@neio/chat'
import {useEffect} from "react";

export default function MyReactPage() {
    // you need to generate the token from using Nei Auth API
    // get token from your preferred storage
    const token = localStorage.getItem('token'); 
    
    useEffect(()=>{
        Neio.configure('#app', {access_token})
    },[]);
    
    return (
        <Layout>
            <h1>My React page</h1>
            <p>This is a React page</p>
        </Layout>
    );
}
```

## Vue Example

###  Add CSS to your application
```vue title="src/App.vue"
<script setup lang="ts">
  import '@neio/chat/dist/index.css'
</script>
```

```vue title="src/App.vue"
<script setup lang="ts">
  import { onMounted } from 'vue';
  import Neio from '@neio/chat';
  import { useAuthStore } from 'stores/auth-store';
  
  onMounted(()=>{
    // you need to generate the token from using Nei Auth API
    // get token from your preferred storage
      const token = useAuthStore().access_token;
      Neio.configure('.q-layout', {token});
  });
</script>
```

A new neio chat icon is now available on all your pages.

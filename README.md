## Vue2NetworkStatus
A simple component that analyze network status powered by Vue2

### Installation
```
npm i vue2-network-status --save
```

or CDN by Unpkg
```
<script src="https://unpkg.com/vue2-network-status@1.0.0/dist/vue2-network-status.min.js"></script>
```
View a [Demo](http://vue2-network-status.s3-website.us-east-2.amazonaws.com/)

### Or
``` javascript
import Vue2NetworkStatus from 'vue2-network-status';
```

Register component
``` javascript
export default {
  name: 'MyApp',
  components: {
    Vue2NetworkStatus
  },
};
```

Add component on html
``` html
<Vue2NetworkStatus>You Are Offline!</Vue2NetworkStatus>
```

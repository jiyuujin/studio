# nekohack Studio

I have used [Amplify Studio](https://docs.amplify.aws/console/) in experimental

![](https://i.imgur.com/kczwQR1.jpg)

Please check `Local setup instructions` in Amplify Studio

```bash
amplify pull --appId <APP_ID> --envName staging
```

All components are generated in `src/ui-components`

## Usage

Install [`@aws-amplify/ui-react`](https://www.npmjs.com/package/@aws-amplify/ui-react)

```bash
# @aws-amplify/ui-react
npm install @aws-amplify/ui-react
yarn add @aws-amplify/ui-react
```

Wrap the root component using `AmplifyProvider` at `src/index.tsx`

```tsx
import React from 'react'
import ReactDOM from 'react-dom'

import Amplify from 'aws-amplify'
import '@aws-amplify/ui-react/styles.css'
import { AmplifyProvider } from '@aws-amplify/ui-react'
import App from './App'

import awsconfig from './aws-exports'

Amplify.configure(awsconfig)

ReactDOM.render(
    <React.StrictMode>
        <AmplifyProvider>
            <App />
        </AmplifyProvider>
    </React.StrictMode>,
    document.getElementById('root')
)
```

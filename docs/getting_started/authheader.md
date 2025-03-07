---
title: Auth Header - React Auth Kit
description: Get the formatted authentication token by just calling Auth Header hook or Higher order component and pass it to all the API calls.
---


# Auth Header  :material-ip-network:

<div data-ea-publisher="authkitarkadipme" data-ea-type="text" id="authheader"></div>

Get the Auth Header for future requests from any Component simply by using `HOC` or `Hooks`

- For Functional Components, you can use `#!js useAuthHeader()` hook inside any components
- For class-based components, you can wrap the component inside `#!js withAuthHeader()` HOC function.


## Hook

### Import

```js title="Import useAuthHeader in your app"
import useAuthHeader from 'react-auth-kit/hooks/useAuthHeader';
```

### Usage

```jsx title="SecureComponent.js"
import React from 'react'
import useAuthHeader from 'react-auth-kit/hooks/useAuthHeader';

const SomeComponent = () => {
    const authHeader = useAuthHeader()

    return(
        <div>
            {authHeader}
        </div>
    )
}
```

### API

[reference/react-auth-kit/hooks/useAuthHeader](./../reference/react-auth-kit/hooks/useAuthHeader.md)

## Higher Order Component

### Import

```js title="Import withAuthHeader in your app"
import withAuthHeader from 'react-auth-kit/hoc/withAuthHeader';
```

### Usage

```jsx title="SecureComponent.js"
import React from 'react';
import withAuthHeader from 'react-auth-kit/hoc/withAuthHeader';

class SomeComponent extends React.Component {
    render(){
        return (
            <div>
                {this.props.authHeader}
            </div>
        )
    }
}

export default withAuthHeader(SomeComponent)
```

### API

[reference/react-auth-kit/hoc/withAuthHeader](./../reference/react-auth-kit/hoc/withAuthHeader.md)

---

<p align="center">&mdash; 🔑  &mdash;</p>
<p align="center"><i>React Auth Kit is <a href="https://github.com/react-auth-kit/react-auth-kit/blob/master/LICENSE">MIT License</a> code</i></p>

<div align="center"><a href="https://react-forme.now.sh/"><img src="https://raw.githubusercontent.com/bluebill1049/react-forme/master/website/logo.png" alt="React forme Logo - React hook form valiation" width="500px" /></a></div>

> React form management without the hassle 

[![Tweet](https://img.shields.io/twitter/url/http/shields.io.svg?style=social)](https://twitter.com/intent/tweet?text=React+Forme&url=https://github.com/bluebill1049/react-forme)&nbsp;[![CircleCI](https://circleci.com/gh/bluebill1049/react-forme.svg?style=svg)](https://circleci.com/gh/bluebill1049/react-forme) [![Coverage Status](https://coveralls.io/repos/github/bluebill1049/react-forme/badge.svg?branch=master)](https://coveralls.io/github/bluebill1049/react-forme?branch=master) [![npm downloads](https://img.shields.io/npm/dm/react-forme.svg?style=flat-square)](https://www.npmjs.com/package/react-forme)
[![npm](https://img.shields.io/npm/dt/react-forme.svg?style=flat-square)](https://www.npmjs.com/package/react-forme)
[![npm](https://img.shields.io/npm/l/react-forme.svg?style=flat-square)](https://www.npmjs.com/package/react-lazyload-image)

- Super easy to create forms and integrate
- Build with React hook, performance and developer experience in mind
- Follow html standard for validation
- Tiny size without other dependency 2 kB (minified + gzipped)
- Build a quick form with [form builder](https://react-forme.now.sh/builder)

## Install

    $ npm install react-forme

## [Website](https://react-forme.now.sh/api)

- [API](https://react-forme.now.sh/api)
- [Demo](https://react-forme.now.sh)
- [Form Builder](https://react-forme.now.sh/builder)

## Quickstart

```jsx
import useForm from 'react-forme';

function App() {
    const { register, handleSubmit, errors } = useForm();
    const onSubmit = (data) => { console.log(data); }
    console.log(errors);
    
    return <form onSubmit={handleSubmit(onSubmit}>
        <input name="firstname" ref={(ref) => register({ ref, required: true })} />
        <input name="lastname" ref={(ref) => register({ ref, pattern: "[a-z]{1,15}" })} />
        <input type="submit" />
    </form>
}

```

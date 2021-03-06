## Hanifrev's Error Documentation

---

### ReactJS

- **_Image from API unable to load on react_**
  > https://stackoverflow.com/questions/60622180/display-image-from-api-in-react
- **_Fetch api react hooks_**
  > https://medium.com/thecodefountain/fetch-api-data-using-useeffect-react-hook-465809ca12c6
- **_Runtime Generator_**
  > add babel plugin transform runtime
- **_Props in link react router_**
  > https://stackoverflow.com/questions/30115324/pass-props-in-link-react-router
- **_Error handling in react hooks_**
  > https://medium.com/technofunnel/error-handling-in-react-hooks-e42ab91c48f4
- **_Pass variable parameter api url_**
  > https://stackoverflow.com/questions/50421683/react-js-how-do-i-pass-variables-parameters-to-the-api-url
- **_Reload page when clicking on react link_**
  > https://reactgo.com/react-refresh-page/
- **_Favicon not displayed_**
  > https://stackoverflow.com/questions/37298215/add-favicon-with-react-and-webpack
- **_PWA manifest (if manualy not working or error)_**
  > https://www.npmjs.com/package/webpack-pwa-manifest
- **_Router page not found on netlify (and reload not found)_**

  > https://community.netlify.com/t/netlify-page-not-found-when-sharing-react-router-dom-based-links/11744/5 looks jaylowe1's answer on Apr 20,

  ```
  "build": "webpack --mode=production && echo '/* /index.html 200' | cat >dist/_redirects",
  ```

---

### Vanilla CSS

- **_Prevent page margin expand_**
  ```
  overflow: hidden (on containter)
  ```
- **_Custom media queries on css framework_**

  > https://stackoverflow.com/questions/45847090/media-queries-in-material-ui-components

- **_Vertical Center_**

  > https://davidwalsh.name/css-vertical-center

  ```
    top: 50%;
    transform: translateY(-50%);
    position: relative;
    overflow: hidden;
  ```

  ANOTHER METHOD

  ```
    margin: 0;
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    width: 100%; //optional, if the content and image position are broken
  ```

- **_Overflow hidden on position:absolute_**

  > put overflow: hidden on the content that contain position:absoulute, or on it's container
  > https://stackoverflow.com/questions/5513382/absolute-position-and-overflowhidden

---

### Tailwind CSS

- **_Intellisense_**
  > if not working try to disable, reload, then enable, reload ctrl + space to view

---

### NextJS

- **_Import font (custom font)_**

  >

  ```
  customFont={
        <link
          href="https://fonts.googleapis.com/css2?family=Ubuntu&display=swap"
          rel="stylesheet"
        />
      }
  ```

  Put inside of <head />, then use it {fontFamily: 'font_name'}

- **_id="\_\_next" styling_**
  > https://github.com/vercel/next.js/issues/4834
  ```
  <Root theme={theme} scheme={scheme} className="overflow">
    	<style>
        {`
      	    #__next { overflow: hidden }
          `}
    	</style>
  ....
  </Root>
  ```
- **_NODE_ENV is not recognized as an internal or external command, operable program or batch file._**

  > https://github.com/laggingreflex/win-node-env

  ```
  npm install -g win-node-env
  ```

- **_if there is error on console.log [forwardRef (container)]_**
  > its means that there is an empty active container,
  > disable the whole container or fill it with something

---

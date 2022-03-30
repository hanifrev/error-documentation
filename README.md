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

- **_Cannot read property 'map' of undefined with react hooks_**

  > https://stackoverflow.com/a/55667055/11358449 > https://www.debuggr.io/react-map-of-undefined/

  Add inline If with Logical && Operator (https://reactjs.org/docs/conditional-rendering.html#inline-if-with-logical--operator)

  ```
  {items && items.map(item => {
    return <div key={item.id}>{item.title}</div>;
  })}
  ```

- **_Put two state on event/function/attribute_**

  > https://stackoverflow.com/questions/68380457/setting-two-state-variable-onclick-in-react

  ```
  onClick={() => {
      setState1(true);
      setState2(false)
      }
    }
  ```

---

### Javascript Related

- **_Get unique value_**
  ```
  [...new Set(a)]
  ```
  ```
  const numbers = [2,3,4,4,2,3,3,4,4,5,5,6,6,7,5,32,3,4,5]
  console.log([...new Set(numbers)]) // [2, 3, 4, 5, 6, 7, 32]
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

- **_CSS Ternary Operator_**

  > https://stackoverflow.com/a/66387037/11358449

- **_Image Resize & Keep Aspect ratio_**
  ```
      object-fit: cover;
      width: 100%;
      height: 250px;
  ```
  > https://stackoverflow.com/a/39039206

---

### Tailwind CSS

- **_Intellisense_**

  > if not working try to disable, reload, then enable, reload ctrl + space to view

- **_Tailwind not working_**
  > check tailwind.config, on purge, usually missing path (src), try this:
  > purge: ['./pages/**/*.{js,ts,jsx,tsx}','./src/components/**/*.{js,ts,jsx,tsx}'],

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

- **_next/image Unconfigured Host_**

  > https://nextjs.org/docs/messages/next-image-unconfigured-host

  Add the hostname of your URL to the images.domains config in next.config.js

  ```
  module.exports = {
    images: {
      domains: ['assets.example.com'],
    },
  }
  ```

- **_Dynamic Routing getServerSideProps_**

  > https://github.com/vercel/next.js/discussions/13309 > https://stackoverflow.com/questions/61222726/dynamic-routing-with-getserversideprops-in-nextjs/61240697#61240697

  ```
  export async function getServerSideProps(context) {
  const { id } = context.query;
  const res = await fetch(`https://restcountries.eu/rest/v2/name/${id}`);
  const country = await res.json();

  console.log(`Fetched place: ${country.name}`);
  return { props: { country } };

  ```

- **_Data Fetching_**

  > https://stackoverflow.com/a/69075605/11358449

  > You can only use getInitialProps, getServerSideProps, getStaticProps in Next.js PAGES folder, these methods will not work outside pages folder

- **_Get query string params from URL_**

  > https://stackoverflow.com/a/61969441/11358449
  >
  > Use getInitialProps methods,

  ```
  const Index = ({id}) => {
  return(<div>{id}</div>)
  }

  Index.getInitialProps = async ({ query }) => {
    const {id} = query

    return {id}
  }
  ```

---

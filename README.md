###REACTJS
-Image from API unable to load on react
https://stackoverflow.com/questions/60622180/display-image-from-api-in-react

-Fetch api react hooks
https://medium.com/thecodefountain/fetch-api-data-using-useeffect-react-hook-465809ca12c6

-Runtime Generator
add babel plugin transform runtime

-Props in link react router
https://stackoverflow.com/questions/30115324/pass-props-in-link-react-router

-error handling
https://medium.com/technofunnel/error-handling-in-react-hooks-e42ab91c48f4

-pass variable parameter api url
https://stackoverflow.com/questions/50421683/react-js-how-do-i-pass-variables-parameters-to-the-api-url

-reload page when clicking on react link
https://reactgo.com/react-refresh-page/

-favicon not showed
https://stackoverflow.com/questions/37298215/add-favicon-with-react-and-webpack

-pwa manifest (if manualy not working or error)
https://www.npmjs.com/package/webpack-pwa-manifest

-router page not found on netlify (and reload not found)
https://community.netlify.com/t/netlify-page-not-found-when-sharing-react-router-dom-based-links/11744/5 looks jaylowe1's answer on Apr 20,
"build": "webpack --mode=production && echo '/\* /index.html 200' | cat >dist/\_redirects",

===========================================
###VANILLA CSS
-Prevent page margin expand
overflow: hidden on containter

===========================================
###TAILWINDCSS
-Intellsene
if not working try to disable, reload, then enable, reload
ctrl + space to view

==========================================
###NEXTJS
-import font
*put this inside <head />
customFont={
<link
            href="https://fonts.googleapis.com/css2?family=Ubuntu&display=swap"
            rel="stylesheet"
          />
}
*then use it, fontFamily: 'font_name'

-id="**next" styling
https://github.com/vercel/next.js/issues/4834
<Root theme={theme} scheme={scheme} className="overflow">
<style>
{` #**next { overflow: hidden }
`}
</style>
....
</Root>

-NODE_ENV is not recognized as an internal or external command, operable program or batch file.
_ npm install -g win-node-env
_ https://github.com/laggingreflex/win-node-env

# ps-hud Editing Guide
 A simple unofficial how-to guide on editing and compiling svelte typescript for Project Sloth ps-hud for QBCore FiveM

## Step 1 - install base tools
    Install nodejs https://nodejs.org/en/

    Install cygwin http://www.cygwin.com/install.html

## Step 2 - install nodejs npm/pnpm packages	BASH PROMPT

    Open cygwin bash prompt
    Run
    `npm install -g pnpm`             [From <https://pnpm.io/installation> ]

    Let it finish.

    Then run the get initializer for the svelte engine
    `npm init vite`                         [From <https://github.com/sveltejs/template> ]

    Give the project a name. [the default is fine.]

    Select the svelte-ts optional    [ use arrow keys ]

    Let it complete and leave this window open in the background. We will use bash again in step 4.

## Step 3 - install and run the svelte engine	CMD / PSHELL
    Start cmd prompt or powershell 
    Navigate to the new vite-project folder
    [If you installed cygwin to default location of `c:\cygwin64`, the vite-project will be found in 
    `C:\cygwin64\home\yourprofile\vite-project`]

    `cd vite-project`

    `npm install`
    `npm run dev`

    This will install the dev tools 'sed' etc

    Leave the cmd window open - this is your svelte compiler running in the background

## Step 4 - make your edits to the svelte typescript. 
### recommended to use the VS Code svelte addin [https://marketplace.visualstudio.com/items?itemName=svelte.svelte-vscode]

    In Windows Explorer, place a COPY of ps-hud inside your cygwin homedrive holder, we will edit this 
    one and once we successfully compile, we can copy the changed files [the /html/ directory contents ] 
    back over to your production [live] server ps-hud folder.

    in your favorite editor (Visual Studio Code obv)
    Edit whatever you need to change in the `C:\cygwin64\home\yourprofile\ps-hud\svelte-source\src` 
    directory. remember to save your changes. when you are ready continue to step 5.

## Step 5 - compiling your svelte typescript package!

    Switch over to the bash prompt

    navigate to the svelte-source folder        (not /src)
    cd /cygdrive/driveletter/pathto/ps-hud/svelte-source

    Run the _alternate_ nodejs pnpm package manager (pnpm) with the svelte plugin 
    `pnpm run build`

    this now compiles. and once complete, the changed files will be listed in the bash summary.
    Now we can copy the changed files [the /html/ directory contents ] back over to your production [live] server ps-hud folder.

## Step 6. - testing

    ensure your ps-hud and log onto your server. i didnt need to clear my cache but i did need to relog.



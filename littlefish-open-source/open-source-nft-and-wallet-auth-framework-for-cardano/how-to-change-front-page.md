# How to change front page?

### Opening the Project in Visual Studio Code

Now that you have the project cloned to your local machine, you need to open it in Visual Studio Code (VSCode). VSCode is a powerful editor that provides robust support for TypeScript and React development.

#### Opening the Project

1. Launch Visual Studio Code.
2. Navigate to `File > Open Folder...` from the top menu.
3. Browse to the location where you cloned the repository, select the `boilerplate-e` folder (or whatever you named the folder), and click `Open`. This action will load your project into VSCode.

#### Editing the Hero Section

The hero section of your application is a key part of your user interface, designed to capture users' attention and convey the main message of your application quickly. Here’s how you can locate and modify this section in the file located at `/components/landing/hero-section.tsx`:

**Locate the Hero Section File**

1. In the VSCode sidebar, navigate to the `components` folder.
2. Drill down to the `landing` sub-folder.
3. Open the file named `hero-section.tsx`.

**Modify the Hero Section**

Once you have the `hero-section.tsx` file open, you can make changes to the text and style as needed:

*   **Change the Headline Text**: Find the `<h1>` tag to modify the main headline of the hero section.

    ```typescript
    <h1 className="bg-gradient-to-br from-white to-white/40 bg-clip-text py-6 text-5xl font-medium leading-none tracking-tighter text-transparent sm:text-4xl md:text-5xl lg:text-6xl">
      Your New Headline Text Here
    </h1>
    ```

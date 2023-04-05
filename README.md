# Kasm Workspaces Registry

This is a repository of the workspaces supported by Kasm. The workspaces list is automatically generated and can be used when creating new workspaces or using the 1 click installer

## Create your own workspace registry

We have tried to make it as simple as possible for people to create their own registries that work with Kasm, the easiest way to do that is to follow these steps:

---

### 1. Click on "Use this template", select Create a new repository. 

![image](https://user-images.githubusercontent.com/5698566/230080486-08d4c678-a0bd-4f30-863b-5f7f0bb9182f.png)


> **Note**
> If you set the **Repository name** to `kasm-registry` you wont have to make any changes to the `baseUrl` later, unless you want to use a (sub)domain.

Select a **Repository name**, this name will also be used later for the `baseUrl`, tick the **Include all branches** checkbox, then click on the **Create repository from template** button.

![use-template](https://user-images.githubusercontent.com/5698566/230080115-e81a5663-5752-44fc-94a5-ea7721e5745b.gif)

---

### 2. Click on the actions tab and check whether workflows need enabling, if they do, enable them, otherwise you should be good to go.

![image](https://user-images.githubusercontent.com/5698566/230056251-09d722e8-41d8-4adf-b166-b623624e19ec.png)

---

### 3. Go back to the `Code` tab, then click the `site` folder, click `next.config.js`, then click the edit button. Fill in the `env` section with the relevant information and change the basePath if needed (details below).

![edit-conf](https://user-images.githubusercontent.com/5698566/230075839-ec698589-1276-4163-bd5e-34642a108e7f.gif)

![image](https://user-images.githubusercontent.com/5698566/230057592-a6fbde4d-2bda-44ca-b77d-62c58ed97cc4.png)

| Property  | Description |
| --------- | ----------- |
| env.name  | The name you want to display for your registry. |
| env.description  | A short description to display when a store's information button is pressed. |
| env.icon  | The image to display for your registry. You can upload an image to `/site/public/` and reference that by https://domain.com/1.0/image.png or if you aren't using a {sub}domain by referencing it from https://username.github.io/repositoryname/1.0/image.png where image.png is the name of the image you uploaded. Alternatively just put the url of an image available on the web. |
| env.listUrl  | The link to the root of your site. For example https://username.github.io/repositoryname/ it should always include a trailing slash. |
| env.contactUrl  | A link users can use to contact you on, such as your github issues page (right click the **Issues** tab in the top menu - next to the **Code** tab - and select `copy link address` and paste that in). |
| basePath  | If you are using a domain or a subdomain, your basePath will just be `basePath: '/1.0',`, otherwise change the value to include what you chose for the repository name in step 2 `basePath: '/repositoryname/1.0',`. **The `1.0` will be replaced with the branch name automatically, so you should always keep it as 1.0.** |

---

### 4. Upload your workspaces to the `/workspaces` folder and delete the default workspace if you want

> **Note**
> If you just want to get something working, you can skip this step as a template workspace is included.

When you are ready to start adding your own workspaces check out https://kasmweb.com/docs/latest/guide/workspace_registry.html#create-your-own-workspace-registry for more details

![image](https://user-images.githubusercontent.com/5698566/230060229-d4e0c0d9-eb94-437d-abda-fa9b751e0cce.png)

![image](https://user-images.githubusercontent.com/5698566/230060562-72a7f444-2d9e-4188-80dd-4a88af9e9e3e.png)

---

### 5. Go to the `Settings` tab, then the `Pages` left menu item and make sure the dropdown underneath **Branch** is set to gh-pages, if not, set it and click Save.

> **Note**
> If you ticked the "Include all branches" checkbox in step 1, this should all be set up for you, if not, just follow the instructions below

![gh-pages](https://user-images.githubusercontent.com/5698566/230077012-938704c4-af44-4d3c-8023-0732c34a78bc.gif)

If you see a message like the following:

![image](https://user-images.githubusercontent.com/5698566/230061310-f2883e2f-7279-45c9-8cc5-de56dcc6e03f.png)

Then congratulations everything is done! Just click the **Visit Site** button.

---

If you don't see that button yet, then not to worry, it's likely that you are just too quick (also if you do see the button but it doesn't reflect the changes you made, this next bit is relevant as well)

Check on the CI progress in the **Actions** tab, 

![image](https://user-images.githubusercontent.com/5698566/230061667-63829dbd-46f2-4f7b-96c4-0cab8279e8a6.png)

Once `Page build and deployment` is finished go back to Settings / Pages and you should have a live site. Click on the Visit Site button.

---

**You should now have a working site which includes any workspaces you added or the default if you haven't made any changes yet**

![image](https://user-images.githubusercontent.com/5698566/230064289-9e8967a1-4ff9-43f3-8495-f4170c23a80f.png)

---

[![](https://cdn.loom.com/sessions/thumbnails/256fac3d2bbb422b8e779ac1c8244d33-00001.gif)](https://www.loom.com/share/256fac3d2bbb422b8e779ac1c8244d33 "")

## New schema version

If a new schema version comes out, this is what you will need to do.

1. Create a new branch with the schema version as the branch name (for example, 1.1)
1. That should be all you need to do.

More details about the schema can be found at https://kasmweb.com/docs/latest/guide/workspace_registry.html#schema

## Discovery

The tag below will hopefully make it easier for people to find your Workspace Registry by clicking on [this github search link](https://github.com/search?q=in%3Areadme+sort%3Aupdated+-user%3Akasmtech+%22KASM-REGISTRY-DISCOVERY-IDENTIFIER%22&type=repositories). If you want to make it harder to find your repository for some reason, just remove this section.

KASM-REGISTRY-DISCOVERY-IDENTIFIER

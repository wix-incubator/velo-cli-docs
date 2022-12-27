# `Velo CLI` - Documentation Source Files
This repository includes all the documentation files for the `Velo CLI`. The following documentation is visible through the [`Velo CLI` Documentation](LinkToViewer).

### Organize the Wix Docs Menu - categories, order, names, etc

1. Go to the [`Veo CLI` Menu Editor](LinkToViewer/menu-editor).
2. Make you changes & export once you finish.
3. Send us the export config file to [#wix-docs](https://app.slack.com/client/T02T01M9Y/CC1U35ZRA) channel

### Adding docs to the "API Reference" section in Wix Docs:

1. Follow our instructions in our [Docs Generation Guide](https://bo.wix.com/wix-docs/rnd/wix-docs/wix-docs/how-to-generate-documentation).
2. Make sure your repo have a `documetation.yaml` file according to our [Documentation.yaml Guide](https://bo.wix.com/wix-docs/rnd/wix-docs/wix-docs/documentation-yaml-guide).

### Adding docs to the "Articles" section in Wix Docs:

1. Write your guide in markdown syntax. [Learn more about Markdown](https://bo.wix.com/wix-docs/rnd/wix-docs/wix-docs/markdown-cheat-sheet)
2. Images - in case your markdown file is including images, you have two options to add them:
	 1. Full link to the image - in case the images are not stored in Github.
	 2. Relative link to the image - in case you want to use relative link to the image in this repo, you must locate the image in the `/media` folder.
3. Upload your `.md` file/s to the `/guides` folder inside this repo. You can insert it to one of the existing folders inside the `/guides` folder or create your own.
3. Go to the Wix Docs menu-config file [`/guides/guides.json`](./guides/guides.json)
4. Add your file information to `articles` in one of the existing categories (Development, Production Preparations, etc). If you can't find a relevant category, you may add one.
	Add the following fields:
	1. `name` - the name you would like to show in the Wix Docs left menu.
	2. `url` - a relative link to your file.
	3. `isMdFile` - use `true` when the `url` is pointing for a markdown file.
	4. `isExternalLink` - use `true` when the `url` is pointing to an external link (will open in new tab).
	5. `group` - you can put your guide under sub category by adding path of folders.


	for example:
	```JSON
		{
		  "items": [
		    {
		      "title": "Getting Started",
		      "articles": [
				{
				  "name": "Overview",
				  "url": "./Overview.md",
				  "isMdFile": true
				},
				{
				  "name": "Authentication",
				  "url": "./Authentication.md",
				  "group":"First Level",
				  "isMdFile": true
				},
				{
				  "name": "Permissions",
				  "url": "./Permissions.md",
				  "group":"First Level.Second Level",
				  "isMdFile": true
				}
		      ]
		    }
		  ]
		}
	```

	would look like:

	![image](https://user-images.githubusercontent.com/53995839/109794065-249c0580-7c1e-11eb-859b-eedbe3e96bce.png)



5. Commit & Push
6. Visit [`Velo CLI` Documentation](LinkToViewer) to find your article.
	> **Be patient:** It takes 20~30 minutes for the article to get online

# Post Reader

Post Reader is a Github repository that can be forked to deploy a hyperlink aggregating website, for your specific topic, to Github Pages. Anyone with a GitHub account that creates a Pull Request can contribute content to the website.

The source repository (this one), includes a few example hyperlinks related to [Angular](https://angular.dev/), the framework this repository was built with. The examples can be viewed at this repository's [Github Page](https://thebeard.github.io/post-reader/).

## How to Contribute an Article or Post (Hyperlink)

_For points (7) to (10) see the example template below list this._

1. <a href="https://github.com/signup" target="_blank">Create a Github Account</a> if you don't have one yet
1. Return to this page
1. Go to the <a href="https://github.com/thebeard/post-reader/blob/main/src/content/template" target="_blank">New Hyperlink Template Page</a>
1. Copy the template using the **Copy raw file** button located in the File Preview toolbar 
1. Click the `+` (**Add file**) button in the **Files** sidebar on the left
1. Paste the template content
1. Optionally, insert a `Title` tag. (Will be inferred from original content if ommitted)
1. Insert one or more `Tags` tags, to ensure your content is categorised accordingly.
1. Most importantly, insert the hyperlink into the `Link` tag using the format in the example.
1. Below the meta section (starting and ending with `---`) you are able to add a summary for your hyperlink using **Markdown** syntax. If not submitted, a summary will be automatically generated.
1. Use the **Commit** button to progress to the next step.
1. If prompted, optionally add a commit message.
1. From the two options presented, to commit directly or to create a Pull Request, select the **Pull Request** option.
1. Finally confirm your commit to submit your hyperlink post.
1. A member of the approval committee will now receive your submission and approve it for display on the website.

```markdown
---
[//]:# (Title: My title)
[//]:# (Tags: #my, #tags)
[//]:# (Link: https://my-example.com)
---

# My Example header

My example summary goes here. Lorem Ipsum dolor sit amet ...
```
_Example template_

## How to use this Github Repository to create your own Hyperlink Aggregator site

### Select your deployment method

#### Github Pages

By default, for any commits made to the `main` branch of your new repository, a deployment to Github Pages will triggered using Github Workflows.

Configure your Custom Domain to allow your website to display on your pre-registered domain of choice.

To disable Github Pages deployments, delete the file `.github/workflows/npm-publish-github-packages.yml`

#### Via Terraform

A sample set of terraform scripts can be found at the `/terraform` location. The sample terraform scripts are configured to deploy to AWS. Update and use as per your cloud provider and CI/CD framework accordingly.

See other section below as well.

#### Other

When setting up your own build and continuous integration pipelines, please note this application uses a custom npm command. Use `npm run build-with-content` to build your application.


### Fork the application

1. Fork the project to a new public repository
1. Ensure necessary Pull Request and Commit permissions are set up to allow for post approvals by the administrator and/or moderators
1. Change the title at the top of this markdown file (`# Post Reader`)
1. Change the two intro paragraphs at the top of this markdown file, to reflect the topic and purpose of your own website.
1. In the file located at `src/app/app.config.ts` change the site title on **line 24**
1. Remove the example posts in the `src/content` folder
1. Submit and commit your first post

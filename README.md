## YouTube Upload Client using Dropzone.js and Google API v3 (Javascript)

You can use the [editor on GitHub](https://github.com/paulzmuda/youtube-client/edit/master/README.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### Usage

### Examples

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Browser Support

- Chrome 7+
- Firefox 4+
- IE 10+
- Opera 12+ (Version 12 for MacOS is disabled because their API is buddy)
- Safari 6+

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/paulzmuda/youtube-client/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

## Why use this take on the YouTube API?

The most common uses of the YouTube API are with server-side languages such as PHP.  This poses a problem when trying to upload large video files since your web server is forced to act as the middleman between the end-user and YouTube.  Uploads buffer these video files into your server's memory before passing them along to YouTube.  Using the Javascript API eliminates this process, no longer taxing the resources of your web server and clears a bottleneck.  The reason I originally had to create this was because I had to upload large video files to a high traffic website. Our server only had 1 gigabyte of memory which is what most low-cost hosts provide, and trying to upload videos larger than 300mb was causing the server to overload it's memory resources and crash.  This would be a great tool for files of any size not only because of the increased upload speeds, but also because of it's simplicity of implementation into any existing system.  If you're using a pay-as-you-go service such as Amazon Web Services, this saves you money.

High traffic sites that need to upload large video files to YouTube

You run the risk of crashing (or dramatically slowing down) your web server if you try uploading a large video file on a basic instance (such as EC2 Micro.). If you have a high traffic website and large video files, you would find more efficiency outsourcing the heavy lifting to the client.  The only plugins I've found to date, are using the Google PHP API to upload videos, but before the video is uploaded to YouTube, it's buffered into your web server's memory.  If you're trying to upload a 500+ megabyte file, on a server with only 1gb of memory, you're going to crash your website.  For this reason, using the JavaScript API solves this problem.


### MIT License

See LICENSE file

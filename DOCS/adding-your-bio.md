# How do I add my bio to the site?

Adding your bio can be summarized in three easy steps:

1. Finding a square (yes it must be square), good resolution profile picture
2. Adding your metadata to a list
3. Writing a biography page


## 1. Your profile picture
The profile pictures are stored under [../images/bio](../images/bio). The format is not important, but please use the naming standard convention firstnamelastname.jpg (or .png, etc.). You should find a picture that you like, make sure it is cropped to be square (non square images look really weird) and then add it to this folder.

## 2. Adding your metadata
Did you see that each bio page has a link to Twitter, or a website, or other? We do this by way of Jekyll's data format, which is called `.yml`. The lab members are generated from the data file [../_data/authors.yml](../_data/authors.yml). Here is what an author entry looks like:

      Curt Langlotz:
        name: "Curt Langlotz"
        uri: "https://curtlanglotz.com/"
        email: "langlotz@stanford.edu"
        bio: "Professor of Radiology and Biomedical Informatics at Stanford University"
        role: "Lab Director"
        avatar: "bio/curtlanglotz.jpg"
        twitter: "curtlanglotz"
        github: langlotz

Notice the very top line, in this example "Curt Langlotz" - this is the identifier for the data object that will be referenced in your bio to obtain the right data for the page. This should be your first and last name, first letters capitalized, sans any special titles. You can copy paste someone else's entry and add it to the bottom of the file to use as a template! You can leave out any fields that you like, however please don't leave out your name, role, or avatar. Here is some more information on the different fields:


- name: is self explanatory.
- uri: should refer to any personal site (or something like Google+, LinkedIn) that you want under the "website" field. This is optional.
- email: is your email address, only include if you want it to appear on your bio. This is recommended, so interested people can contact you!
- bio: This is the little blurb of text that appears under your picture on the biography page itself. Please include this.
- role: This is the text that appears under your picture on the lab roster page, and should be your title in context of the lab.
- avatar: You will just need to change the name of the image. This path is relative to the "images" folder.
- twitter: Your twitter handle, if you have one!
- github: Your github user name! Share your code, yo.

Other tags that you can add include:
- location
- bitbucket
- codepen  
- dribbble 
- flickr   
- facebook
- foursquare
- github
- google_plus
- keybase  
- instagram
- lastfm   
- linkedin 
- pinterest
- soundcloud
- stackoverflow  (eg "123456/username" - the last part of your profile url, e.g. http://stackoverflow.com/users/123456/username)
- steam    
- tumblr   
- vine     
- weibo    
- xing     
- youtube  

Go to town!

## 3. Add Your biography
The last thing you need to do is add your biograph page. Each person has a biography page, which is a markdown file stored in the [../_members](../_members) folder. The easiest thing to do is copy someone else's bio, and then fill it in with your information. The only requirement is that you maintain the same structured header, but fill it with your own information. For example:

      ---
      layout: single
      title: "Vanessa Sochat"
      author: Vanessa Sochat
      header:
        teaser: "bio/vanessasochat.jpg"
      excerpt: "Systems Engineer for Research Computing and Stanford Medicine" 
      ---

You don't need to change `layout`. The `title` should be what you want for the header of your page, e.g., this is where you put all your MDs and PhDs or other. The `author` tag is very important - this should match exactly to the author name you added to the authors.yml file. the `teaser` is going to add your image to the roster page, and it should link to the same one. Finally, the `excerpt` is the little bit of text that (again) describes your full title.

Once you have this header done, you can go to down with the content! Both markdown and html are supported. If you need help with something, ping @vsoch.

Great job! That's it. You next should preview the page, and push to Github. For instructions on these steps, see the [testing-deploying-site.md](testing-deploying-site.md) notebook.

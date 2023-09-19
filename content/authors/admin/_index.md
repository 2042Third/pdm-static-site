---
# Display name
title: Yi Yang 

# Is this the primary user of the site?
superuser: true

# Role/position
role: ''

# Status emoji
status:
  icon: 

# Organizations/Affiliations
#organizations:
#- name: 腾讯
#  url: ""

# Short bio (displayed in user profile at end of posts)
bio: My research interests include end-to-end encrypted systems, encryption, and information security.

#interests:
#- Artificial Intelligence
#- Computational Linguistics
#- Information Retrieval

#education:
#  courses:
#  - course: PhD in Artificial Intelligence
#    institution: Stanford University
#    year: 2012
#  - course: MEng in Artificial Intelligence
#    institution: Massachusetts Institute of Technology
#    year: 2009
#  - course: BSc in Artificial Intelligence
#    institution: Massachusetts Institute of Technology
#    year: 2008

# Social/Academic Networking
# For available icons, see: https://wowchemy.com/docs/getting-started/page-builder/#icons
#   For an email link, use "fas" icon pack, "envelope" icon, and a link in the
#   form "mailto:your-email@example.com" or "#contact" for contact widget.
social:
  - icon: envelope
    icon_pack: fas
    link: 'about/#contact' # For a direct email link, use "mailto:test@example.org".
#  - icon: twitter
#    icon_pack: fab
#    link: https://twitter.com/wowchemy
#  - icon: instagram
#    icon_pack: fab
#    link: https://instagram.com/geocushen
    
# Uncomment below for Github link
  - icon: github
    icon_pack: fab
    link: https://github.com/2042third

# Link to a PDF of your resume/CV from the About widget.
# To enable, copy your resume/CV to `static/files/cv.pdf` and uncomment the lines below.
# - icon: cv
#   icon_pack: ai
#   link: files/cv.pdf

# Enter email to display Gravatar (if Gravatar enabled in Config)
email: "yiyang5@andrew.cmu.edu"
---

Yi Yang is a graduate student at Carnegie Mellon University studying Information Security. He likes to write code and build things. He is currently working on a personal data manager (PDM) projects for fun. He is also looking for internship opportunities in the summer of 2024. 

 ### Some status on the projects (updated on Sep 19, 2023):
- PDM Desktop App (This is what I am actively working on for the past two months or so):
  - Encryption is finished (parallelized instead of single threaded as in the browser WebAssembly version)
  - Notes update is *not* finished
    - This is because I am working on the binary file encryption features first
    - Should be done relatively soon...
    - Only mentally blocked on implementing the basic network calls to the server... (literally just a few lines of code...)
    - but it currently can retrieve, decrypt, and show notes from the server
  - Chat not finished
  - Have a binary file encryption "plugin" for folders and files that can encrypt files in cloud drive folders
    - This is very cool because it can encrypt using pdm-crypt-module and the servers only need to keep the relative locations of the files and folders in a particular cloud drive folder.
    - Should have a working version of this in a week or so
  - Local storage is finished (the most robust local storage out of all the others)
    - Using virtual file system in the memory as SQLite database, and only encrypted data is touching the hard drive
 - PDM Mobile App: 0.1.0-alpha
   - Encryption is finished
   - Notes update is finished
   - Local storage is partially finished
     - Local storage is using Redux persist
     - Encrypted using pdm-crypt-module
     - Next step is to cache the encrypted data in local storage when internet is not avaliable
   - Chat not finished
 - PDM Web App: 0.1.0-alpha
   - Encryption is finished
   - Notes update is finished
   - Chat not finished (should be done earlier than mobile app)
   - Local storage partially finished~~~~
     - Encrypted using pdm-crypt-module
     - Local storage is using IndexedDB in browsers (all browsers support it, but many users just turn off the feature for security reasons)
  
    


{{< icon name="download" pack="fas" >}} {{< staticref "uploads/resume.pdf" "newtab" >}}Download{{< /staticref >}} my resumé as a PDF.


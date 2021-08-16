# ![favicon32px](https://user-images.githubusercontent.com/72383148/123824522-be996380-d91b-11eb-8f09-4ce388807675.png) How to Top & Side Naviagtion  Template added on Geppetto Application
### Let's get Start ![computer-display](https://user-images.githubusercontent.com/72383148/123821588-29956b00-d919-11eb-91b3-74259f32d209.png)
 To layout the procedure to add new template to geppetto application. Geppetto can generate different types of UI designs by user friendly designed template web pges and template screens.
## Prerequisites :
We need geppetto UI application and some node application server for adding the new template. List of applications needed are listed below:

 - Use **Visual Studio Code** Tools and Click the Extensions icon ![extensions-view-icon](https://user-images.githubusercontent.com/72383148/123835413-1d63da80-d926-11eb-9734-e22da720ae6b.png)
and install Live-server or (https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer)
 - **Base64 Image** to Convert the Encoder this Link - https://elmah.io/tools/base64-image-encoder/
 - Top Navigation template - Zip File 
 - Local machine Geppetto application deploy ***(or)*** live geppetto application dev - https://dev.app.geppettosoftware.com/ create an account
 - NOSQLbooster Application - https://nosqlbooster.com/downloads   ![download](https://img.icons8.com/office/18/000000/download--v2.png)
 - Geppetto Backend Folder with path 
	 - Template Manager - ***/geppettotest/application/services/templatemanager*** 
	 - Screen Manager - ***/geppettotest/application/services/screenmanager*** 
	 - Angular Template managerv10 - ***/geppettotest/generator/services/Angular-Template-managerV10***
 - Geppetto Frontend UI Folder 
	 - Template - ***/geppettotest/application/clients/desktop/src/assets/templates***

## Procedures:
-   UI/UX team will give the template file for add new template
-   Get the html file(index.html) from given template file
-   Important* things in below the tags should be here html template both Top and Side navigation
-   Insert the copied code from template html file to screen designer and Save the screen
-   To create a new object in template array in template manager.
-   Delete the existing geppetto templates collection and re run the template manager service.
- Template add generation side to create services:
### 1) UI/UX team will give the template file for add new template

 - UI/UX team will give the template zip file. You should extract 
	![extract template](https://user-images.githubusercontent.com/72383148/123789744-1ffd0a80-d8fb-11eb-8e4b-b939fe4bb995.jpg)
 - Choose the template folder and Now you can get the files for add template like this - (second Image)
 ![templatepath](https://user-images.githubusercontent.com/72383148/123790113-97329e80-d8fb-11eb-8b7b-98f03cd61690.jpg)
	![folder](https://user-images.githubusercontent.com/72383148/123790129-9bf75280-d8fb-11eb-935b-8693421a6832.jpg)
	
### 2) Get the html file(index.html) from given template file
 - Copy the code from designed template html file this code. Also you should add the css file under the style tag.
 `<style> add a css style </style>`
 `</body>`
 `</html>`
 -  If  images are available in extracted file please  kept in the angular template managerv10.

### 3) Important* things in below the tags should be here html template both Top and Side navigation
			

 - **Header tag***
 - **Nav tag***
 - **Footer***
 
 - [ ]  First, change template align and css, html format to check and then add a **nav** tag

  <nav id="template-i090p" class="navbar navbar-inverse">
        <div id="template-iyoc4" class="navbar-header">
            <span onclick="openNav()" id="in2oj" class="">
                <i class="fa fa-bars" aria-hidden="true"></i></span>
            
    <nav id="template-i090p" class="navbar navbar-inverse">
            <div id="template-iyoc4" class="navbar-header">
            <span onclick="openNav()" id="in2oj" class="">
                <i class="fa fa-bars" aria-hidden="true"></i></span>
            <button type="button" data-toggle="collapse" data-target="#myNavbar" id="template-ioico"
            
                class="navbar-toggle">
                <span id="template-iy169" class="icon-bar">
                </span>
                <span id="template-ivo7o" class="icon-bar">
                </span>
                <span id="template-ihry1" class="icon-bar">
                </span>
            </button>
        </div>
        <div id="mySidenav" class="sidenav">
            <a [routerLink]="['javascript:void(0)']" onclick="closeNav()" id="template-if7ki" class="closebtn">
                <i class="fa fa-close size-30" aria-hidden="true"></i></a>
            <div id="MainMenu" class="">
            
            </div>
        </div>
    </nav>
  

 - [ ] To HTML template test on **live-server** everything is fine, **Let's start add a template** ![display](https://img.icons8.com/ios-glyphs/60/000000/technology-items.png)

### 4) Insert the copied code from template html file to screen designer and Save the screen
 - Open Geppetto application in local or live 
 - Click, create the new project and Open a project app
 	 ![createproject](https://user-images.githubusercontent.com/72383148/123806040-32337480-d90c-11eb-8e5f-1c20b259885c.jpg)
	 - Click, the add feature and create one feature
	 - After created you have to click the view button in your feature
	 - Now click the **Screen** and click **the Add screen** 
	  - Click the Last download icon which is **import your template** 
	  - Now place the whatever copied html code from the template html file
	  - Click the **import** button then you can see template image in screen
		 designer and save the template screen.
![screencast-gif](https://user-images.githubusercontent.com/72383148/123812943-1fbc3980-d912-11eb-9828-f0701bd81419.gif)
- MongoDB connection establish
	-Click the connect button
	-Click edit tab in this move to authentication tab 
-After set username as admin and password as password
![Screenshot from 2021-08-16 12-34-16](https://user-images.githubusercontent.com/80459304/129524444-78c1f742-f2a8-43c4-afcb-efdb60d6a576.png)
- It will store into the mongo db with screens collection. we can get the template data from here.
![Screenshot from 2021-05-11 19-45-05](https://user-images.githubusercontent.com/71403617/117830710-84073900-b291-11eb-86f3-115d93a56d64.png)

### 5) To create a new object in template array in template manager

 -  Go to this file path : ***/geppettotest/application/services/templatemanager/src/assets/geppettoTemplate.ts***
- Next we are going to create a new object for adding new template array **geppettoTemplate.ts**  as same as from existing geppetto template, You  should create a new object with following image keys and values
	
	- **Template Syntax :**
	
			{
			    "gjs-assets" : ["[]"],
			    "gjs-styles" : [],
			    "gjs-components" : [],
			    "gjs-html" : "",
				  "gjs-css" : "",
				  "stylesheets" : [
					      "https://stackpath.bootstrapcdn.com/bootstrap/4.3.1/css/bootstrap.min.css",
					      "https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/css/bootstrap.min.css",
					      "https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.css"
				   ],
				  "scripts" : [
					      "https://ajax.googleapis.com/ajax/libs/jquery/3.2.1/jquery.min.js",
					      "https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/js/bootstrap.min.js"
			     ],
				   "css-guidelines" : [ 
					   { tagName: 'form', className: 'form'}, 
					   { tagName: 'input', className: 'form-control' }, 
					   { tagName: 'select', className: 'form-control' }, 
					   { tagName: 'textarea', className: 'form-control' }, 
					   { tagName: 'button', className: 'btn btn-primary' }
				    ],
				    "name": "TEMPLATE NAME UPPERCASE",
				    "flag": "active",
				    "navigation-type": "side",
				    "template_image" : [{
						    "imagename" : "templatename_template",
						    "image" : ""
					 }]
			  }

		![Screenshot from 2021-05-11 19-55-40](https://user-images.githubusercontent.com/71403617/117832267-f7f61100-b292-11eb-983a-57d80af5c62d.png)
- we need to place the codes in the **geppettoTemplate.ts** under the **template manager**  from saved screen data from mongo db such as **gjs-html, gjs-css, gjs-assets, gjs-style, stylesheets, scripts, css-guidelines**

	![screensDB](https://user-images.githubusercontent.com/61690990/109118590-86b1c200-7769-11eb-8a32-578545aea36a.png)

**"name" :** You should mention the Template name **"your template name"**
**"navigation-type" :** you should mention the type as **top** or **side**
**"flag"**: You should mention the flag is **inactive** or **active**
 
### Note: If flag is active you can view the template otherwise doesn't show in geppetto app
**"imagename" :** You should mention the image name "related to image"
**"image" :** You should encrypt the your template image as **base64** (you can use online editor LINK attach prerequisites) like previous image and paste it

![Screenshot from 2021-05-11 20-24-17](https://user-images.githubusercontent.com/71403617/117837234-e9115d80-b296-11eb-9d02-c90427b79e69.png)

- After add all the keys and values you can view the code like below image        
![geppettotemplates](https://user-images.githubusercontent.com/61690990/109117922-a4caf280-7768-11eb-8b9d-32a30f28ff76.png)

### 6) Delete the existing geppetto templates collection and re run the template manager service.
Now we have new template object in template manager so next need to delete the geppetto templates table for existing templates 
 It will automatically update with new template details in DB.
 **Before Delete the geppetto_template collection**
 ![Screenshot from 2021-05-11 20-38-00](https://user-images.githubusercontent.com/71403617/117839606-00e9e100-b299-11eb-89b9-a2991d4c9087.png)
 
- After should remove the docker container and docker images of templatemanager microservice only and return again
				

			    Docker Command :
						    - Docker Remove Container - docker rm -f container_name
						    - Docker Remove Image - docker rmi image_name
				Both Command Use : docker rm -f container_name, ..... && image - docker rmi image_name, ......

 
 ![Screenshot from 2021-05-11 21-26-04](https://user-images.githubusercontent.com/71403617/117846984-912b2480-b29f-11eb-8a85-4765401b0cb8.png)

    ``Note : make sure template object flag is active``

![flag-name](https://user-images.githubusercontent.com/61690990/109133993-92a67f80-777b-11eb-9f84-303eef7b623b.png)

### 7) Template add generation side to create services:
- This navigation methods are present in the following file path : ***/geppettotest/generator/services/Angular-Template-managerV10/src/services/angularTemplateService.ts***
- Add a Condition to generate Top or Side navigation 
	
	- Top Navigation - **this.generateTopNavTemplate()** method.
	- Side Navigation - **this.generateSideNavTemplate()** method.
	![templatemethod](https://user-images.githubusercontent.com/72383148/123833220-c0ffbb80-d923-11eb-9174-4141903248af.jpg)

- You should implement the navigation method like as below image.

![Screenshot from 2021-05-11 21-34-02](https://user-images.githubusercontent.com/71403617/117848177-a94f7380-b2a0-11eb-9cc9-e8bfa6ab58ef.png)

If Navigation type is **Side**, it will go to **sideNavigation function**. Otherwise it will go to **topNavigation function.
-After implementing the navigation method we go to our Geppetto builder in our local .
	-In that click the code generation.
	-After generate the code there is a new project in our repo ..
	-Clone the project .
	-npm i 
	-Run ng serve --port 0000
# Conclusion:
Finally we have added the new template to geppetto application  
![Screenshot from 2021-05-11 21-39-21](https://user-images.githubusercontent.com/71403617/117848960-76f24600-b2a1-11eb-81a9-e3d1016bf93f.png)
After click the **Select Template button** you can view your added template
![Screenshot from 2021-05-11 21-39-45](https://user-images.githubusercNow we copy the code from repository to our local
203
                Now we copy the code from repository to our local
203
                ontent.com/71403617/117849518-0566c780-b2a2-11eb-94d9-e745d8b137d4.png)

Note: then you must add the flag is active in template object other wise not showed in the UI but it store into the Data Base.

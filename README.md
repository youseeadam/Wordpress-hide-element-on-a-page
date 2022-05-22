# How to hide an element on a WordPress Page.
Many times I want to hide just a single element on a page in WordPress, there are plugins for this, but you can do it pretty easy on your own.  It's important to remember that it just hides the element, it will still redner

It really isn't that tricky with a few basic key points.

How to hide an element on a page in WordPress
It really isn't that tricky.
1.	Open a web browser and go the page you want to edit
2.	Right click on the element and choose inspect (or press F12 to open the element inspector)
 ![image](https://user-images.githubusercontent.com/19500079/169708656-cca7f4bb-d596-421c-97b2-04f1e6d533cb.png?width=100)

3.	That will highlite that specific element, but not necessarily the entire elment containing the block
 ![image](https://user-images.githubusercontent.com/19500079/169708688-ae0fd864-d573-4756-ab24-1f86502a143b.png)<p>
<img width="918" alt="image" src="https://user-images.githubusercontent.com/19500079/169708713-298ce866-128d-4945-9503-ac52530f96ae.png">
 
4.	So as you scroll your mouse over other elements, you will see different parts highlighting.  For example, I want to hide the entire header on a single page. Here I highlighted the site title, but not all of what I want to hide. I still want to hide the tag line
 
 
5.	So I will continue to move my mouse up the chain until I get everything I wanted highlighted
6.	Site Branding is the one I want to hide. Notice how I see both the element and the border
 
 ![image](https://user-images.githubusercontent.com/19500079/169708782-08f8b290-6f97-4d83-b612-c1c942c5d532.png)
![image](https://user-images.githubusercontent.com/19500079/169708801-593999fc-79e9-42c9-8cc9-c9416a7e557a.png)

7.	So let's make sure that it is indeed the correct thing.
8.	With the element highlighted, I am going to override the style within the element style, just type after that curly bracket display:none
 ![image](https://user-images.githubusercontent.com/19500079/169708820-e455f29c-4af1-42f3-a406-f9c0179b02e3.png)

9.	Now that I know I have the right element, I need to find the correct CSS for it, this is just by trial until you find the right one. So I will delete the display : none I just typed and will go through the styles explorer until I found the right one by entering in display:none.  In time you will figure out the pattern.
10.	Ends up being this is the one I want.  I picked this one to explain something as well
  ![image](https://user-images.githubusercontent.com/19500079/169708855-ba6d04a2-c705-4c9d-95a8-6bc01a977091.png)

  Notice how part of the css is gray, you don't want to override the gray, that may control something more important that will break the site more.
  
11.	What you need is everything after the last grayed out comma, in this case it is .site-branding
12.	So now we have the element we need to hide.
13.	To get the page scroll back to the top of the explorer. There is the body tag.  From that you need the page ID
 ![image](https://user-images.githubusercontent.com/19500079/169708888-f35bb76e-3ab8-4cbe-8029-7d23ea64516c.png)

14.	So now you need to set display:none on page page-id-2351
15.	In most WordPress themes there is an additional css
16.	Add the CSS entry
  
  ![image](https://user-images.githubusercontent.com/19500079/169708898-fab68493-e230-4713-bdc0-5417f070e795.png)

17.	Publish the changes, and you are set.
Now it's important to know that this just HIDES the elements. If you go look into the element explorer after you make the change, you will see it is still there, just not rendered. But now, you know how to find an element on a page and edit it.

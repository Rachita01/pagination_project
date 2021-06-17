**Prerequisite :-** 

   1.React app created using command - _npx create-react-app projectname_

2. Install axios using command - _npm i axios_

3. Copy the path of posts api from _jsonplaceholder_

4. Include bootstrap link in index.html from _getbootstrap.com_

**Flow of implementation of pagination:-**

Included hooks in app.js - useState and useEffect(helps to mimic some of lifecycle components used in class component)

Defined states for posts(set as empty initially), loading(set as false initially), postsPerPage(set as 10 initially) and currentPage(set as 1 initially) using useState

Used async-await function along with axios to fetch the posts data from api(axios.get('url') in useEffect Hook.

Created a folder of components and in that created a file Posts.js for listing posts to app and imported Posts.js file in App.js and passed in props - posts and loading in calling Posts component.

Three things that needs to be defined in App.js are - 

   * indexOfLastPost = currentPage * postsPerPage

   * indexOfFirstPost = indexOfLastPost - postsPerPage

   * currentposts = posts.slice(inbdexOfFirstPost,indexOfLastPost)

Created new file in components folder - Pagination.js

Applied for loop from 1 to totalPosts/postsPerPage

Imported Pagination.js to App.js and sent two props totalPosts which is equal to posts.length and postsPerPage.

To apply pagination, we have to pass one more prop called paginate to pagination which will take number as an argumnet and will setCurrentPage to that number.

**Screenshot of output:-**
![image](https://user-images.githubusercontent.com/27857747/122382382-7ecf9500-cf87-11eb-81f5-7ccb8388aa2c.png)


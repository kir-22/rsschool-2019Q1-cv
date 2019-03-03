# Kireyeu Kiryll
##Contacts:
* **Phone:** _+375-29-809-24-90_;
* **E-mail:** _kirill89kireew@gmail.com_;
* **Skype:** _kirill.kireev9_.
##Summary:
> I learn easily. I like to learn something new. I'am purposeful, responsible. I like Javascript. I'd like to progress in Webdevelopment and create beautiful applications. I study Javascript and his frameworks (Node.js, TypeScript) himself. I finish a course - "Develop Game on Unity3D". I also want to create a HTML5 game. And I will make every effort to become a developer!

##Skills:
* C#, JavaScript, HTML5, CSS3, NodeJS, Unity3D, TypeScript, Less, Photoshop, Git, Bitrix, React(junior), Webpack.

##Example code:
` ``import { init, addInit } from './init';
let next;
let prev;
export{next, prev}
export function ajax(){
fetch(`https://www.googleapis.com/youtube/v3/search?key=AIzaSyDR4nYtKG6R4r2ByKEmvGl9Q3ulSRJcHbM&type=video&part=snippet&maxResults=15&q=${this.value}`)
.then((response)=>{
  return response.json();
})
.then((data)=>{
  next = data.nextPageToken;
  let arr = data.items.map((item)=> item.id.videoId);
  fetch(`https://www.googleapis.com/youtube/v3/videos?key=AIzaSyCTWC75i70moJLzyNh3tt4jzCljZcRkU8Y&id=${arr.join(',')}&part=snippet,statistics`)
  .then((res)=>{
    return res.json();
  })
  .then((stat)=>{
    console.log(stat.items);
    init(stat.items);
  })
});
}
export function addedAjax(next){
  fetch(`https://www.googleapis.com/youtube/v3/search?key=AIzaSyDR4nYtKG6R4r2ByKEmvGl9Q3ulSRJcHbM&type=video&part=snippet&maxResults=15&pageToken=${next}`)
  .then((response)=>{
    return response.json();
  })
  .then((data)=>{
    console.log('#1',next);
    console.log('#2', data);
    next = data.nextPageToken;
    prev = data.prevPageToken;
    let arr = data.items.map((item)=> item.id.videoId);
    fetch(`https://www.googleapis.com/youtube/v3/videos?key=AIzaSyCTWC75i70moJLzyNh3tt4jzCljZcRkU8Y&id=${arr.join(',')}&part=snippet,statistics`)
    .then((res)=>{
      return res.json();
    })
    .then((stat)=>{
      addInit(stat.items);
    })
  });
  }`` `
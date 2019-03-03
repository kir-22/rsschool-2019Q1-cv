# Kireyeu Kiryll

## Contacts:
* **Phone:** _+375-29-809-24-90_;
* **E-mail:** _kirill89kireew@gmail.com_;
* **Skype:** _kirill.kireev9_.

## Summary:
> I learn easily. I like to learn something new. I'am purposeful, responsible. I like Javascript. I'd like to progress in Webdevelopment and create beautiful applications. I study Javascript and his frameworks (Node.js, TypeScript) himself. I finish a course - "Develop Game on Unity3D". I also want to create a HTML5 game. And I will make every effort to become a developer!

## Skills:
* C#, JavaScript, HTML5, CSS3, NodeJS, Unity3D, TypeScript, Less, Photoshop, Git, Bitrix, React(junior), Webpack.

## Example code:

`` ` import { init, addInit } from './init';
  let next;
  let prev;
  export{next, prev};

`` `export function ajax(){

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
}
  `` `

## Practis:
1. Site: templa.by
2. Rsscool: Site LAMBDA
3. For test on platform: GeekBrains
4. For improve my skills on codewars: Codewars

## Course:

### HIGER ADUCATION
*2012* | Belarusian National Technical University

       | Instrument-making faculty, Micro and nanotechnics (engineer-technologist)

### PROFESSIONAL DEVELOPMENT, COURSES
*2018* | The basics of game development on Unity

       | HTP, Game Developer

*2014* | Software testing

       | Training Technology center "BelHard", SOFTWARE Testing (tester)

*2014* | Testing web-based applications

       | Training Technology center "BelHard", SOFTWARE Testing (tester)

## English level
>My level English is a A1-A2. I want to improve my English. I'd like to lern English fast. I study English himself: Duolingo, SkyEng, Youtoube video. I study him every day, because i want to speak English free.
![English Level](https://www.itestenglish.com/images/graph6.png)
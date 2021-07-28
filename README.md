# GSAP_Website

DEMO: https://midastung.github.io/GSAP_Website/index.html

## 以下內容是實作中的重點整理:
### GSAP - Timeline
>這個timeline功能可以不必理會上一部動畫的花時，再進行判斷下一個動畫的時間接續
```javascript=
const tl = gsap.timeline({ defaults: { ease: 'power1.out' } });
```
* timeline.to -> 從原本的樣子變成....
* timeline.from -> 從...樣子變成原本的樣子
* timeline.fromTo -> 從...變成... 
* " -= 1 " 再快1秒執行動畫
```javascript=
tl.to('.text', { y: '0%', duration: 1, stagger: 0.25 });
tl.to('.slider', { y: "-100%", duration: 1.5, delay: .5 });
tl.to('.intro', {y: "-100%", duration:1}, "-=1.2");
tl.fromTo('nav', { opacity: 0}, { opacity: 1, duration: 1});
tl.fromTo('.big-text', { opacity: 0}, { opacity: 1, duration: 1}, '-=1');
```

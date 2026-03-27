2026 Presentation about ratiometric scaling, utilizing data from the WASE and MESA studies as examples.

## [https://parameterz.github.io/beyond-the-ratio](https://parameterz.github.io/beyond-the-ratio)

Handy bookmarklet for turning the cursor into a laser pointer:

```
javascript:(function(){if(document.getElementById('__laser__')){document.getElementById('__laser__').remove();document.getElementById('__laser_style__')?.remove();return;}const s=document.createElement('style');s.id='__laser_style__';s.textContent='*{cursor:none!important}#__laser__{position:fixed;pointer-events:none;z-index:2147483647;width:18px;height:18px;border-radius:50%;background:radial-gradient(circle,#fff 0%,#ff2200 35%,rgba(255,34,0,0.4) 65%,transparent 100%);box-shadow:0 0 8px 4px rgba(255,60,0,0.7),0 0 20px 8px rgba(255,0,0,0.3);transform:translate(-50%,-50%);}.__laser_ghost__{position:fixed;pointer-events:none;z-index:2147483646;border-radius:50%;transform:translate(-50%,-50%);background:radial-gradient(circle,rgba(255,180,80,0.9) 0%,rgba(255,60,0,0.6) 40%,transparent 100%);box-shadow:0 0 6px 2px rgba(255,60,0,0.5);}';document.head.appendChild(s);const d=document.createElement('div');d.id='__laser__';document.body.appendChild(d);document.addEventListener('mousemove',e=>{d.style.left=e.clientX+'px';d.style.top=e.clientY+'px';const g=document.createElement('div');g.className='__laser_ghost__';const size=10+Math.random()*6;g.style.cssText='left:${e.clientX}px;top:${e.clientY}px;width:${size}px;height:${size}px;opacity:0.7;transition:opacity 2.5s ease-out,width 2.5s,height 1.5s;';document.body.appendChild(g);requestAnimationFrame(()=>{g.style.opacity='0';g.style.width='2px';g.style.height='2px';});setTimeout(()=>g.remove(),2550);});})();
```

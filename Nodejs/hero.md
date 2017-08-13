# Hero编辑器 {ignore= true}

<!-- @import "[TOC]" {cmd="toc" depthFrom=1 depthTo=6 orderedList=false} -->
<!-- code_chunk_output -->

* [创建启动项目](#创建启动项目)
* [显示hero](#显示hero)
* [创建HERO对象](#创建hero对象)

<!-- /code_chunk_output -->

## 创建启动项目

```
ng new angular-tour-of-heroes
cd angular-tour-of-heroes
ng serve -o
```

## 显示hero
> src\app\app.component.ts
```typescript
import { Component } from '@angular/core';
@Component({
  selector: 'app-root',
  template: `<h1>{{title}}</h1><h2>{{hero}} details!</h2>`,
  styleUrls: ['./app.component.css']
})
export class AppComponent {
  title = 'Tour of Heroes';
  hero = 'Windstorm';
}
```

网页查看执行效果：
![](assets/markdown-img-paste-2017081315510608.png)

## 创建HERO对象
修改如下代码：
> src\app\app.component.ts
```typescript
import { Component } from '@angular/core';

@Component({
  selector: 'app-root',
  template: `
    <h1>{{title}}</h1>
    <h2>{{hero.name}} details!</h2>
    <div><label>id: </label>{{hero.id}}</div>
    <div><label>name: </label>{{hero.name}}</div>
    `,
  styleUrls: ['./app.component.css']
})
export class AppComponent {
  title = 'Tour of Heroes';
  hero: Hero = {
    id: 1,
    name: 'Windstorm'
  };
}
export class Hero {
  id: number;
  name: string;
}
```

网页查看执行效果如下：
![](assets/markdown-img-paste-20170813160615235.png)



[返回](./readme.md)

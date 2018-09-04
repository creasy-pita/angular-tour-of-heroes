问题
1 @input 装饰器 
You used the @Input decorator to make the hero property available for binding by the external HeroesComponent.

2 import 其他 componet 后 在这些componet的什么功能 和 是怎么使用的  what ,how 

3 为什么 在 app.module.ts 导入后 就可以到处使用，到处使用指什么

4 <li *ngFor="let hero of heroes$ | async" >  heroes会否有更复杂的操作 比如  <li *ngFor="let hero of  formatA(heroes$) | async" >

5 Observable subscribe 包含了 事件概念，是否是 ：实时更新同步触发的概念
Observable 表示可观察对象，  此类对象 可以被订阅，订阅主体可以加入处理的功能逻辑 ，当可观察对象发生事件时，会执行这个功能逻辑代码 
比如
 
`let button = document.querySelector('button');`
`Rx.Observable.fromEvent(button,'click')//返回一个Observable对象`
`	.subscribe(()=>console.log('Clicked!'));`
把点击事件封装到一个Observable对象中，并转化成数据流的形式，最后通过subscribe方法对整个事件进行监听。当button发生click事件时 对应Observable对象便发出一个消息，这条消息会被subscribe()的observer的回调函数所捕获 并执行
注：了解了  观察者模式 观察者，监听者后比较容易理解 
6  keystroke 中keyup事件的解读  
##通过注册search(searchBox.value) 观察keyup事件。  
##search 内部传递给 可观察对象 searchTerms： private searchTerms = new Subject<string>(); 调用它的 next(value) 方法往 Observable 中推送一些值
##Pipe方法中 定义处理
  <input #searchBox id="search-box" (keyup)="search(searchBox.value)" /> 

7 路由  包括 路由出口和路由连接 和 路由模块
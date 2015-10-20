# 介绍React

* React 只针对View层的JavaScript库

* 一般常规的操作都是引入DOM操作库，例如jQuery, Zepto, Mootools等操作DOM, 但是每次操作DOM都会引发DOM树的更新，导致页面
刷新效率低。React把这种改变停留在虚拟DOM（JavaScript对象）上，检查状态，如果确实需要更新真实DOM时，也只是按需更新，这样会提高页面DOM更新效率。

关键概念:

    Virtual DOM：JavaScript模拟的DOM表述
    
    JSX: 类似于XML的标签语法，可以编译成JavaScript

    Synthetic Event System: 在DOM事件基础上封装了一层

    Components: 组件， UI Component, 可以继承
    
    Single data flow: 数据单向流
    
    Immutable.js: 保持数据不变性
    
    Flux: react 架构组织模式
    
    Isomorphic Applications: 代码即可以运行在客户端，也可以运行在服务端。一次编写，多处使用，可以用在Mobile，后台，前台
    
    React Native: 使用JavaScript, React编写原生iOS, Android应用。
    
JSX 转换为JavaScript

    var myText = "Hello";
    return <div className="foo">
        <p>{myText}</p>
        <img src="bar.png" />
    </div>;
    
    =>
    
    var myText = "Hello";
    return React.createElement('div', {className: 'foo'},
      React.createElement('p', {}, myText);
      React.createElement('img', {src: 'bar.png'});
    );
    


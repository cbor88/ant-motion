---
order: 4
title: 背景随滚动下滑
hidden: true
cols: 1
---

背景随滚动下滑(待优化)。

````jsx
import BannerAnim, { Element } from 'rc-banner-anim';
import TweenOne from 'rc-tween-one';
import 'rc-banner-anim/assets/index.css';
class Demo extends React.Component {
  render(){
    return (
      <BannerAnim prefixCls="banner-user" bgParallaxAll={{ y: [-1500, 200] }}>
        <Element 
          prefixCls="banner-user-elem"
          key="0" 
          bg="https://os.alipayobjects.com/rmsportal/IhCNTqPpLeTNnwr.jpg"
        >
          <TweenOne className="banner-user-title" animation={{ y: 30, opacity: 0, type: 'from' }}>Ant Motion Demo</TweenOne>
          <TweenOne className="banner-user-text" animation={{ y: 30, opacity: 0, type: 'from', delay: 100 }}>Image source from the network Demo, please upload pictures to replace.Image source </TweenOne>
        </Element>
        <Element 
          prefixCls="banner-user-elem"
          key="1" 
          bg="https://os.alipayobjects.com/rmsportal/uaQVvDrCwryVlbb.jpg"
        >
          <TweenOne className="banner-user-title" animation={{ y: 30, opacity: 0, type: 'from' }}>Ant Motion Demo</TweenOne>
          <TweenOne className="banner-user-text" animation={{ y: 30, opacity: 0, type: 'from', delay: 100 }}>Image source from the network Demo, please upload pictures to replace.Image source </TweenOne>
        </Element>
      </BannerAnim>);
  }
}
ReactDOM.render(
  <Demo />
, mountNode);
````

````css
.banner-user-elem{
  height: 400px;
  text-align: center;
  color: #fff;
  position: relative;
  overflow: hidden;
}
.banner-user-elem .banner-user-title{
  font-size: 22px;
  top: 40%;
}
.banner-user-elem .banner-user-text{
  top: 40%;
}
````

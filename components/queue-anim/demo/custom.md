---
order: 4
title: 自定义动画进出场
cols: 2
---

通过 `animConfig` 来自定义动画进出场。

````jsx
import { Button } from 'antd';
import QueueAnim from 'rc-queue-anim';

const Test = React.createClass({
  getInitialState() {
    return {
      show: true,
    };
  },
  onClick() {
    this.setState({
      show: !this.state.show,
    });
  },
  render() {
    return (
      <div>
        <p className="buttons">
          <Button type="primary" onClick={this.onClick}>切换</Button>
        </p>
        <QueueAnim className="demo-content"
          animConfig={[
            { opacity: [1, 0], translateY: [0, 50] },
            { opacity: [1, 0], translateY: [0, -50] }
          ]}>
          {this.state.show ? [
            <div className="demo-kp" key="a">
              <ul>
                <li></li>
                <li></li>
                <li></li>
              </ul>
            </div>,
            <div className="demo-listBox" key="b">
              <div className="demo-list">
                <div className="title"></div>
                <ul>
                  <li></li>
                  <li></li>
                  <li></li>
                </ul>
              </div>
            </div>
          ] : null}
        </QueueAnim>
      </div>
    );
  }
});

ReactDOM.render(<Test />, mountNode);
````

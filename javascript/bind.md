# Bind vs. Arrow Functions

I put together a quick [jsperf](https://jsperf.com/bind-vs-arrow-function-test/1) to show the difference between bind and arrow functions for binding arguments.

In a React setting, this would be valuable in something like this:

```javascript
class MyBooklist extends Component {
  state = {
    items: [{id: 1, read: false}, {id: 2, read: false}, {id: 3, read: false}]
  }
  toggleRead = ({id, read}) => {
    this.setState({
      items: this.state.items.map(i => (i.id === id) ? {id, read: !read} :  i)
    })
  }
  render(){
    return <ul>
      {this.state.items.map(item => <li key={item.id} onClick={() => this.toggleRead(item)}>{item.id} - {item.read ? "Read" : "Not Read"}</li>)}
    </ul>
  }
}

ReactDOM.render(<MyBooklist />, document.getElementById('root'));
```

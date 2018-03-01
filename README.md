# react-jsonrpc-client
A JSON Rpc client for React that uses promises to call to JSON Rpc APIs.

## Usage Example
```javascript
import JsonRpcClient from '/path/to/jsonrpcclient'
class TutoringCalendar extends Component {
  componentDidMount() {
    var api = new JsonRpcClient({
      endpoint: 'https://url.to/api',
      headers: {
        'X-Token': this.state.token
      }
    })
    api.request(
      METHOD_NAME,
      PARAM_1,
      PARAM_2,
      PARAM_3
    ).then(function(response) {
      this.setState({apiResponse: response})
    }.bind(this)
  }

}

## Usage

### Initialize a request

```ruby
HttpClient::Request.new(method: )
```




### Options

| option        | Description | Default |
|---------------|-------------|---------|
| method        | Http request method | ```:get``` |
| app           | This attribute is responsible for getting all the corresponding info related to the application you are sending a request to, add the application info to .env file and prefix them with the name; e.g., 'APPNAME_URL'. |
| retry_count   | The number of retries incase of failure. | ```0``` |
| data          |  |
| headers       | |
| success_block |

### Configuration

in your ```.env``` file add your applications list with replacing the ```APPNAME``` and the values :
```
## Applications_List 
APPNAME_APP_ID=12345678
APPNAME_TOKEN=123lASDASD12324
APPNAME_URL=https://jsonplaceholder.typicode.com/posts
```

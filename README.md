## Usage
you can use the gem by starting a request :
```ruby
HttpClient::Request.new(method:, app:, retry_count:, data:, headers:, &success_block)
```
and you should pass the arguments as shown in the options section.
### Options

| option        | Description | Default |
|---------------|-------------|---------|
| method        | Http request method | ```:get``` |
| app           | This attribute is responsible for getting all the corresponding info related to the application you are sending a request to, add the application info to .env file and prefix them with the name; e.g., 'APPNAME_URL'. |
| retry_count   | The number of retries incase of failure. | ```0``` |
| data          | This should be the query data when method is ```:get``` or the data you are sending when method is ```:post, :put or :patch```. | ```{}``` |
| headers       | This contains the headers of your request | ```{}``` |
| success_block | This will be executed when the response status is success |

### Configuration

in your ```.env``` file add your applications info with replacing the ```APPNAME``` and the values :

```
APPNAME_APP_ID=12345678
APPNAME_TOKEN=123lASDASD12324
APPNAME_URL=https://jsonplaceholder.typicode.com/posts
```
## Example 
After installing the Gem 
put in your rails application wherever you want to use it:
```ruby
HttpClient::Request.new(
                  method: :get,  
                  app: :example_app, 
                  retry_count: 5, 
                  headers: { 'Content-Type': 'application/json' }
                )
```
create a ```.env``` file and put your application info on it : 
```
EXAMPLE_APP_URL=https://jsonplaceholder.typicode.com/posts
```

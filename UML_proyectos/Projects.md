## Project one: Twitter use case and class diagrams

![Project 1 diagram](https://i.postimg.cc/8kfhGs3K/P1-Twitter-drawio.png)

### Project one: Teacher's solution to Twitter use case diagram

![Project 1 use case teacher solution](https://s3-us-west-2.amazonaws.com/devcamp-pictures/Problem+Solving+images/Project+1%3A+Twitter/Post+Tweet+use+case+diagram.PNG)

### Project one: Teacher's solution to Twitter class diagram

![Project 1 class teacher solution](https://s3-us-west-2.amazonaws.com/devcamp-pictures/Problem+Solving+images/Project+1%3A+Twitter/Twitter+Class+Diagram.PNG)

______________________________________________________________________

## Project two: E-commerce diagrams (class & activity)

![Project 2 my solution](https://i.postimg.cc/WzZrwfgL/ecommerce-project-2-drawio.png)

### Project two: Teacher's solution to E-commerce activity diagram 

![Project 2 teacher solution ac](https://s3-us-west-2.amazonaws.com/devcamp-pictures/Problem+Solving+images/Project+2%3A+Coffee+Ordering+Application/eCommerce+Activity+Diagram.png)

### Project two: Teacher's solution to E-commerce class diagram

![Project 2 teacher solution class](https://s3-us-west-2.amazonaws.com/devcamp-pictures/Problem+Solving+images/Project+2%3A+Coffee+Ordering+Application/eCommerce+Class+Diagram.PNG)


_________________________________________________________________________

## Project three: Phone parser diagrams (package & sequence)

![p3 my solution](https://i.postimg.cc/kMwHx18w/p3-phone-parser.jpg)

### Project three: Teacher's solution to package diagram

```
require "phone_parser/version"
require "phone_parser/country_codes"

module PhoneParser
  def self.parse(number, country_code: '1')
    number.delete!("^0-9")
    digit_length_validator(number)
    CountryCodes.country_code_validator(number, country_code)
  end

  def self.digit_length_validator number
    number.length < 10 ? (raise PhoneLengthError) : (number)
  end
end

class PhoneLengthError < StandardError
  def message
    'Phone numbers need to have at least 10 digits'
  end
end

```

![package diagram](https://s3-us-west-2.amazonaws.com/devcamp-pictures/UML+images/Screen+Shot+2017-10-12+at+4.09.39+PM.png)

### Project three: Teacher's solution to sequence diagram

![p3 sequence diagram](https://s3-us-west-2.amazonaws.com/devcamp-pictures/Problem+Solving+images/Project+3%3A+Phone+Parsing+Code+Library/Phone+Parser+sequence+diagram.PNG)

_______________________________________________________

## Project four: Fleet management system (activity, package, deployment, class)

Cursive in Package means that's copied from the teacer's solution

![p4 act pckg](https://i.postimg.cc/vB8gZ3tK/p4-fleet-management-acc-pckg.jpg)

![p4 dep class](https://i.postimg.cc/YkqFZRhf/p4-fleet-part-2.jpg)

### Project four: Teacher's solution to fleet management system (activity & package)

![p4 acc teacher](https://s3-us-west-2.amazonaws.com/devcamp-pictures/Problem+Solving+images/Project+4%3A+Enterprise+Fleet+Management+System/Maintenance+activity+diagram.PNG)

![p4 pckg teacher](https://s3-us-west-2.amazonaws.com/devcamp-pictures/Problem+Solving+images/Project+4%3A+Enterprise+Fleet+Management+System/Fleet+Management+System+package+diagram.PNG)

### Project four: Teacher's solution to fleet management system (deployment & class)

![p4 dep teacher](https://s3-us-west-2.amazonaws.com/devcamp-pictures/Problem+Solving+images/Project+4%3A+Enterprise+Fleet+Management+System/Fleet+Management+System+deployment+diagram.PNG)

Starting with the load balancer, I went with one of the most basic options here,k which is a 50 percent traffic split. This means that if I get two requests then the first one I'm going to be sending to the first application server and then the second one I'm going to be sending to the secondary server. So if User A comes in when they go the Web site the load balancer takes that traffic and redirects them here. User B hits it right afterwards and then they are sent here and the whole point of using a load balancer is pretty much like it sounds. You want to balance the load of traffic so that you're not so dependent on one system. The other nice benefit is if there's some kind of fault with this application server, and it goes down, then this other server can take all of the requests.

So how are these application servers able to serve identical content and pages to the user? A lot of it comes down to the cache cluster. What caching allows you to do is to be able to save references and other components either on the user's system or on your own server. This is a critical component when it comes to improving the performance of applications.

Lastly, we have our database cluster. Part of the reason why I structured it this way is because this is a pretty common pattern. You want to be able to cache certain items that are not changed on a regular basis--usually view-centric items--however, you don't want to cache data. Imagine a scenario where you have a user who wants to go check the status of their maintenance request. If you cache that maintenance request then that record is not going to update for them, even if someone went in and did change the status. So it's very important to understand which items should be cached and which ones shouldn't. Usually the way that I will run something like this is anything that changes on a regular basis I'll place inside of the database cluster and then I will not perform any caching on that.

![p4 class teacher](https://s3-us-west-2.amazonaws.com/devcamp-pictures/Problem+Solving+images/Project+4%3A+Enterprise+Fleet+Management+System/Fleet+Management+System+class+diagram.PNG)

_____________________________________________________________

## Project five: Uber car service (Activity, package, use case, deployment)

![p5 act pkg](https://i.postimg.cc/8kKgnFhR/P5-uber-1.jpg)

![p5 uc dep](https://i.postimg.cc/wMGKtP6f/P5-uber-2.jpg)

### Project five: Teacher's solution to Uber project (activity & package)

![p5 acc teacher](https://s3-us-west-2.amazonaws.com/devcamp-pictures/Problem+Solving+images/Project+Solution%3A+Uber+Activity+Diagram+%23+1313/image1.png)

![p5 pkg teacher](https://s3-us-west-2.amazonaws.com/devcamp-pictures/Problem+Solving+images/Project+Solution%3A+Uber+Package+Diagram+%23+1314/image1.png)

### Project five: Teacher's solution to Uber project (use case & deployment)

![p5 uc teacher](https://s3-us-west-2.amazonaws.com/devcamp-pictures/Problem+Solving+images/Project+Solution%3A+Uber+Use+Case+Diagram+%23+1315/image1.png)

![p5 dep teacher](https://s3-us-west-2.amazonaws.com/devcamp-pictures/Problem+Solving+images/Project+Solution%3A+Uber+Deployment+Diagram+%23+1316/image1.png)

___________________________________________________________

## Project six: Education assesment system (activity, class, state machine, deployment)

![p6 act class](https://i.postimg.cc/LsrJ6T5k/p6-education-part-1.jpg)

Cursive is from teacher's solution

![p6 sm dep](https://i.postimg.cc/2yHbmfZy/P6-part-2.jpg)

### Project six: Teacher's solution to education assesment system (activity & class)

![p6 act teacher](https://s3-us-west-2.amazonaws.com/devcamp-pictures/Problem+Solving+images/Project+Solution%3A+Education+Assessment+Activity+Diagram+%23+1317/image1.png)

![p6 class teacher](https://s3-us-west-2.amazonaws.com/devcamp-pictures/Problem+Solving+images/Project+Solution%3A+Education+Assessment+Class+Diagram+%23+1318/image1.png)

### Project six: Teacher's solution to education assesment system (state machine & deployment)

![p6 sm teacher](https://s3-us-west-2.amazonaws.com/devcamp-pictures/Problem+Solving+images/Project+Solution%3A+Education+Assessment+State+Machine+Diagram+%23+1319/image1.png)

![p7 dep teacher](https://s3-us-west-2.amazonaws.com/devcamp-pictures/Problem+Solving+images/Project+Solution%3A+Education+Assessment+Deployment+Diagram+%23+1320/image1.png)

_______________________________________________________

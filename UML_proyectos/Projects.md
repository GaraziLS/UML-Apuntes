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

## Project four: Fleet management system (activity, package)

Cursive in Package means that's copied from the teacer's solution

![p4 acc pckg](https://i.postimg.cc/vB8gZ3tK/p4-fleet-management-acc-pckg.jpg)

### Project four: Teacher's solution to fleet management system (activity)

![p4 acc teacher](https://s3-us-west-2.amazonaws.com/devcamp-pictures/Problem+Solving+images/Project+4%3A+Enterprise+Fleet+Management+System/Maintenance+activity+diagram.PNG)

### Project four: Teacher's solution to fleet management system (activity)

![p4 pckg teacher](https://s3-us-west-2.amazonaws.com/devcamp-pictures/Problem+Solving+images/Project+4%3A+Enterprise+Fleet+Management+System/Fleet+Management+System+package+diagram.PNG)
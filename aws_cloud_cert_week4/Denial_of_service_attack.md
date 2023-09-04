# <ins> Denial-of-Service Attacks </ins> #

- D-D-O-S, DDoS, the `distributed denial-of-service`. It's an `attack` `on your enterprise infrastructure`

- `you've heard of it`,` Your security team might have written a plan for it`.`You know that many businesses have been devastated by it`

-  But `what exactly is it`? And `more importantly`,` how can you defend against it?`

- But to be clear, `this is a 14-hour discussion to really understand it all`. 

- But you need to `at least know the fundamentals of how the attacks are carried out`. And `how AWS can "automatically defend your infrastructure" from these crippling assaults.`

- The `objective of a DDoS attack` `is to shut down your application's ability to function` `by overwhelming the system to the point` `it can no longer operate.`

- `In normal operations, your application takes requests from customers and returns results.`

- `In a DDoS attack`, the `bad actor tries to overwhelm the capacity of your application`,` basically to deny anyone your services.`

- `But a single machine attacking your application` `has no hope of providing enough of an attack by itself.`

- `So the distributed part is that the attack leverages other machines around the Internet to unknowingly attack your infrastructure`

- `The bad actor creates an army of zombie bots, brainlessly assaulting your enterprise`

- `The key to a good attack, and I call it that, when I should call it powerful, I mean it's definitely chaotic evil.`

- `But the key is to have the assault commander do the smallest amount of work needed`

- `And have the targeted victim receive an unbearable load of resulting work they must process through`

- So `let me cherry-pick a few specific attack examples that work really well.`


    - `The UDP flood` :-

        - `it is based on the helpful parts of the Internet, like the National Weather Service`

        - Now `anyone can send a small request to the weather service and ask, give me weather`. And `in return`, `the weather service's fleet of machines will send back a massive amount of weather telemetry forecasts, updates, lots of stuff.`

        - `So the attack here is simple`

        - `The bad actor, sends a simple request, give me weather, but it gives a fake return address on the request , your return address`

        - `So, now the weather service very happily floods your server with megabytes of rain forecasts`

        - `your system could be brought to a standstill just sorting through the information it never wanted in the first place.`


    - Now, `that is one example of half a dozen low level brute force attacks`, `all designed to exhaust your network.`

    - `Some attacks are much more sophisticated`, like the `HTTP level attacks`

    - `HTTP level attacks` :-

        - `which look like normal customers asking for normal things.`

        - `Like complicated product searches over and over and over, all coming from an army of zombified bot machines`

        - `They asked for so much attention that regular customers can't get in.`

    
    - `They even try horrible tricks like the Slow Loris attack.`

    - `Slow Loris attack`:-

        - `Imagine, standing in line at the coffee shop when someone in front of you takes seven minutes to order their whatever it is they're ordering`

        - `And you don't get to order until they finish and get out of your way`

        - `A Slow Loris attack is the exact same thing.`

        - `Instead of a normal connection`, `I would like to place an order in the normal way of saying`

        - `The attacker pretends to have a terribly slow connection by` very slow voice of `I would like to place an order`

        - `You get the picture.`

        - `Meanwhile, your production servers are standing there waiting for the customer to finish their requests, they can dash off and return the result.`

        -  `But until they get the entire packet, they can't move on to the next thread, the next customer`


    - `A few Slow Loris attackers can exhaust the capacity of your entire front-end with almost no effort at all.`


- `I could go on monologuing for hours just talking about the elegantly evil architecture of these attacks`

- `But we are on the clock here, and it is time to stop these attacks cold`

- `Here's the cool solution, you already know the solution`

- `Everything we've been talking about over this entire course` `is not only good architecture`, `but it also helps solve almost all DDoS attack vectors` `with` `zero additional effort or cost.`

- First attack, the low level network attacks like the UDP floods, solution :- 

    - `Security Groups`

    - `Security groups only allow in proper request traffic`

    - `Things like weather reports use an entirely different protocol than the ones your customers use.`

    - `Not on the list, you don't get to talk to the server.`

    - `And what's more?` `Security groups operate at the AWS network level`, `not at the EC2 instance level like an operating system firewall might`

    - So massive attacks like `UDP floods or reflection attacks` just get `shrugged off by the scale of the entire AWS regions capacity`. `Not your individual EC2s capacity.`

- `This is a case where our size is a huge advantage in your protection.`

- `I won't say it's impossible to overwhelm AWS, but the scale it would take, it would be too expensive for these bad actors.`

- `Slow Loris attacks? How to Get rid of it :- `

    - `Look at our elastic load balancer`

    - `Because the ELB handles the HTTP traffic request first`

    - `So it waits until the entire message, no matter how fast or slow, is complete before sending it over to the front-end web server.`

    - `Sure, you can try to overwhelm it. `

    - `But remember how the ELB is scalable,`

    - `how it runs at the region level.`

    - `To overwhelm ELB, you would once again have to overwhelm the entire AWS region.`


- `It's not theoretically impossible, but too massively expensive for anyone to pull off.`

- For the `sharpest, most sophisticated attacks`, `AWS also offers specialized defense tools called AWS Shield with AWS WAF i.e AWS Web application firewall`.

- `AWS WAF uses a web application firewall to filter incoming traffic for the signatures of bad actors`

- `It has extensive machine learning capabilities and can recognize new threats as they evolve.`

- A`nd proactively help defend your system against an ever growing list of destructive vectors`

- `The take away is a well architected system, is already defended against most attacks`

- ` by using AWS Shield Advanced, you can turn AWS into your partner against DDoS attacks.`
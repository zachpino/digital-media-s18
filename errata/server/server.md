Servers are no different from the computers that we use every day, except that they are often `headless`, and lack any kind of display or input. Instead, they sit in stacks of hundreds of identical machines in air conditioned `datacenters` in locations where real estate is cheap and internet access is fast. Each physical machine can also be partitioned into several virtual machines, so that many users can use the resources of each server and determine their own configurations.

![datacenter](http://datacenterfrontier.com/wp-content/uploads/2015/09/amazon-dc-hamilton.jpg)

Amazon offers services via AWS that powers the servers and other parts of the technology stack of a significant proportion of the internet. We are using it in class because of its free tier and genericness, but other options are available such as the recommendable [Dreamhost](http://www.dreamhost.com) and [HostGator](http://www.hostgator.com). [Google Cloud Computing](http://cloud.google.com) is a competing service as well that offers more power at the cost of complexity.

EC2, Elastic Compute Cloud, is AWS's server offering. 

- Visit http://www.aws.amazon.com.
- Create an account on AWS.
- Login to see the AWS dashboard. 
- Visit the Services menu, and under the `Compute` menu, select `EC2`.
- Click the `Launch Instance` button.

AWS will then offer you options for which operating system and configuration to install on the virtual server we are now creating. These preset configurations are called `Amazon Machine Images`, and many exist for very specific purposes like hosting Wordpress sites and running academic computing applications. 

Servers tend to use Linux or Windows as their operating system, though Mac servers exist [at tremendous relative cost](https://macminicolo.net). Linux servers are far more common, as Linux is a free and open source operating system. In class, we will use the well-supported and fairly standard Ubuntu Linux Server without any fanciness at the start.

- Select `Ubuntu Server 16.04 LTS (HVM), SSD Volume Type - ami-b7a114d7`
- Select `t2.micro` Instance Size, which is tagged `free tier eligible`
- Click `Next` a few times, to get to the `Step 6: Configure Security Group` 
- On this screen, we can set how our server can be accessed securely. `Add Rule` to allow this server access for `HTTP` and `HTTPS` and ensure the `Source` is set to `Anywhere`.
- Click `Review and Launch`

You will get a warning about security on the review screen. Don't worry, we'll lock things down in the next step.

- Click `Launch`

A popup will ask you to create a new key pair. This is a file that will allow access to your 

- In the first dropdown menu, select `Create a new key pair`
- Name your keypair file and `Download` it.

This file is incredibly important, and serves to identify you as a secure user of your server. We'll return to it soon, don't delete it!

After a short delay during which Amazon is creating and configuring your virtual server, your machine will boot up for the first time, which is indicated with a `running` green light in the AWS.

Let's now [assign an IP address](assignip.md) so that your server can be accessed on the internet.

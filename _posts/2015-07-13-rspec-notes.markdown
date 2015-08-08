---
layout: post
title:  "My RSpec Notes"
date:   2015-07-13
categories: notes rspec
---

This post talks about setting up and using RSpec and is based on Code School's course on RSpec. This will serve as my general reference/resources point when using RSpec.

## Setting Up

### Install/Update RSpec

{% highlight ruby %}
gem install rspec
{% endhighlight %}

### Add To A Project

{% highlight ruby %}
# must be done inside of project directory
rspec --init
{% endhighlight %}

## Basics

### Where To Save Files

Assuming the file you're writing tests for exists within the lib directory (e.g. /lib/file.rb), you will want to save your respective spec (read: test - test is synonymous with specification here) file in the spec/lib/ directory (e.g. spec/lib/file_spec.rb).

Inside the file, you want to include the following:
{% highlight ruby %}
require "spec_helper"
{% endhighlight %}

### Writing A Test

Inside your *spec/lib/monkey_spec.rb* file:
{% highlight ruby %}
require "spec_helper"
require "monkey" # require the monkey.rb file

describe Monkey do # here, Monkey is the name of the class we're testing
    # Monkey could be replaced with a string like "A Monkey"
    it "is named Frank" do
        # create the environment
        monkey = Monkey.new(name: "Frank")
        # create the expectation
        monkey.name.should == 'Frank'
    end

    it "has no bananas" do
        monkey = Monkey.new(name: "Frank")

        monkey.bananas.should < 1
    end
end
{% endhighlight %}

Inside your *lib/monkey.rb* file:

{% highlight ruby %}
class Monkey

attr_accessor :name, :bananas

def initialize(args = {})
    @name = args.fetch(:name)
    @bananas = args.fetch(:bananas, 0)
end

end
{% endhighlight %}

### Terminology

**matcher** - Operator used for comparison within an expectation.

**modifier** - This is what we use to define what we expect (e.g. "#.should").
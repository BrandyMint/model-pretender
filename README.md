# Model::Pretender

TODO: Write a gem description

## Installation

Add this line to your application's Gemfile:

    gem 'model-pretender'

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install model-pretender

## Usage

    class TestClass < ModelPretender
      boolean_attr_accessor :boolean
      date_attr_accessor :date 
      time_attr_accessor :time 
      integer_attr_accessor :integer 
    end

    time = Time.now
    date = Date.today
    
    test=TestClass.new({ :boolean=>'1', :date=>date.to_s, :time => time.to_s, :integer => '3' })
    test.boolean # true
    test.date # Date
    test.time # Time
    test.integer # 3
    
    form_for(test) # Supported
    test.attributes # Hash
    test.serializable_hash # Hash

## Contributing

1. Fork it
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request

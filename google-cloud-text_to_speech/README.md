# Ruby Client for Cloud Text-to-Speech API ([Alpha](https://github.com/googleapis/google-cloud-ruby#versioning))

[Cloud Text-to-Speech API][Product Documentation]:
Synthesizes natural-sounding speech by applying powerful neural network
models.
- [Client Library Documentation][]
- [Product Documentation][]

## Quick Start
In order to use this library, you first need to go through the following
steps:

1. [Select or create a Cloud Platform project.](https://console.cloud.google.com/project)
2. [Enable billing for your project.](https://cloud.google.com/billing/docs/how-to/modify-project#enable_billing_for_a_project)
3. [Enable the Cloud Text-to-Speech API.](https://console.cloud.google.com/apis/library/texttospeech.googleapis.com)
4. [Setup Authentication.](https://googleapis.github.io/google-cloud-ruby/#/docs/google-cloud/master/guides/authentication)

### Installation
```
$ gem install google-cloud-text_to_speech
```

### Preview
#### TextToSpeechClient
```rb
require "google/cloud/text_to_speech"

text_to_speech_client = Google::Cloud::TextToSpeech.new
text = "test"
input = { text: text }
language_code = "en-US"
voice = { language_code: language_code }
audio_encoding = :MP3
audio_config = { audio_encoding: audio_encoding }
response = text_to_speech_client.synthesize_speech(input, voice, audio_config)
File.open('example.mp3', "wb"){|file| file.write response.audio_content}
```

### Next Steps
- Read the [Client Library Documentation][] for Cloud Text-to-Speech API
  to see other available methods on the client.
- Read the [Cloud Text-to-Speech API Product documentation][Product Documentation]
  to learn more about the product and see How-to Guides.
- View this [repository's main README](https://github.com/googleapis/google-cloud-ruby/blob/master/README.md)
  to see the full list of Cloud APIs that we cover.

[Client Library Documentation]: https://googleapis.github.io/google-cloud-ruby/#/docs/google-cloud-text_to_speech/latest/google/cloud/texttospeech/v1
[Product Documentation]: https://cloud.google.com/texttospeech

## Enabling Logging

To enable logging for this library, set the logger for the underlying [gRPC](https://github.com/grpc/grpc/tree/master/src/ruby) library.
The logger that you set may be a Ruby stdlib [`Logger`](https://ruby-doc.org/stdlib-2.5.0/libdoc/logger/rdoc/Logger.html) as shown below,
or a [`Google::Cloud::Logging::Logger`](https://googleapis.github.io/google-cloud-ruby/#/docs/google-cloud-logging/latest/google/cloud/logging/logger)
that will write logs to [Stackdriver Logging](https://cloud.google.com/logging/). See [grpc/logconfig.rb](https://github.com/grpc/grpc/blob/master/src/ruby/lib/grpc/logconfig.rb)
and the gRPC [spec_helper.rb](https://github.com/grpc/grpc/blob/master/src/ruby/spec/spec_helper.rb) for additional information.

Configuring a Ruby stdlib logger:

```ruby
require "logger"

module MyLogger
  LOGGER = Logger.new $stderr, level: Logger::WARN
  def logger
    LOGGER
  end
end

# Define a gRPC module-level logger method before grpc/logconfig.rb loads.
module GRPC
  extend MyLogger
end
```

## Supported Ruby Versions

This library is supported on Ruby 2.3+.

Google provides official support for Ruby versions that are actively supported
by Ruby Core—that is, Ruby versions that are either in normal maintenance or
in security maintenance, and not end of life. Currently, this means Ruby 2.3
and later. Older versions of Ruby _may_ still work, but are unsupported and not
recommended. See https://www.ruby-lang.org/en/downloads/branches/ for details
about the Ruby support schedule.

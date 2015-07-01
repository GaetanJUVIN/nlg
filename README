# Hi everyone.

NLG is very easy to use.

```sh
$ gem 'nlg', github: "GaetanJUVIN/nlg"
```

Example:

#### test_nlg.rb
```sh
require 'nlg'

dataset_json = File.read("json_place.txt")
dataset = JSON.parse(dataset_json)
paragraph = Nlg::Paragraph.new(dataset["subjects"], dataset["defaults"])
paragraph.build
paragraph.sentences.each do |sentence|
  puts sentence
end
```

#### json_place.txt
```sh
{
	"defaults": {
	"tense": "present",
		"verb": "have",
		"pronoun": "it", 
		"voice": "active",
		"aspect": "habitual",
		"preposition": "of"
	},

	"subjects": {
		"subject": "Pune",
		"objects": {
			"population":{
				"value": "57841284790",
				"specifications": {}
			},
			"rainfall": {
				"value": "198",
				"specifications": {
			    	"complement": "mm"
			        }
				},
			"high temperature": {
				"value": "45",
				"specifications": {
					"complement": "°C"
				},
				"conjugated_with": ["low temperature"]
				},
			"low temperature": {
				"value": "20",
				"specifications": {
					"complement": "°C" },
					"conjugated_with": ["high temperature", "low temperature", "rainfall"]
				},
			"forts": {
				"value": ["sinhgad", "lohgad"],
				"specifications": {
					"preposition": "named"
				},
				"conjugated_with": ["high temperature", "low temperature", "rainfall"]
			}
		}
	}
}
```

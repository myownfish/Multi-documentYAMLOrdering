# Multi-documentYAMLOrdering

Difference between Spring Boot 2.3 and 2.4

Multi-document YAML Ordering
If you use multi-document YAML files (files with --- separators) then you need to be aware that property sources are now added in the order that documents are declared. With Spring Boot 2.3 and earlier, the order that the individual documents were added was based on profile activation order.

If you have properties that override each other, you need to make sure that the property you want to "win" is lower in the file. This means that you may need to reorder the documents inside your YAML.

Spring Boot 2.3: profile activated last has higher priority
Spring Boot 2.4: profile write at the bottom of the YAML files has higer priority

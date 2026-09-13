# VAT-Identifier-Discovery

Q:UK VAT numbers are nine digits with a checksum, so only a small fraction of the possible combinations are valid. What happens if you point that observation at HMRC’s checker, and is it a good idea?
A:The checksum can help remove invalid VAT numbers before checking them with HMRC. However, I would not generate large numbers of VAT candidates and test them all, as this could create too many requests. I would use the checksum mainly to check VAT numbers that were already found. 

Q:how would you keep this dataset current, given companies register and deregister continuously?
A:I would periodically update the dataset using Companies House to identify newly registered, changed or deregistered companies. Existing VAT numbers could also be revalidated periodically, with the date of the last verification stored for each record.

Q:how would you know your dataset was wrong at scale, with nothing complete to compare it against?
A:Without a complete reference dataset, it would not be possible to know with certainty that the dataset is wrong at scale. I would regularly check a random sample manually and look for things such as invalid VAT numbers or company details that do not match. 

Q:which of your sources would you not be comfortable using in a product we sell, and why?
A:I would not rely directly on AI-generated results because they can be wrong or outdated. I would also be careful with unknown third-party websites. They can be useful for finding possible VAT numbers, but I would verify the information using more reliable sources such as Companies House and HMRC. 

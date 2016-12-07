java logstash和 ruby logstash 做一个对比(4cores 4g 虚拟机)



|app	        |filter	|filteworkers	    |cpu used(avg)|data example	  |data numbers	|time consuming（测试10次的avg）|
|:------------- |:----- |:----------------- | -----------:|:------------- | -----------:| ----------------------------:|
|rubylogstash	|grok	|4(默认cpu核数)	|280%	       |apache	       |1000w	|1625s|
|javalogstash	|grok	|4(默认cpu核数)	|330%	       |apache	       |1000w	|543s|						
|rubylogstash	|null	|4(默认cpu核数)	|200%	       |字符串(test 01) |1000w   |705s|
|javalogstash	|null	|4(默认cpu核数)	|180%	       |字符串(test 01) |1000w   |170s|
|rubylogstash	|json	|4(默认cpu核数)	|260%	       |json 字符串     |1000w   |1504s|
|java logstash	|json	|4(默认cpu核数)	|310%	       |json 字符串     |1000w   |430s|

以上三种场景的处理效率，javalogstash是rubylogstash的倍数分别是2.99倍  4.15倍  3.49倍


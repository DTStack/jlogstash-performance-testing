java logstash和 ruby logstash 做一个对比(4cores 4g 虚拟机)



app	filter	filteworkers	cpu used(avg)	data example	data numbers	time consuming（测试10次的avg）

ruby logstash	grok	4(默认cpu核数)	280%	apache	1000w	1625s

java log stash	grok	4(默认cpu核数)	330%	apache	1000w	543 s

						
						
ruby logstash	null	4(默认cpu核数)	200%	字符串(test 01)	1000w	705s

java log stash	null	4(默认cpu核数)	180%	字符串(test 01)	1000w	170s
						
ruby logstash	json	4(默认cpu核数)	260%	json 字符串	1000w	1504s

java logstash	json	4(默认cpu核数)	310%	json 字符串	1000w	603s

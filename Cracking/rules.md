---
layout: default
title: Rule based cracking
parent: Wiki/Cracking/cracking.md
---
<h1>Rule based cracking hashcat</h1>

example:
{% highlight bash%} 
hashcat -m 5600 /home/user1/hash.txt /home/user1/wordlist.txt --rules=/opt/hashcat/rules/best64.rule -O -w 3
{% endhighlight %}

Recommended order for efficient rule based cracking:
1 - best64.rule
2 - InsidePro-PasswordsPro.rule
3 - rockyou-30000.rule
4 - OneRuleToRuleThemAll.rule

OneRuleToRuleThemAll.rule:
https://www.notsosecure.com/one-rule-to-rule-them-all/
A very powerful rule that has the highest successful cracking rate. It is not the most efficient however.

If all else fails you can try the very extensive dive.rule (this will take a long time).
Always make sure you have a good wordlist to go along with these rules. rockyou.txt is usually a good starting place.


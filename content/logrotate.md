[https://linux.cn/article-4126-1.html](https://linux.cn/article-4126-1.html)

## daily and size
dail and size is contradictory.

local definitions override global ones, and later definitions > override earlier ones from the manpage of logrotate.

```shell
logrotate -d -v rotatefile.conf
```
> use the verbose option to see which rules are used. From my tests I believe only the last rule is used because more specific rules can override more general rules. 

https://serverfault.com/questions/391538/logrotate-daily-and-size
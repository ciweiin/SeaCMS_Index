# 可能的原因一

data/admin目录和js/目录下的文件没有可修改权限，设置权限为可修改或777即可。   

# 可能的原因二

opcache缓存加速器兼容上有问题。 修改 php.ini文件，关闭opcache加速。 ; zend_extension=php_opcache.dll   

# 可能的原因三

xcache缓存加速器兼容上有问题。 修改 php.ini文件，关闭xcache解决办
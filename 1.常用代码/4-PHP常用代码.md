1.寻找数组中是否存在某个值，并且返回下标。

```php
/**
$userdb = array(
0 => array(
        'uid' => 100,
        'name' => 'Sandra Shush',
        'url' => 'urlof100'
    ),
 
1 => array(
        'uid' => 5465,
        'name' => 'Stefanie Mcmohn',
        'pic_square' => 'urlof100'
    ),
 
2 => Array(
        'uid' => 40489,
        'name' => 'Michael',
        'pic_square' => 'urlof40489'
    )
    );

        $uID= array_column($userdb,'uid');
   
        var_dump(array_search(40489, $uID));//存在返回下标，不存在返回false
    */
```

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

2.多维数组所有key转为小写

```php
/**

PHP 多维数组所有key转为小写 || 大写

@param $array       //数据

@param int $case    //CASE_LOWER 小写、CASE_UPPER 大写

@return array
*/
function array_change_key_case_all(&$array, $case = CASE_LOWER)
{
$array = array_change_key_case($array, $case);
foreach ($array as $key => $value) {
    if (is_array($value)) {
        array_change_key_case_all($array[$key], $case);
    }
}

return $array;
}
```


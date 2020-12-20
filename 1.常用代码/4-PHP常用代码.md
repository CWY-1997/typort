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

2.导出csv文件

```php
public function  index()
    {
        ini_set('max_execution_time', '0');
        ini_set("memory_limit", 5048576000); // Byte 1000 兆，即 1G
        ini_set('display_errors', '1');
        error_reporting(0);
		//$allDate二维数组
        $str = "时间,接口名称,版本号,用户名,次数\n";
        $str = iconv('utf-8', 'gb2312', $str);
        foreach ($allDate as $item) {
            $question = iconv('utf-8', 'gb2312', $item['opening_time']);
            $a = iconv('utf-8', 'gb2312', $item['api']);
            $b = iconv('utf-8', 'gb2312', 'jde_v5');
            $c = iconv('utf-8', 'gb2312', 'ebs_user');
            $d = iconv('utf-8', 'gb2312', $item['sun']);
            $str .= $question . "," . $a . "," . $b . "," . $c . "," . $d . "\n";
        }
        $filename = '众信2020-11-12.csv';
        $this->export_filename($filename, $str);
    }
    public function export_filename($filename, $data)
    {
        header("Content-type:text/csv");
        header("Content-Disposition:attachment;filename=" . $filename);
        header('Cache-Control:must-revalidate,post-check=0,pre-check=0');
        header('Expires:0');
        header('Pragma:public');
        echo $data;
    }
```

3.PHP通过链接地址下载文件

```php
$path //保存路径
$s //下载地址
file_put_contents($path, $s);
```


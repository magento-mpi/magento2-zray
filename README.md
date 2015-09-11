Z-Ray-Magento
=============

This is an extension to add functionality to the Zend Server Z-Ray. It will result 
in additional tab(s) to be presented in the browser.

Detailed info on [Z-Ray wiki page](https://wiki.corp.x.com/display/MPI/Using+Magento2+Z-Ray+extension)

Installation
------------
First install latest version of [Zend Server](http://www.zend.com/en/products/server/downloads)

[Getting Started guide with Zend Sever](http://files.zend.com/help/Zend-Server-IBMi/content/getting_started_with_z-ray.htm)

Open your browser at http://localhost:10081/ZendServer/License/ and click "Update License" and enter the following details:

<pre><code>
Order Number: Magento
License Key: BGKG8050801G81FCD7F099D07A5B9651
</code></pre>

Create a directory named magento2 in Zend Server plugins directory, and add the contents of this repo within.

Example: (assuming default install directory for Zend Server)

```
    /usr/local/zend/var/plugins/magento2
```

NOTE: While the filename zray/zray.php is required, the file logo.png can be named whatever 
you desire and is specified from within the zray.php code as below.

```
    $zrayMagento->getZRay()->setMetadata(array(
        'logo' => __DIR__ . DIRECTORY_SEPARATOR . 'logo.png',
    ));
```

Edit zray/zray.php, set absolute path of your magento installation folder to MAGENTO_PATH constant

```
define('MAGENTO_PATH', '/var/www/html/magento2');
```

Open magento in browser and see zray panel at the bottom of the page 

More Info
------------

- [Z-Ray Documentation](https://github.com/zend-server-plugins/Documentation)
- [Zend.com](http://www.zend.com/en/products/server/z-ray)
- [Zend Server Online Help](http://files.zend.com/help/Zend-Server/zend-server.htm#z-ray_concept.htm)
- [Z-Ray extension for Magento1](https://github.com/zend-server-extensions/Z-Ray-Magento)

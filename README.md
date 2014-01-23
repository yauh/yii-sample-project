# Yii-Sample-Project

This is a simple example project with the PHP Yii-Framework. It is used as a sample project in the PHP-CI bootstrap.

Notes
=====

This project should serve as an example of how you can use Yii with the PHP enabled Jenkins-CI. Please note, that if you create your own projects that you need to take care of the following

### Path adjustments

If you create your webapp using 

```yiic webapp my-shiny-yii-project```

and you plan on using your project with the PHP-CI environment set up using these scripts, then you will need to adjust paths in three files. The reason is, that the Yii framework needs to be in the same place on all machines running the webapp.

Alternatively you can copy the yii folder to where your webapp expects it on the CI server.

First file

` ./my-shiny-yii-project/index.php`

Make sure to configure the location of `$yii` properly:

```$yii='/var/www/yii/framework/yii.php';```

Second comes the test-index file

` ./my-shiny-yii-project/index-test.php`

Make sure to configure the location of `$yiit` properly:

```$yiit='/var/www/yii/framework/yiit.php';```

And if you should use yiic let's not forget it either

` ./my-shiny-yii-project/protected/yiic.php`

Make sure to configure the location of `$yiic` properly:

```$yiic='/var/www/yii/framework/yiic.php';```

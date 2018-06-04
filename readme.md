<h2>ZN Framework Filesystem Package</h2>
<p>
Follow the steps below for installation and use.
</p>

<h3>Installation</h3>
<p>
You only need to run the following code for the installation.
</p>

```
composer require znframework/package-filesystem
```

<h3>Example Usage</h3>
<p>
Basic level usage is shown below.
</p>

<h3>Documentation For File Library</h3>
<p>
Click for <a href="https://docs.znframework.com/dosya-sistemi/dosya-kutuphanesi">documentation</a> of your library.
</p>

```php
<?php require 'vendor/autoload.php';

ZN\ZN::run();

File::write('example.txt', 'Example');

echo File::read('example.txt');
```

<h3>Documentation For Folder Library</h3>
<p>
Click for <a href="https://docs.znframework.com/dosya-sistemi/dizin-kutuphanesi">documentation</a> of your library.
</p>

```php
<?php require 'vendor/autoload.php';

ZN\ZN::run();

Folder::create('Example');

Folder::delete('Example');
```

<h3>Documentation For Upload Library</h3>
<p>
Click for <a href="https://docs.znframework.com/dosya-sistemi/yukleme-kutuphanesi">documentation</a> of your library.
</p>

```php
<?php require 'vendor/autoload.php';

ZN\ZN::run();

use ZN\Request\Post;

if( Post::uploadButton() )
{
    Upload::mimes('image/jpeg', 'image/png')->start('uploadFile', 'upload');

    output( Upload::error() );
}

echo Form::enctype('multipart')->open('form');
echo Form::file('uploadFile');
echo Form::submit('uploadButton', 'Upload');
echo Form::close();
```
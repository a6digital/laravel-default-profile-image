# Laravel Default Profile Image

Laravel package to create default profile image using name of user.


## Installation

Install using composer:

    composer require a6digital/laravel-default-profile-image

Edit `app/config/app.php` and add the `providers`

    'providers' => [
        'A6digital\Image\DefaultProfileImageServiceProvider'
    ]

    
## Basic Usage

To create a profile image just do

	$img = \DefaultProfileImage::create("Name Surname");
	\Storage::put("profile.png", $img->encode());

	
This will create a profile image that has 512px width&height using the first letters of name and surname.

![Profile Image](https://raw.githubusercontent.com/a6digital/laravel-default-profile-image/master/docs/images/profile.png)

## Advanced Usage

Create a white color text over black color background profile image that has 216px width&height.

	$img = \DefaultProfileImage::create("Name Surname", 256, '#000', '#FFF');
	\Storage::put("profile.png", $img->encode());

![Profile Small Image](https://raw.githubusercontent.com/a6digital/laravel-default-profile-image/master/docs/images/profile-small.png)
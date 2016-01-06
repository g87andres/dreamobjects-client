# arleslie\DreamObjects
Client for DreamObjects to work with AWS S3 API (for Laravel)

# Installation
In your `composer.json` add:
```
    "repository": [
        {
            "type": "vcs",
            "url": "https://github.com/arleslie/dreamobjects-client"
        }
    ],
```

In `config\filesystems.php` add the following under `'disks' => [`
```
        'dreamobjects' => [
            'driver' => 'dreamobjects',
            'key'    => 'WysSPV7bOuoyu-ZoS4LU',
            'secret' => 'zFBU7GnCmhmJZ-1zZ4kn3fjg4GM1rUyhAVPVVewz',
            'bucket' => 'billingserv-cdn'
        ],
```

Add the ServiceProvider: `arleslie\DreamObjects\ServiceProvider` to your `app.php`.

# Notes
This uses `league/flysystem-aws-s3-v2` and is not compatible with `league/flysystem-aws-s3-v3`.
A requirement of `league/flysystem-aws-s3-v3` will install the newest version of `aws/aws-sdk-php` which will cause this to package to fail.

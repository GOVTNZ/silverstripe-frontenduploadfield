# Frontend Uploadfield

Frontend UploadField for SilverStripe 4 with Dropzone.js.

## Installation

    composer require jamesbolitho/silverstripe-frontenduploadfield


## Field Configuation

To use this field use:

	use jamesbolitho\frontenduploadfield\UploadField;

Create your field as normal in your form:

	$upload1 = UploadField::create('Images', 'Images');


Set allowed file types:

	$upload1->getValidator()->setAllowedExtensions(array('jpg','jpeg','gif'));
	  

Set allowed max file size:

	$sizeMB = 1; // 1 MB
	$size = $sizeMB * 1024 * 1024; // 1 MB in bytes
	$upload1->getValidator()->setAllowedMaxFileSize($size);


Set to allow multiple file upload:

	$upload1->setIsMultiUpload(true);
	  

Set allowed number of files to upload:

	$upload1->setAllowedMaxFileNumber(5);


## ToDo's:

- Only been tested with images so needs further development and testing with files.
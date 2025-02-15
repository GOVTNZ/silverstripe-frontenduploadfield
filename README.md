# Frontend Uploadfield

Frontend UploadField for SilverStripe 4 with Dropzone.js.  jQuery is also required to be included in your front end template.

## Installation

    composer require jamesbolitho/silverstripe-frontenduploadfield


## Field Configuation

To use this field use:

	use jamesbolitho\frontenduploadfield\UploadField;


Create your field as normal in your form:

	$upload1 = UploadField::create('Images', 'Images');


Set upload folder:

	$upload1->setFolderName("Uploads/my-upload-folder/");


Set allowed file types:

	$upload1->getValidator()->setAllowedExtensions(array('jpg','jpeg','gif'));
	  

Set allowed max file size:

	$sizeMB = 1; // 1 MB
	$size = $sizeMB * 1024 * 1024; // 1 MB in bytes
	$upload1->getValidator()->setAllowedMaxFileSize($size);


Set to allow files to be removed from upload field:

	$upload1->setRemoveFiles(true);
	
*Please note that this also removes files from assets as well.*	
	

Set to allow multiple file upload:

	$upload1->setIsMultiUpload(true);
	  

Set allowed number of files to upload:

	$upload1->setAllowedMaxFileNumber(5);


Set timeout for the XHR requests in milliseconds:

	$upload1->setTimeout(30000);


## ToDo's:

- Add ability to alter more Dropzone settings programmatically through silverstripe i.e. chunk sizing etc.
- Add more icons for non image files e.g. pdf, word etc.
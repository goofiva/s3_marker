# s3_marker

Scripts using aws-cli to create, read, and wait for marker files.

## Commands

### s3\_is\_file
Return 0 if s3 file is found. Return 1 if file is not found.

	#s3_is_file $REGION $BUCKET $FILE_NAME

	s3_is_file us-west my-bucket my-file.txt
	
### s3\_mk\_bucket
Make a s3 bucket.
	
	#s3_mk_bucket $BUCKET
	
	s3_mk_bucket my-bucket
	
### s3\_rm\_file
Remove a s3 file.

	#s3_rm_file $BUCKET $FILE_NAME
	
	s3_rm_file my-bucket my-file.txt
	
### s3\_touch
Create an empty file in s3.
	
	#s3_touch $BUCKET $FILE_NAME
	
	s3_touch my-bucket my-file.txt
	
### s3\_wait\_for\_file
Wait for a file to appear in s3.
	
	#s3_wait_for_file $REGION $BUCKET $FILE_NAME $TIMEOUT_DURATION
	
	s3_wait_for_file us-west my-bucket my-file.txt 4000
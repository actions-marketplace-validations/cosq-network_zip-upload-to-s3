# Zip Upload to S3

This GitHub Action archives files and uploads them to an S3 bucket.

## Usage

To use this action, add the following to your workflow file:

```yaml
uses: your-username/zip-upload-to-s3@v1
with:
  inputFiles: '*.py'
  s3BucketName: 'my-bucket'
  zipFileName: 'my-zip-file.zip'
  s3ObjectKey: 'my-zip-file.zip'


The `inputFiles` input is required and specifies the files to archive. The files can be a glob pattern, such as `*.py`.

The `s3BucketName` input is also required and specifies the name of the S3 bucket.

The `zipFileName` input specifies the name of the Zip archive to be created.

The `s3ObjectKey` input specifies the S3 object key for the uploaded Zip archive.

The `addDirectoryPath` input is optional and specifies whether to include the directory path in the zipped archive. The default value is `false`.

## Outputs

This action does not have any outputs.

## Example

The following example archives all Python files in the current directory and uploads them to an S3 bucket named `my-bucket` with the object key `my-zip-file.zip`:

yaml
uses: your-username/zip-upload-to-s3@v1
with:
  inputFiles: '*.py'
  s3BucketName: 'my-bucket'
  zipFileName: 'my-zip-file.zip'
```

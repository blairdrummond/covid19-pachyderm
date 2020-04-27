# covid19-pachyderm

1. Create your docker image
   - Go into the docker folder and build the image
   - Make sure that the pipeline file is updated to reference that version

2. Create the `seeds` repo
   - Go into the seeds folder
   - Generate the `seeds.json` file (output is 1 json per line)
   - Upload the `seeds.json` to Pachyderm
 
3. Upload your data
   - Go into the data folder and use --data and --branch
   - Make sure to reference the branch when you run your pipeline.

4. Create your pipeline!
   - Read through the yml file to make sure it's ok.
   - Make sure that the data branch is correct
   - Make sure the image version you're using is correct
   - Run `pachctl create pipeline -f wifr-pipeline.yml`


Viola!

See the status with

```sh
pachctl list pipeline
pachctl list job
```

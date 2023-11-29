## Learnings

- Multistage images is one of the best way to reduce the image size.
- `--target` option can be used to compile till a particular stage.
- Adding `DOCKER_BUILDKIT=0` before docker build command will make sure only the images which are useful for building the final target will be processed.
- It is very important to compile the code `statically` without any dynamic links.
- Dyanmic links can be checked by using `$ ldd <compiled_file_name>`.
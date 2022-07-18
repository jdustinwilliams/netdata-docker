I had to follow this to make fix Docker permissions problem: https://github.com/netdata/netdata/issues/10793#issuecomment-802146027

>  @ilyam8 @Ferroin So yes the solution is just to have created the folder before. This is what i did :
> mkdir ${CONFIG_DIR}/netdata
> mkdir ${CONFIG_DIR}/netdata/{cache,config,lib}
> chmod -R 775 ${CONFIG_DIR}/netdata
> sudo chown -R 201:201 ${CONFIG_DIR}/netdata
>
> then you start your docker-compose and all is ok without any errors !

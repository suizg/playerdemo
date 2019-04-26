OUT_APP		 = ../bin/ffdemo
IN_FILE      = main.c
INCLUDE_PATH_FFMPEG = /usr/local/Cellar/ffmpeg/4.1.1/include/
INCLUDE_PATH_SDL = /usr/local/Cellar/sdl2/2.0.9_1/include/ 
INCLUDE = -I$(INCLUDE_PATH_FFMPEG)libavutil/ -I$(INCLUDE_PATH_FFMPEG)libavdevice/ \
			-I$(INCLUDE_PATH_FFMPEG)libavcodec/ -I$(INCLUDE_PATH_FFMPEG)libswresample \
			-I$(INCLUDE_PATH_FFMPEG)libavfilter/ -I$(INCLUDE_PATH_FFMPEG)libavformat \
			-I$(INCLUDE_PATH_FFMPEG)libswscale/ -I$(INCLUDE_PATH_SDL)SDL2/
 
FFMPEG_LIBS = -lavformat -lavutil -lavdevice -lavcodec -lswresample -lavfilter -lswscale
SDL_LIBS	= -lSDL2 
LIBS		= $(FFMPEG_LIBS) $(SDL_LIBS)
 
COMPILE_OPTS = $(INCLUDE)
C 			 = c
OBJ 		 = o
C_COMPILER   = cc
C_FLAGS 	 = $(COMPILE_OPTS) $(CPPFLAGS) $(CFLAGS)
 
LINK 		 = cc $(IN_FILE) -o 
LINK_OPTS    = -lz -lm  -lpthread
LINK_OBJ	 = main.c
 
.$(C).$(OBJ):
	$(C_COMPILER) -c $(C_FLAGS) $<
 
 
$(OUT_APP): $(LINK_OBJ)
	$(LINK)$@  $(LIBS) $(LINK_OPTS)
 
clean:
		-rm -rf *.$(OBJ) $(OUT_APP) core *.core *~ include/*~

CC	=	g++

DIRPATH = ../../games

RM	=	rm -f

SRC	=	OpenGl.cpp \
		Shader.cpp \
		DDS.cpp \
		Font.cpp \
		Mesh.cpp \
		Model.cpp \

NAME	=	lib_arcade_opengl.so

OBJ = $(SRC:.cpp=.o)

PIC	=	-fPIC

SHARED	=	-shared

CXXFLAGS = 	-std=c++14 -fPIC -W -Wall -Werror -Wextra -rdynamic -lGLEW -lGLU -lGL -lglfw3 -lXext -ldl -lrt -lm -lX11 -lpthread -lXrandr -lXinerama -lXi -lXxf86vm -lXcursor -lassimp -lSOIL -fPIC

CPPFLAGS = -I./../../Include/

MV	=	mv

all: $(NAME)

$(NAME):
	$(CC) $(PIC) -c $(SRC) $(CPPFLAGS) $(CXXFLAGS)
	$(CC) $(SHARED) $(PIC) -o $(NAME) $(OBJ) $(CPPFLAGS) $(CXXFLAGS)

clean:
	$(RM) $(OBJ)

fclean: clean
	$(RM) $(NAME)

re:	fclean all

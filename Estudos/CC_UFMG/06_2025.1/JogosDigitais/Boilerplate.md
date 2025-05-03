
# CMake:
```CMake
cmake_minimum_required(VERSION 3.26)  
# Configurando o padrão c++  
set(CMAKE_CXX_STANDARD 17)  
  
# Configurando o nome e executável do projeto  
set(PROJECT_NAME "project_name")  
project(${PROJECT_NAME})  
  
find_package(SDL2 2.32.2 EXACT REQUIRED)  
add_executable(${PROJECT_NAME} main.cpp)  
target_link_libraries(${PROJECT_NAME} ${SDL2_LIBRARIES})
```

# Main:
```C++
#include <SDL.h>

int main(int argc, char* args[]){
	
	int init_code = SDL_Init(SDL_INIT_VIDEO);
	  
	if (init_code < 0) {  
	    SDL_Log("Initialization error!");  
	    return -1;  
	}  
	  
	SDL_Window* window = SDL_CreateWindow(  
	    "SDL2 Window",  
	    SDL_WINDOWPOS_CENTERED,  
	    SDL_WINDOWPOS_CENTERED,  
	    500, 500,  
	    SDL_WINDOW_SHOWN  
	    );  
	  
	if (window == nullptr) {  
	    const char* error_message = SDL_GetError();  
	    SDL_Log(error_message);  
	    return -1;  
	}
	
	SDL_Renderer* renderer = SDL_CreateRenderer(  
	    window,  
	    -1,  
	    SDL_RENDERER_ACCELERATED |  
	    SDL_RENDERER_PRESENTVSYNC);  
	  
	if (renderer == nullptr) {  
	    const char* error_message = SDL_GetError();  
	    SDL_Log(error_message);  
	    return -1;  
	}
	
	bool running = true;  
	while (running) {  
	    SDL_Event event;  
	    while (SDL_PollEvent(&event)) {  
	        if (event.type == SDL_QUIT)  
	            running = false;  
	    }
	}
	
	SDL_DestroyRenderer(renderer);  
    SDL_DestroyWindow(window);  
    SDL_Quit();  
    
    return 0;  
}
```

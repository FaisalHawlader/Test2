# CPPND: Capstone Snake Game Example
* Compared to the starter code, many additional features were added to upgrade the game using advanced object-oriented programming (Classes & Inheritance), dynamic memory management (Smart Pointers), and Concurrency (Multi threads & mutex locks) techniques.
* Three snakes are in the game
* There are two players to compete against each other, and you need to use two hands to control the left snake command: w, a, s, d (Up, left, down, right)
and right snake command: i, j, k, l (up, left, down, right)
* Blue Snake is Left, Green Snake is Right, Red Snake is Viper(Cannot be touched, if you touch then game over), Yellow ones are food.

## Dependencies for Running Locally
* cmake >= 3.7
  * All OSes: [click here for installation instructions](https://cmake.org/install/)
* make >= 4.1 (Linux, Mac), 3.81 (Windows)
  * Linux: make is installed by default on most Linux distros
  * Mac: [install Xcode command line tools to get make](https://developer.apple.com/xcode/features/)
  * Windows: [Click here for installation instructions](http://gnuwin32.sourceforge.net/packages/make.htm)
* SDL2 >= 2.0
  * All installation instructions can be found [here](https://wiki.libsdl.org/Installation)
  * Note that for Linux, an `apt` or `apt-get` installation is preferred to building from source.
* gcc/g++ >= 5.4
  * Linux: gcc / g++ is installed by default on most Linux distros
  * Mac: same deal as make - [install Xcode command line tools](https://developer.apple.com/xcode/features/)
  * Windows: recommend using [MinGW](http://www.mingw.org/)

## Basic Build Instructions

1. Clone this repo/navigate to the root directory
2. Make a build directory in the top level directory: `mkdir build && cd build`
3. Compile: `cmake .. && make`
4. Run it: `./SnakeGame`.

## How To Play Game 
* Use keyboard arrows to move your snake
* Blue Snake is Left, command: w, a, s, d (Up, left, down, right)
* Green Snake is Right, command: i, j, k, l (up, left, down, right)
* Red Snake is Viper(Cannot be touched, if you touch then game over), 
* To get points eat food, Yellow ones are food.
* When your snake eat food, the speed of the game and body of all snakes in the game will increase.

## Rubric

__README (All Rubric Points REQUIRED)__

|DONE | CRITERIA | MEETS SPECIFICATIONS|
|-- | -- | --|
| :heavy_check_mark: | A README with instructions is included with the project |The README is included with the project and has instructions for building/running the project. <br />If any additional libraries are needed to run the project, these are indicated with cross-platform installation instructions. <br />You can submit your writeup as markdown or pdf.|
| :heavy_check_mark: | The README indicates which project is chosen. | The README describes the project you have built. <br />The README also indicates the file and class structure, along with the expected behavior or output of the program. |
| :heavy_check_mark: | The README includes information about each rubric point addressed. | The README indicates which rubric points are addressed. The README also indicates where in the code (i.e. files and line numbers) that the rubric points are addressed. |

__Compiling and Testing (All Rubric Points REQUIRED)__

|DONE | CRITERIA | MEETS SPECIFICATIONS|
|-- | -- | --|
| :heavy_check_mark: | The submission must compile and run. | The project code must compile and run without errors. <br />We strongly recommend using `cmake` and `make`, as provided in the starter repos. If you choose another build system, the code must compile on any reviewer platform. |

__Loops, Functions, I/O__

|DONE | CRITERIA | MEETS SPECIFICATIONS|
|-- | -- | --|
| :heavy_check_mark: | The project demonstrates an understanding of C++ functions and control structures.| A variety of control structures are used in the project. <br />The project code is clearly organized into functions.|
|  | The project reads data from a file and process the data, or the program writes data to a file. | The project reads data from an external file or writes data to a file as part of the necessary operation of the program.|
| :heavy_check_mark: | The project accepts user input and processes the input.|The project accepts input from a user as part of the necessary operation of the program.|

__Object Oriented Programming__

|DONE | CRITERIA | MEETS SPECIFICATIONS|
|-- | -- | --|
| :heavy_check_mark: | The project uses Object Oriented Programming techniques. | The project code is organized into classes with class attributes to hold the data, and class methods to perform tasks. |
| :heavy_check_mark: | Classes use appropriate access specifiers for class members. | All class data members are explicitly specified as public, protected, or private.|
| :heavy_check_mark: | Class constructors utilize member initialization lists. | All class members that are set to argument values are initialized through member initialization lists.|
| :heavy_check_mark: | Classes abstract implementation details from their interfaces. | All class member functions document their effects, either through function names, comments, or formal documentation. Member functions do not change program state in undocumented ways.|
| :heavy_check_mark: | Classes encapsulate behavior. | Appropriate data and functions are grouped into classes. Member data that is subject to an invariant is hidden from the user. State is accessed via member functions.|
| :heavy_check_mark: | Classes follow an appropriate inheritance hierarchy. | Inheritance hierarchies are logical. Composition is used instead of inheritance when appropriate. Abstract classes are composed of pure virtual functions. Override functions are specified.|
| :heavy_check_mark: | Overloaded functions allow the same function to operate on different parameters. | One function is overloaded with different signatures for the same function name. |
| :heavy_check_mark:| Derived class functions override virtual base class functions. |One member function in an inherited class overrides a virtual base class member function.|
| :heavy_check_mark: | Templates generalize functions in the project. | One function is declared with a template that allows it to accept a generic parameter.|

__Memory Management__

|DONE | CRITERIA | MEETS SPECIFICATIONS|
|-- | -- | --|
| :heavy_check_mark: | The project makes use of references in function declarations. | At least two variables are defined as references, or two functions use pass-by-reference in the project code.| game.cpp (Line 128), snake.h (Line 41), game.h (Line 20, 33), controller.h (Line 8-11) |
|  | The project uses destructors appropriately. | At least one class that uses unmanaged dynamically allocated memory, along with any class that otherwise needs to modify state upon the termination of an object, uses a destructor. |
|  | The project uses scope / Resource Acquisition Is Initialization (RAII) where appropriate. | The project follows the Resource Acquisition Is Initialization pattern where appropriate, by allocating objects at compile-time, initializing objects when they are declared, and utilizing scope to ensure their automatic destruction.|
| :heavy_check_mark: | The project follows the Rule of 5. | For all classes, if any one of the copy constructor, copy assignment operator, move constructor, move assignment operator, and destructor are defined, then all of these functions are defined.|
| :heavy_check_mark: | The project uses move semantics to move data, instead of copying it, where possible. | For classes with move constructors, the project returns objects of that class by value, and relies on the move constructor, instead of copying the object. |
| :heavy_check_mark: | The project uses smart pointers instead of raw pointers. | The project uses at least one smart pointer: unique_ptr, shared_ptr, or weak_ptr. The project does not use raw pointers.|

__Concurrency__

|DONE | CRITERIA | MEETS SPECIFICATIONS|
|-- | -- | --|
| :heavy_check_mark: | The project uses multithreading. | The project uses multiple threads in the execution.| game.cpp (Line 79) |
|  | A promise and future is used in the project. | A promise and future is used to pass data from a worker thread to a parent thread in the project code.|
|  | A mutex or lock is used in the project. | A mutex or lock (e.g. std::lock_guard or `std::unique_lock) is used to protect data that is shared across multiple threads in the project code.|
|  | A condition variable is used in the project. | A std::condition_variable is used in the project code to synchronize thread execution.|

# InfiniteDecks
Allows to
- Create more than 4 decks per profile
- Keep decks for Soku2 characters when disabling Soku2
- Give a name to decks
- Copy decks
- Use a randomized deck
- Use no deck
- Create a deck with less than 20 cards, that will be filled to 20 cards at each game with random cards
- Play outdoors as Remilia (in netplay, only works when hosting and if P2 doesn't play Remilia or has a parasol)

The mod works even when your opponent doesn't use it.
On their end, you will select the "random" deck.

# Build
Requires CMake, git and the VisualStudio compiler (MSVC).
Both git and cmake needs to be in the PATH environment variable.

All the following commands are to be run inside the visual studio 32bits compiler
command prompt (called `x86 Native Tools Command Prompt for VS 20XX` in the start menu), unless stated otherwise.

## Initialization
First go inside the folder you want the repository to be in.
In this example it will be C:\Users\PinkySmile\SokuProjects but remember to replace this
with the path for your machine. If you don't want to type the full path, you can drag and
drop the folder onto the console.

`cd C:\Users\PinkySmile\SokuProjects`

Now let's download the repository and initialize it for the first time
```
git clone https://github.com/SokuDev/InfiniteDecks
cd InfiniteDecks
git submodule init
git submodule update
mkdir build
cd build
cmake .. -G "NMake Makefiles" -DCMAKE_BUILD_TYPE=Debug
```
Note that if you want to build in Release, you should replace `-DCMAKE_BUILD_TYPE=Debug` with `-DCMAKE_BUILD_TYPE=Release`.

## Compiling
Now, to build the mod, go to the build directory (if you did the previous step you already are)
`cd C:\Users\PinkySmile\SokuProjects\InfiniteDecks\build` and invoke the compiler by running `nmake`.

You should find the resulting InfiniteDecks.dll mod inside the build folder that can be to SWRSToys.ini.
In my case, I would add this line to it `InfiniteDecks=C:/Users/PinkySmile/SokuProjects/InfiniteDecks/build/InfiniteDecks.dll`.
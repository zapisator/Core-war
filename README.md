# CoreWar

Проект CoreWar Школы 21 от Сбербанк

Our company was bored at first to even begin doing the project. They said it was too easy and not interesting. I said I would take care of that part of the issue. Before we started, I ordered the book Alaint I. Holub, "C+ C++: Programming With Objects in C and C++. From there I took a lot of ideas: an abstract class or interface, the idea of a garbage collector (not really a garbage collector, but a class that makes sure it removes all the resources it requests), some design patterns, and a way to write classes more clearly. Although, of course, the restrictions the school imposed on the code format (no more than 5 functions in a file). Not every file managed to implement these ideas, but I tried very hard. Time passed, and we still did not start the project. I set out to learn how to properly write a compiler. Beforehand I described our compiler using the Extended Backus-Naur form. Little by little we got to work. I was also interested in articles on related topics. In every way I didn't let my colleagues get bored. And here is what we had.

The goal of the project is to write an assembler for the game CoreWar, as well as a virtual machine to run the game. For more information see the file [sbj/11_corewar.en.pdf](https://github.com/TesenDesk/CoreWar/blob/working_flow/sbj/11_corewar.en.pdf).

At the moment it is done:
- [x] Assembler (100% complete)
- [x] Virtual machine (100% complete)
- [x] Visualization (100% complete)

To run the program, first do `make`.
<details>
 <summary>Additional compilation options</summary>

 <code>make d</code> or <code>make debug</code> or <code>make DEBUGMODE=1</code> - build project in debug mode

 <code>make rd</code> or <code>make redebug</code> or <code>make re DEBUGMODE=1</code> - force rebuild project in debug mode (all files will be rebuilt again)
</details>

## Assembler

To run the assembler, use the command
```
./asm FILENAME
```
where `FILENAME` is the `.s` format file containing your champion's source code. The program will convert it to a `.cor` file, which is necessary for the game. You can learn more about these files in the file [sbj/11_corewar.en.pdf](https://github.com/TesenDesk/CoreWar/blob/working_flow/sbj/11_corewar.en.pdf).

## Virtual machine

To start the virtual machine, run the command
```
./corewar [-d N -v N] [[-n number] <champion1.cor> <...>]
```
where `champion1.cor` is the champion file in the `.cor` float. There can be from one to four such files (by default)

### Additional virtual machine flags:

<ul>
 <li><code>-n N, -number N </code> - set player number, where N is a number from 1 to 4 (when playing with 4 players). The default is a sequential number</li>
 <li><code>-d N, -dump N</code> - stop the game after N cycles and dump the memory</li>
 <li><code>-v N</code> - switch print level, where N:
 <ul>
  <li>0 - Show only candidate submission and victory message</li>
  <li>1 - Show lives</li>
  <li>2 - Show cycles</li>
  <li>4 - Show operations</li>
  <li>8 - Show death</li>
 </ul>
 (Default is 0)
</li>
 <li><code>-curses</code> - run in Ncurses mode (visualization)</li>
</ul>

## Screenshots

![img1](https://github.com/TesenDesk/CoreWar/raw/working_flow/images/vm_visual_4.png)

This project was done

- cmissy [@nikkyniknikita](https://gitlab.com/nikkyniknikita)
- ftothmur [@zapisator](https://gitlab.com/zapisator)
- jjerde [@tesen708](https://gitlab.com/tesen708)
- mstygg [@ikira](https://gitlab.com/ikira)

2020 Moscow, Russia


# Spongedown

```bob
                 _____________
 +---------+     \            \        +------------+
 | md+bob  |----->) spongedown )------>| html + svg |
 +---------+     /____________/        +------------+
```

Spongedown converts markdown to html with support for 
[svgbob diagrams](https://github.com/ivanceras/svgbobrus)



|  中文处理 | Data  |   CJK      |
|-----------|-------|------------|
|**Table**  | `are` | supported  |
| as        | well  |            |

The next `code block` fenced with `bob` will be rendered into an svg

```bob

                                     .--> Base::Class::Derived_A
                                    /
            .-.                    .----> Base::Class::Derived_B    
           (x1y)----.             /           \     .----------------------.
            '-'      \           /             .---->\ Base::Class::Derived \
        Alice         \         /               \     \----------------------\
            \          \       /            ____ '---->\ Base::Class::Derived \
             \          \     /            /    \       '----------------------'
              \          \   .----------->( SVG  )                         
               \          V /              \____/
                \    .-----------.              
                 '->(    Bob      )
                     '-----------'
                       /  \ \ \
                      '    \ \ \  
                      |     \ \ \
                      .      \ \ '--- The::Latest
                     /|       \ \      \     +-----------------------+
                 Foo  '        \ \      '--->| The::Latest::Greatest |
         ________    /|         \ \          +-----------------------+
        /  Bar  /<--' '          \ '- I::Am::Running::Out::Of::Ideas
       '-------'     /|           \
                 Baz  '            \      .-----------.
                     /              '----/ Last::One /
               Quux V                   '-----------'

+----------------------+
|                      |
|       中文处理       |
|       12345678       |
|                      |
+----------------------+

             .---.  .---. .---.  .---.    .---.  .---.
    OS API   '---'  '---' '---'  '---'    '---'  '---'
               |      |     |      |        |      |
               v      v     |      v        |      v
             .------------. | .-----------. |  .-----.
             |  文件系统  | | |   调度器  | |  | MMU |
             '------------' | '-----------' |  '-----'
                    |       |      |        |
                    v       |      |        v
                 .----.     |      |    .---------.
                 | IO |<----'      |    |   网络  |
                 '----'            |    '---------'
                    |              |         |
                    v              v         v
             .---------------------------------------.
             |              硬件抽象层               |
             '---------------------------------------'

```


## Improvements in svgbob
- Generated SVG size is now optimized
- [CJK is now supported](https://github.com/ivanceras/svgbobrus/pull/7)
- Supports a wide array of [diagram element combinations](https://ivanceras.github.io/svgbobrus/)



Supports normal code blocks too.


```rust
fn main(){
    println!("Hello world!");
}
```

### Links
* [Spongedown repo](https://github.com/ivanceras/spongedown)
* [Svgbob demo](https://ivanceras.github.io/svgbobrus/) 
    - [repo](https://github.com/ivanceras/svgbobrus)
* [Svgbob in hackernews](https://news.ycombinator.com/item?id=12621680)
* [pulldown-cmark](https://github.com/google/pulldown-cmark)

> Speech bubbles in ascii
> and more..

```bob

     ________________________________________________
   ,'                                                `.
  /    Note that the ascii diagrams is well aligned    \
 |   if you are using monospaced terminal based         |
 |  text editors such as vim, nano.                     |
 |  Rendering the text in html `<pre><code>`            |
 |  and in graphical text editors                       |
 |  will not align very well,                           |
 |  since the CJK characters is occupying only ~1.5     |
  \   of space instead of 2.                           /
   `.______________________________  ________________,'
                            _______\ \____________________
                          ,'                              `.
                         /                                  \
                        |        That's all folks!           |
                         \                                  /
                          `._______  _____________________,'
                                  /,'
                                 /'
     .--._.-----._.--._.----.
    .' \  (`._   (_)     _   \
  .'    |  '._)         (_)  |
  \ _.')\      .----..---.   /
  |(_.'  |    /    .-\-.  \  |
  \     0|    |   ( O| O) | o|
   |  _  |  .--.____.'._.-.  |
   \ (_) | o         -` .-`  |
    |    \   |`-._ _ _ _ _\ /
    \    |   |  `. |_||_|   |
    | o  |    \_      \     |     -.   .-.
    |.-.  \     `--..-'   O |     `.`-' .'
  _.'  .' |     `-.-'      /-.__   ' .-'
.' `-.' '.|='=.='=.='=.='=|._/_ `-'.'
`-._  `.  |________/\_____|    `-.'
   .'   ).| '=' '='\/ '=' |
   `._.'  '---------------'
           //___\   //___\
             ||       ||
             ||_.-.   ||_.-.
            (_.--__) (_.--__)

```

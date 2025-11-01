+++
date = '2025-11-01T16:49:20+01:00'
draft = false
title = 'October 2025'
+++

The most well documented month of my life (so far). Sometimes it's hard to see how much you progress,
 both as a developer or as a person, journaling is one of the solutions that helps you take a step back
 and look at what you did, how you did it and what you would change.

# More than I could ever expect

October was an incredible month of my life, both personal and professional. Of course this blog will focus on the professional
 side of my life, due to the nature of the blog being public. October was my last month at reMarkable and what a 
 fantastic journey it was, cannot thank enough the mentorship and friendships I received during my tenure. I know some of them
 will end up reading this blog and when you do I want you to internalize how amazing you are.

Now to the point. My main goal with writing this simple blogpost today is to unblock myself, I have wanted to start my own blog
 for a very long time and while I am full of ideas, I've revised the current ideas I have in the pipeline and they are all, in
 my own opinion in my own blog, very good. However due to the pressure of doing something that I've never done before and 
 sucking at it, which we all feel, I have postponed writing the first technical piece. So while I want to follow the advice
 given in [How To Write More Blog Posts](https://kristoff.it/blog/write-more/), I cannot yet as I first need to feel comfortable writing
 something down for others to read.

I am fully aware of my own shortcoming as a writer, but I must start somewhere.

# Stuff 

This is it, this is the stuff I've worked on this month:

## Unity

I've never written a single line of C# in my entire life but in my next job I'll have to and most of all I'll get to read a lot
 of C#. One of my new coworkers recommended in a joking manner to learn C# via Unity. And so I did!

Well not really, what I learned while doing a few tutorials in Unity is how valuable a good starting point is. Unity has very many
 tutorials but a lot of them depend on other tutorials or are not updated to the latest version of Unity. So to go through these
 several tutorials I had to install 3 different versions of Unity (which takes quite a lot of time). While installing the different
 versions I started to grow more interested in other topics and so I ended up dropping.

## C++ Starting Template Project

I love C++, I hate C++. C++ is one of my favorite languages to develop in but the ecosystem itself is very lacking compared to more
 modern languages such as Rust or Zig or Python or JS etc. Whenever I want to start a new project nowadays, I never choose C++. 
 While I love writing the language and using it, just setting up a project always takes all the joy away from working on something new.
 Which is why I created my own [C++ Template project](https://github.com/nunokaeru/template-cpp), it most likely won't fit your needs, but 
 it fits mine so try it out.

I also finally spent some time learning how to set up the Clang compiler on Linux... Should push a patch to the repo to support linux clang.
 It's very easy to fall into the trap to think that something should be easy, in reality most things are, obtaining the missing context for 
 why they don't seem to work, well that can be a pain and very often C++ tooling will inflict that pain on you. NOTE: installing `clang` does
 not install `clang-find-deps` by default, maybe next time I'll remember, or I'll just write a blogpost or template with that written down.

## Task Tracker Terminal UI

This is a simple Go project to keep track of tasks. Everyone has done a similar project in their lifetimes, the fun part about this one
is how I've learned about Terminal UIs and the frameworks that exist for many languages, like the original [ncurses](https://github.com/mirror/ncurses) in C, or Rust's [ratatui](https://ratatui.rs/), or Zig's [Zaxis](https://github.com/rockorager/libvaxis), or the one I ended up using
in Go [gocui](https://github.com/jroimartin/gocui).

Also another cool library I used is [sqlc](https://github.com/sqlc-dev/sqlc), what a wonderful [library](https://conroy.org/introducing-sqlc) to not use ORMs but instead just write SQL yourself and have a generator that allows you to use it in your app.

## This blog

Also written during October, was this very own blog. Well "written", more like choose the technologies to use. I was inbetween two choices, [Zine](https://github.com/kristoff-it/zine)
 or [Hugo](https://github.com/gohugoio/hugo). I chose Hugo just for the maturity of the tool, it's very well known as a static website generator and
 is also quite nice to use. I chose to use a template called [Rusty Typewriter](https://github.com/math-queiroz/rusty-typewriter) but unfortunately as it always happens I ended up having to rewrite a lot of it according to my own taste (More things to come!).

The bigger challenge on getting my blog up and running was on how to host it. Still have a lot to learn in this area but I ended up choosing this
 static website solution with Hugo and Github Pages, simple, cheap and available.

## Rustlings

What an amazing project [Rustlings](https://github.com/rust-lang/rustlings). My new job will also have a Rust component! I don't know Rust, so
 so Rustlings is a great place to start learning. I found it so funny that in Rust functions can just steal yo shit, unlike in C++ where you either
 copy a value or pass a reference, in Rust instead of copying the value the function just steals yo shit.

```rust
    fn bye_bye(vec: Vec<i32>) -> Vec<i32> {
        let mut vec = vec;
        vec.push(88);
        vec
    }

    fn oh_no() {
        let vec0 = vec![22, 44, 66];
        let vec1 = fill_vec(vec0); // good bye vec0, it was nice knowing ya
        
        println!(vec0[0]) // BOOM
    }
```

## Unfuckify

What an amazing project, the original project [Unfuckify](https://github.com/sandsmark/unfuckify) had one simple goal: remove auto from C++ codebases.
 It does not sound like the heftiest goal of all time but due to how behind C++ tooling is compared to other languages, something like determining which type a variable is (which the compiler already knows) becomes and incredible task. There were lots of things to learn from this project, 
 llvm / clang / posix / using C from C++ and so much more.

One of things I attempted to learn in this project was how long just reading a file could take with many different C and C++ approaches, immortalized
 in this [branch](https://github.com/nunokaeru/auto-b-gone/tree/check-auto-performance-experiment) and how finicky micro-benchmarking can be. I also came out of it with a takeaway about microbenchmarking, which is: "just do it". The results that I obtained were very poor in terms of being able to make a decision on standard library (C and C++) approaches but I managed to write some terrible code and so I could very clearly throw my own code out of the window. Tool used: [Hyperfine](https://github.com/sharkdp/hyperfine), never got [poop](https://github.com/andrewrk/poop) to work.

# Talks

There have also been several amazing talks I've listened to during this month mostly about:

- Data Oriented Design, starting from [Mike Acton's talk](https://www.youtube.com/watch?v=rX0ItVEVjHc) and other talks that follow in it's footsteps like [Pratical DOD](https://www.youtube.com/watch?v=IroPQ150F6c).
- The list of talks called Back to Basics from CppCon. One of them being [API Design](https://youtu.be/zL-vn_pGGgY?si=eLnO5GB80LeV_ezo).

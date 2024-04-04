## Home repository of JDemetra+ v 3.x R ecosystem
<!--

**Here are some ideas to get you started:**

🙋‍♀️ A short introduction - what is your organization all about?
🌈 Contribution guidelines - how can the community get involved?
👩‍💻 Useful resources - where can the community find your docs? Is there anything else the community should know?
🍿 Fun facts - what does your team eat for breakfast?
🧙 Remember, you can do mighty things with the power of [Markdown](https://docs.github.com/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)
-->

### Structure

```mermaid
flowchart TB
    subgraph rjd3toolkit_depends ["Packages dépendants de rjd3toolkit"]
        direction TB


        subgraph rjd3_other[" "]
            rjd3bench
            rjd3revisions
            rjd3nowcasting
        end
        
        subgraph rjd3x13_tramo[" "]
            rjd3x13
            rjd3tramoseats
        end

        rjd3providers --> rjdemetra3
        rjd3x13_tramo --> rjdemetra3

        rjd3x13_tramo --> ggdemetra3
        rjd3highfreq --> ggdemetra3
        rjd3x11plus --> ggdemetra3
        rjd3filters --> ggdemetra3
        
        rjd3filters --> rjd3x11plus
        rjd3sts --> rjd3highfreq
        rjd3highfreq --> rjd3stl

    end

    rjd3toolkit --> rjd3toolkit_depends

  click rjd3toolkit "https://github.com/rjdemetra/rjd3toolkit" _blank
  click rjd3nowcasting "https://github.com/rjdemetra/rjd3nowcasting" _blank
  click rjd3stl "https://github.com/rjdemetra/rjd3stl" _blank
  click rjd3highfreq "https://github.com/rjdemetra/rjd3highfreq" _blank
  click rjd3sts "https://github.com/rjdemetra/rjd3sts" _blank
  click rjd3x11plus "https://github.com/rjdemetra/rjd3x11plus" _blank
  click rjd3filters "https://github.com/rjdemetra/rjd3filters" _blank
  click rjd3providers "https://github.com/rjdemetra/rjd3providers" _blank
  click rjdemetra3 "https://github.com/rjdemetra/rjdemetra3" _blank
  click rjd3x13 "https://github.com/rjdemetra/rjd3x13" _blank
  click rjd3tramoseats "https://github.com/rjdemetra/rjd3tramoseats" _blank
  click rjd3bench "https://github.com/rjdemetra/rjd3bench" _blank
  click rjd3revisions "https://github.com/rjdemetra/rjd3revisions" _blank
  click ggdemetra3 "https://github.com/AQLT/ggdemetra3" _blank
```

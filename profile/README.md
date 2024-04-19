## Home repository of JDemetra+ v 3.x R ecosystem
<!--

**Here are some ideas to get you started:**

🙋‍♀️ A short introduction - what is your organization all about?
🌈 Contribution guidelines - how can the community get involved?
👩‍💻 Useful resources - where can the community find your docs? Is there anything else the community should know?
🍿 Fun facts - what does your team eat for breakfast?
🧙 Remember, you can do mighty things with the power of [Markdown](https://docs.github.com/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)
-->

rjdemetra is an organization dedicated to creating **R packages giving access to JDemetra+ version 3.x algorithms**. Its main contributors come from National Bank of Belgium (NBB), Deutsche Bundesbank (BBk) and the french NSI (Insee).

[JDemetra+](https://github.com/jdemetra) is a versatile time series analysis software, whose core routines are written in Java and also accessible via a Graphical User Interface.

[[Documentation]](https://jdemetra-new-documentation.netlify.app/) | [[Blog]](https://jdemetra-universe-blog.netlify.app/)

Installation procedure and basic examples are given in the readme file of each package. Their documentation is available via GitHub pages.

List of R packages available on this page: 

**Seasonal adjustment**

    - rjd3x13 (Reg-Arima + x11 based decomposition)

    - rjd3tramoseats (Tramo+ AMB decomposition with SEATS)
    
    - rjd3stl (Local regression)

    - rjd3highfreq (extended airline model + extended AMB decomposition)
    
    - rjd3x11plus (extended X11)
    
    - rjd3sts (basic structural models
    
**Benchmarking, Temporal disaggregation, Revision analysis and Nowcasting**

    - rjd3bench (benchmarking and temporal disaggregation)
    
    - rjd3revisions (revision analysis)
    
    - rjd3nowcasting(nowcasting)
    
**Filtering and trend estimation**

    - rjd3filters
    
    - rjd3x11plus (local polynomials)

**General purpose tools**
    
    - rjd3toolkit (specifications, tests, regressors)
    
    - rjd3sts (state space framework)
    
    - rjd3filters (generating moving averages)

  
**Tools related to JDemetra+ Graphical User Interface**
    
    - rjd3providers (input data)
    
    - rjdemetra3 (workspace wrangling)


### Dependency relations 

```mermaid
flowchart TB
    subgraph rjd3toolkit_depends ["All packages depend on rjd3toolkit"]
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

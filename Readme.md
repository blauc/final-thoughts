---
title: Some thoughts on the road
tags: Talk, FEP
description: 
slideOptions:
  theme: white
---

<style>
.reveal { font-size: 30px; }
.reveal section img { background:none; border:none; 
    -shadow:none; }
</style>

# Some thoughts on the road



---

## I Pipelines for cryo-EM refinement

---

### It just works?



---



```graphviz
digraph G {
    orientation=h
    splines= ortho
    ranksep= 0.2
    fontname= "Sans-Serif"
    fontsize= 8
    fontcolor= "#2D3436"

    node [
        shape = box
        fixedsize = true
        labelloc = c
        fontname = "Sans-Serif"
        fontsize = 8]
    
    subgraph{
        input_density -> prepocess
        input_density[label="3D cryo-EM\ndensity data\n(.mrc, .map)"]
    }
    
    subgraph{
        input_structure -> solvate -> relax
    }
    
    prepocess [color = red]
    
    align [color = red]
    
    force_field -> relax
    
    relax -> align
    
    prepocess -> align
    
    align -> shift_data
    
    force_field -> fitting
    
    prepocess -> fitting
    
    relax -> fitting
    
    shift_data -> fitting
    
    shift_data[color = red
    label="translation\nrotation"]
    force_field[label="force field \n water model"]
    input_structure[label="biomolecule\nstructure\n(.pdb)"]
}
```


---

name tools / design principles
explain fit workings
show fit results
show downsampled results

show mdpeditor

---

## What is a cryo-EM density?

> What is rational is real; And what is real is rational.
[name=cfh]

---

## 


> Any relationships between numbers, functions, and operations become transparent, generally applicable, and fully productive only after they have been isolated from their particular objects and been formulated as universally valid concepts[name=emmy noether]

---
> if density and diversity give life, the life they breed is disorderly.[name=jane jacobs]

---


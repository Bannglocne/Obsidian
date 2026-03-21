One **mole** is the amount of [[matter]] that contains as many objects ([[atoms]], [[molecules]],...) as the number of [[atoms]] in exactly 12 g of isotopically pure $^{12}C$ (**Avogadro's number** ($N_A$) = $6.02 \times 10^{23}$)

The mass in grams of one mole of a substance (that is the mass in grams per mole) is called the **molar mass** of the substance.

=> Interconverting Mass & Moles / Mass & Number of Particles
```mermaid
graph LR
    A[Grams]
    B[Moles]
    C[Formula units]

    A <--> |"Use <br> molar <br> mass"| B
    B <--> |"Use <br> Avogadro's <br> number"| C
```

=> Calculating an Empirical Formula: 
```mermaid
%%{init: {'theme': 'base', 'themeVariables': { 'fontSize': '13px', 'nodeSpacing': 30, 'rankSpacing': 40}}}%%
graph LR
    %% Định nghĩa Style nhỏ gọn
    classDef box fill:#fff,stroke:#ffe5d9,stroke-width:1px,color:#000,padding:5px
    classDef label fill:none,stroke:none,color:#555,font-size:11px

    subgraph 1
        direction LR
        A[Mass %] --> B(Assume<br>100g) --> C[Grams]
    end

    subgraph 2
        direction LR
        C --> D(Molar<br>mass) --> E[Moles]
    end

    subgraph 3
        direction LR
        E --> F(Mole<br>ratio) --> G[Empirical<br>formula]
    end

    %% Gán class
    class A,C,E,G box
    class B,D,F label
    
    %% Mũi tên đỏ mảnh hơn
    linkStyle 0,1,2,3,4,5 stroke:#ed1c24,stroke-width:1.5px
```

=> The subscripts in the molecular formula of a substance are always whole-number multiples of the subscripts in its empirical formula.
$$\text{Whole-number multiple} =  \frac{\text{molecular weight}}{\text{empiprical formula weight}}$$
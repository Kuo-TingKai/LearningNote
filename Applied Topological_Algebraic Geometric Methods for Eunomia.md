# Applied Topological/Algebraic Geometric Methods for Eunomia


## Potentials
- Semisupervised learning
    - Generalization of graph convolution filter (see ["Sheaf neural network"](https://arxiv.org/pdf/2012.06333.pdf)) and used for heterogeous graph data (each node/edge has different dimension/type of features)
    - Eg.Can be used for missing value imputation of sparse user database(in the other perspective,it also can be the tool of recommendation system)

- Data fusion (eg.["Towards A Topological Framework for Integrating Semantic Information Sources"](http://ceur-ws.org/Vol-1304/STIDS2014_P2_JoslynEtAl.pdf))
    - Current Application: Prof.Ghrist 的美國國防部計畫
        - Fusing data from multi-source and generate new features, can be used for recommendation system
    - Package [scikit-fusion](https://github.com/mims-harvard/scikit-fusion/tree/master/examples)
    - More detail, can see Justin Curry's [textbook for applied topology](https://arxiv.org/pdf/1303.3255.pdf )
        - Part III application: sensor network

---

- [Barcodes (topological data analysis)](https://www.ams.org/journals/bull/2008-45-01/S0273-0979-07-01191-3/S0273-0979-07-01191-3.pdf) for detecting hierarchical feature pattern of legal natural language processing

---

- Can see every database(structural or nonstructural) as simplicial complex(or a sheaf), see. Spivak's ["Simplicial Database"](https://math.mit.edu/~dspivak/informatics/SD.pdf)
- Build  "section"/"connection"(in the algebraic geometric meaning) between heterogeneous objects/types/attributes/hierarchies of simplicial database. You can image that is like doing tomography to the database.

## Packages
-  [pysheaf](https://github.com/kb1dds/pysheaf) and its [example code](https://github.com/kb1dds/pysheaf/blob/master/pysheaf/SheafCohomologyExample4-9.ipynb)
-  [persues](http://people.maths.ox.ac.uk/nanda/perseus/index.html)


## Other reference
- [My note](https://goodnotes.com/shares/#aHR0cHM6Ly93d3cuaWNsb3VkLmNvbS9zaGFyZS8wNjRrekxRWnJJdkRuSVFGRHprZHFNb0dnI1NoZWFmT3BpbmlvbkRpZmZ1c2lvbl9hbmRfU2hlYWZOTg==)
    - For sheaf neural network, see the last page of slide
    - For the detailed definition of sheaf data, see the rest of the note.
- [Shaef data course](https://www.drmichaelrobinson.net/sheaftutorial/index.html)




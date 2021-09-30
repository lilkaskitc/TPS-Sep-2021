# TPS-Sep-2021

Level 0: Base tree models of LGB, XGB. Several different parameters from other Kagglers are used to diversify. Ridge regression applies on all the tree models to soldify the anchor for next level stacking. Finally, a simple Keras NN is added for diversity which is justified in later stage stacking, though the individual CV is below the trees.

Level 1: Stacking on level 0 predictions with metamodels of LGB, XGB, CatB, NN, Ridge.

Level 2: Stacking on level 1 and level 0 predictions by Ridge. The final outputs is re-input to the same Ridge model for training, the loop is iterated until no further improvement in the CV.

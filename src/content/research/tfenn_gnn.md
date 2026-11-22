---
title: "Tensor Featured Neural Network in a GNN Framework"
shortTitle: "TFENN in a GNN Framework"
summary: "I am exploring whether tensor featured neurons in a graph neural network can improve force prediction in coarse grained molecular dynamics."
authors:
  - Boyang Chen
venue: "Computational Mechanics Laboratory"
year: 2026
order: 1
image: "media/tfenn_gnn/force_benchmark.png"
imageAlt: "My TFENN benchmark comparing force test MAE and training time per epoch with PaiNN, MACE, Wilson and Huang, and MACE CG"
imageFit: "contain"
imageLink: "reports/tfenn_gnn/force_benchmark.pdf"
imageCaption: "My independent TFENN research: test MAE and mean training time per epoch. Labels show trainable parameter counts."
architecture:
  - image: "media/tfenn_gnn/full_network.png"
    alt: "Overall TFENN graph neural network architecture"
    title: "Overall network"
    width: 1093
    height: 1352
  - image: "media/tfenn_gnn/message_block.png"
    alt: "TFENN message block architecture"
    title: "Message block"
    width: 1600
    height: 2264
detailImage: "media/tfenn_gnn/early_urop_poster.webp"
detailImageAlt: "Early UROP poster titled Tensor Feature Equivariant Neural Networks for Benzene Molecules"
detailImageHeading: "Early poster with Kevin and Victory"
detailImageCaption: "Early work with Kevin that started my later exploration. Poster by Boyang Chen, Kevin Garanger, Victory Ogbonnaya, and Julian Rimoli."
detailImageLink: "reports/tfenn_gnn/early_urop_poster.pdf"
detailImageWidth: 2200
detailImageHeight: 1436
galleryHeading: "At UROP"
gallery:
  - image: "media/tfenn_gnn/urop_friends.jpg"
    alt: "Sunny on the left, Victory in the center, and me on the right at the UROP Symposium"
    caption: "With Sunny (left) and Victory (center). Both are my Liquid Rocket teammates, and Victory also worked with me on tensegrity structures."
    width: 1280
    height: 1280
  - image: "media/tfenn_gnn/urop_symposium.jpg"
    alt: "Poster presentations at UCI's UROP Symposium"
    caption: "At UCI's UROP Symposium."
    width: 1280
    height: 1280
links:
  - label: Early poster
    url: "reports/tfenn_gnn/early_urop_poster.pdf"
  - label: Benchmark figure
    url: "reports/tfenn_gnn/force_benchmark.pdf"
---

## How it started

As a UROP Fellow in Professor Julián Rimoli’s Computational Mechanics Laboratory, I documented the lab’s model for bar elements in tensegrity structures, and independently resolved a singularity that arose at small angles near the element’s zero stress state. Inspired by the idea of singular value decomposition, I factored the Hessian matrix of the Hamiltonian into axial and angular parts and applied a Taylor expansion to the angle. This helped the lab overcome a major obstacle and turn to simulations of the model.

I also worked with Kevin Garanger, a postdoctoral researcher, to explore several ideas about incorporating physical constraints into neural networks. We used character tables to encode material symmetries, for example, and tried combining tensor featured neurons with LSTMs to capture both symmetry and history dependence. These experiments taught me how to monitor training and diagnose numerical problems. I presented preliminary results in a poster at UCI’s UROP Symposium.

## My independent research

After the postdoc left, I continued this direction as my independent research. I thought one of the issues we had was having a large scope, so I narrowed down my research to a particular case. I started exploring whether preserving molecular geometry in tensor representations and propagating them with tensor featured neurons could improve force prediction in coarse grained molecular dynamics. I spent the summer working on the formulation, preparing data and building and training the network. When the quarter began, I presented it to Prof. Rimoli.

The force predictions respect frame indifference, and in a benzene liquid benchmark, my model took less than one tenth as long per training epoch as the fastest coarse grained MACE baseline and achieved about 18% lower force prediction error than the most accurate MACE baseline. I have been working on drafting a manuscript describing the whole process.

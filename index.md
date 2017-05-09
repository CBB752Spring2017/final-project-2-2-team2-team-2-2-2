---
layout: page
title: CBB752 Spring 2017
tagline: Final Project
---

Project Title
------------------


Table of Contents
-----------------------




**Contributors**
 -Writing: Olivia Justynski
 -Coding:
 -Pipeline:

### Introduction:





### Writing:

How might SNPs in Carl’s genome impact the use of CRISPR as a treatment? Discuss how individual SNPs would impact the off-target effects in the presence of the SNP.

CRISPR-Cas9 nucleases are gene-editing technology that can be used to cleave specific sites in the genome of a living cell. They are made up of two component parts: a Cas9 protein and a guide RNA (gRNA), also known as a single guide RNA (sgRNA), which is approximately 100 nucleotides in length. When used for genome editing, the CRISPR-Cas9 nuclease recognizes two sites on the target DNA: the protospacer and the protospacer adjacent motif (PAM) sequence. First, the Cas9 protein binds with the PAM site. Next, the 5’ end of the gRNA base-pairs with the protospacer, which is then cleaved.

CRISPR-Cas9 has many applications that involve specific genome editing. It has already been used in agricultural and research contexts, but arguably the most exciting application for CRISPR-Cas9 is to alleviate the effects of genetic disease. In the future, CRISPR-Cas9 could be used to correct disease-causing mutations in patients with cystic fibrosis, muscular dystrophy, or even cancer. However, CRISPR-Cas9 has not yet been proven safe enough for therapeutic use in humans, as it cannot yet be used with perfect accuracy.

A significant challenge to the use of CRISPR-Cas9 is the prevalence of off-target cleavage mutations. In theory, cleavage should only occur at sites with sequences that perfectly match both the protospacer and PAM sequence intended to bind to the gRNA and Cas9 protein, respectively. However, in practice, off-target sites with up to five mismatched nucleotides can also be cleaved by the CRISPR-Cas9 nuclease with similar efficiencies as the intended site. If enough off-target sites are cleaved, this could cause major structural effects in the genome, including deletions, translocations, and other rearrangements. For CRISPR-Cas9 to be used as a therapeutic tool, methods must be improved to computationally predict these off-target effects, detect them if they occur, and effectively prevent them.

Two potential methods of preventing off-target effects are to increase the specificity of CRISPR-Cas9 nucleases and to limit their activity overall. One method to increase CRISPR-Cas9 specificity is to use shorter gRNAs, with the intent that there will only be sufficient base-pairing to bind the gRNA to a given sequence if it is a perfect match. In order to limit the activity of CRISPR-Cas9 nucleases, their half-life may be decreased with the intention of preventing binding to less likely sites. 

Designing gRNAs is an important aspect of CRISPR-Cas9 efficacy. It is important to use gRNAs that have only one perfect match site in the genome, and most desirable to use gRNAs that also have no close matches in the genome.

Recently, software called GuideScan was developed in order to improve the selection of gRNAs (Perez et al. 2017). The software can be customized for a particular genome and Cas9 protein. The user then defines their desired PAM site, the distance between the PAM site and the protospacer, and the size of the gRNA. The software then provides sets of gRNAs that could be used to edit the genome in the desired fashion. Importantly, the software predicts gRNAs that would be prone to off-target effects and eliminates them. Generally, this includes gRNAs for which there are other sequences in the given genome that are an exact or close (by one or two nucleotides) match with the desired protospacer. In this way, GuideScan can be used to increase the specificity of gene-editing with the supplied gRNAs.

Single nucleotide polymorphisms (SNPs), which cause the genome of interest to differ from the reference genome at a particular point, can impact CRISPR-Cas9 efficacy in two ways. First, a SNP in the intended protospacer or PAM site could cause the CRISPR-Cas9 nuclease to cleave that site less efficiently or not at all. This is relatively easily avoided by specifically examining the sequence of the region of the genome where CRISPR-Cas9 is meant to bind and accounting for any SNPs that may be present.

Second, a SNP elsewhere in the genome that increases the similarity of that region to the intended site may introduce an off-target effect. In this case, examining the reference genome may not reveal any off-target sites, but the SNP may have allowed for an unpredictable off-target effect. This is more difficult to detect, because it involves examining a much larger portion of the genome – possibly the entire genome. However, the ability to predict which mismatched sequences or potential SNPs may increase the likelihood of off-target effects may help avoid this problem.

Doench et al. investigated the likelihood of specific sequences to cause off-target effects (2016). They found that off-target effects can result from slightly mismatched PAM sites or protospacer sequences. For example, a Cas9 protein that is targeted to a PAM site with the sequence NGG could show off-target activity at NAG, NCG, or NGA PAM sites. 

Whether mismatched protospacer sequences result in CRISPR-Cas9 activity is heavily dependent on the position of the mismatch and the type of mismatch. For example, in the particular sequence investigated by Doench et al, an insertion or deletion relative to the intended protospacer rarely caused off-target effects, unless they occurred at positions 2, 3, 19, or 20 for insertions or positions 2 or 3 for deletions (2016). Note that in the case of an insertion or deletion relative to the intended protospacer, the DNA or gRNA will bulge outwards, respectively, upon binding.

Mismatched bases are more likely than insertions or deletions to lead to off-target effects. Again, the frequency of off-target effects depends heavily on the position and type of mismatch. For example, in the case studied by Doench et al, off-target activity would be likely to occur if a position occupied by a cytosine in the intended protospacer was replaced by a thymine. In contrast, off-target activity was unlikely if a position occupied by a guanine in the intended protospacer was replaced by a cytosine. Specifically at position 16, no off-target effects would occur if a protospacer pyrimidine was replaced with a purine, but off-target effects would occur if any other nucleotide were replaced with a thymine.

Considering this last example, it can be understood how individual SNPs may cause unpredicted off-target effects. If the intended protospacer had a cytosine at position 16, and another site in the reference genome was a match for the protospacer except for a guanine at position 16, no off-target effects would be predicted, and this site would not be considered a risk. However, if the individual had a SNP that replaced the position 16 guanine with a thymine, off-target effects would occur and could have a strong unintended effect.

These trends, therefore, can be used to predict the likelihood of off-target effects in the genome, particularly when SNPs are present that cause the individual genome to differ from the reference genome. These are important to consider, especially when CRISPR-Cas9 is being used on an individual genome, such as the Zimmerome. 









### Coding:


#### Documentation:


#### Results:







### Pipeline:


#### Documentation:


#### Results:









#### Conclusions:








#### References:

Barrangou R, Doudna JA. 2016. Applications of CRISPR technologies in research and beyond. Nature Biotechnology 34:933-941.

Doench JG, Fusi N, Sullender M, Hegde M, Vaimberg EW, Donovan KF, Smith I, Tothova Z, Wilen C, Orchard R, Virgin HW, Listgarten J, Root DE. 2016. Optimized sgRNA design to maximize activity and minimize off-target effects of CRISPR-Cas9. Nature Biotechnology 34:184-191.

Perez, AR, Pritykin Y, Vidigal JA, Chhangawala S, Zamparo L, Leslie CS, Ventura A. 2017. GuideScan software for improved single and paired CRISPR guide RNA design. Nature Biotechnology.

Tsai SQ, Joung JK. 2016. Defining and improving the genome-wide specificities of CRISPR-Cas9 nucleases. Nature Reviews: Genetics 300-311.
 
 

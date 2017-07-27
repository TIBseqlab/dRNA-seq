dRNA-seq实验流程
=============


### 样本要求：
1. total RNA纯化:为了得到包括small RNA在内的total RNA 选用TRIzol法进行RNA抽提。
2. total RNA质检:Nanodrop检测total RNA OD260/280值在1.8~2.2之间；Qubit2.0检测total RNA浓度≥100 ng/μl，总质量≥10μg；Agilent 2100检测total RNA 28S:18S≥1.5，RIN≥8。

### 实验流程：
1. rRNA-zero：使用Epicentre Ribo-Zero rRNA Removal Kits 去除total RNA 中的rRNA。
2. TEX消化：为了区分primary transcript和processed transcript，需要建立两个cDNA文库：TEX+库，用Terminator 5’-phosphate-dependent exonuclease（TEX，Epicentre）处理，消除带有5’P的processed transcript；TEX-库，不进行TEX处理，溶液中包含5’PPP的primary transcript和5’P的processed transcript。
3. 纯化：利用RNeasy MinElute Cleanup Kit分别对上述两个文库进行纯化。
4. TAP反应：对TEX+库和TEX-库分别进行tobacco acid pyrophosphatase（TAP，Epicentre）处理，TAP能够将初始转录本上的5’-PPP基团转化为5’-P基团，为后续的5’端加RNA接头做准备。
5. 纯化：再次利用RNeasy MinElute Cleanup Kit分别对上述两个文库进行纯化。
6. 建库：进一步利用RNA-Seq Library Preparation Kit for Transcriptome Discovery Gnomegen对上述两个进行dRNA-seq cDNA文库构建。
7. 可选择另外构建一个strand-specific whole-transcript文库并测序分析，该文库包含全部转录组信息，且具有链特异性，用于确认核实TSS。
8. 文库质检：用Qubit2.0、Agilent 2100、Real Time-PCR对文库质量、浓度、片段大小进行质检。
9. 上机测序。
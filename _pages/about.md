---
permalink: /
author_profile: true
image: ../images/photo.jpeg
title: Cloud-Edge Storage Reading Group
---

<br>This is the homepage of the **Cloud-Edge Storage Reading Group**. It brings together researchers and practitioners around the world broadly interested in this topic.  

### Get Involved
- Join our **[Tencent Meeting](https://meeting.tencent.com/dm/ZNbtfdeO5GNk)**: 488-2141-4823


### Upcoming Seminars



### Past Seminars

<span src="" style="float:right;width:100px;height:100px;margin-top:00px">
- 27th Sep 2023, 8:00pm (CST)  
Wenxi Zhu (XMU) <br>
**Oakestra: A Lightweight Hierarchical Orchestration Framework for Edge Computing**  <details>**Conference:**  ATC ’23<br>
**Abstract:** Edge computing seeks to enable applications with strict latency requirements by utilizing resources deployed in diverse, dynamic, and possibly constrained environments closer to the users. Existing state-of-the-art orchestration frameworks (e.g. Kubernetes) perform poorly at the edge since they were designed for reliable, low latency, high bandwidth cloud environments. We present Oakestra, a hierarchical, lightweight, flexible, and scalable orchestration framework for edge computing. Through its novel federated three-tier resource management, delegated task scheduling, and semantic overlay networking, Oakestra can flexibly consolidate multiple infrastructure providers and support applications over dynamic variations at the edge. Our comprehensive evaluation against the state-of-the-art demonstrates the significant benefits of Oakestra as it achieves approximately tenfold reduction in resource usage through reduced management overhead and 10% application performance improvement due to lightweight operation over constrained hardware.<br>
**Link:** [https://www.usenix.org/conference/atc23/presentation/bartolomeo](https://www.usenix.org/conference/atc23/presentation/bartolomeo)  <br> 
**Presentation Slides:** [pdf](../files/Oakestra.pdf)</details>

<span src="" style="float:right;width:100px;height:100px;margin-top:00px">
- 13rd Sep 2023, 8:00pm (CST)  
Ruilin Wu (UESTC) <br>
**Light-Dedup: A Light-weight Inline Deduplication Framework for Non-Volatile Memory File Systems**  <details>**Conference:**  ATC ’23<br>
**Abstract:** Emerging NVM is promising to become the next-generation storage media. However, its high cost hinders its development. Recent deduplication researches in NVM file systems demonstrate that NVM's cost can be reduced by eliminating redundant data blocks, but their design lacks complete insights into NVM's I/O mechanisms.<br>We propose Light-Dedup, a light-weight inline deduplication framework for NVM file systems that performs fast block-level deduplication while taking NVM's I/O mechanisms into consideration. Specifically, Light-Dedup proposes Light-Redundant-Block-Identifier (LRBI), which combines non-cryptographic hash with a speculative-prefetch-based byte-by-byte content-comparison approach. LRBI leverages the memory interface of NVM to enable asynchronous reads by speculatively prefetching in-NVM data blocks into the CPU/NVM buffers. Thus, NVM's read latency seen by content-comparison is markedly reduced due to buffer hits. Moreover, Light-Dedup adopts an in-NVM Light-Meta-Table (LMT) to store deduplication metadata and collaborate with LRBI. LMT is organized in the region granularity, which significantly reduces metadata I/O amplification and improves deduplication performance.<br>Experimental results suggest Light-Dedup achieves 1.01--8.98× I/O throughput over the state-of-the-art NVM deduplication file systems. Here, the speculative prefetch technique used in LRBI improves Light-Dedup by 0.3--118%. In addition, the region-based layout of LMT reduces metadata read/write amplification from 19.35× /9.86× to 6.10× /3.43× in our hand-crafted aging workload.<br>
**Link:** [https://www.usenix.org/conference/atc23/presentation/qiu-jiansheng](https://www.usenix.org/conference/atc23/presentation/qiu-jiansheng)  <br> 
**Presentation Slides:** [pdf]()</details>

<span src="" style="float:right;width:100px;height:100px;margin-top:00px">
- 13rd Sep 2023, 8:00pm (CST)  
Jingyuan Yang (UESTC) <br>
**Tectonic-Shift: A Composite Storage Fabric for Large-Scale ML Training**  <details>**Conference:**  ATC ’23<br>
**Abstract:** Tectonic-Shift is the storage fabric for Meta’s production machine learning (ML) training infrastructure. Industrial storage fabrics for ML need to meet both the intensive IO and high-capacity storage demands of training jobs. Our prior storage fabric, Tectonic, used hard disk drives (HDDs) to store training data. However, HDDs provide poor IO-per-watt performance. This inefficiency hindered the scalability of our storage fabric, and thus limited our ability to keep pace with rapidly growing training IO demands.<br>This paper describes our journey to build and deploy Tectonic-Shift, a composite storage fabric that efficiently serves the needs of our training infrastructure. We begin with a deep workload characterization that guided an extensive hardware and software design space exploration. We then present the principled design of Tectonic-Shift, which maximizes storage power efficiency by combining Shift, a flash storage tier, with Tectonic. Shift improves efficiency by absorbing reads using IO-efficient flash, reducing required HDD capacity. Shift maximizes IO absorption via novel application-aware cache policies that infer future access patterns from training dataset specifications. Shift absorbs 1.51-3.28x more IO than an LRU flash cache and reduces power demand in a petabyte-scale production Tectonic-Shift cluster by 29%.<br>
**Link:** [https://www.usenix.org/conference/atc23/presentation/zhao](https://www.usenix.org/conference/atc23/presentation/zhao)  <br> 
**Presentation Slides:** [pdf](../files/Tectonic-Shift.pdf)</details>

<span src="" style="float:right;width:100px;height:100px;margin-top:00px">
- 6th Sep 2023, 8:00pm (CST)  
Fang Zou (UESTC) <br>
**Portunus: Re-imagining Access Control in Distributed Systems**  <details>**Conference:**  ATC ’23<br>
**Abstract:** TLS termination, which is essential to network and security infrastructure providers, is an extremely latency-sensitive operation that benefits from access to sensitive key material close to the edge. However, increasing regulatory concerns prompt customers to demand sophisticated controls on where their keys may be accessed. While traditional access-control solutions rely on a highly-available centralized process to enforce access, the round-trip latency and decreased fault tolerance make this approach unappealing. Furthermore, the desired level of customer control is at odds with the homogeneity of the distribution process for each key.<br>To solve this dilemma, we have designed and implemented Portunus, a cryptographic storage and access control system built using a variant of public-key cryptography called attribute-based encryption (ABE). Using Portunus, TLS keys are protected using ABE under a policy chosen by the customer. Each server is issued unique ABE keys based on its attributes, allowing it to decrypt only the TLS keys for which it satisfies the policy. Thus, the encrypted keys can be stored at the edge, with access control enforced passively through ABE. If a server receives a TLS connection but is not authorized to decrypt the necessary TLS key, the request is forwarded directly to the nearest authorized server, further avoiding the need for a centralized coordinator. In comparison, a trivial instantiation of this system using standard public-key cryptography might wrap each TLS key with the key of every authorized data center. This strategy, however, multiplies the storage overhead by the number of data centers. Deployed across Cloudflare's 400+ global data centers, Portunus handles millions of requests per second globally, making it one of the largest deployments of ABE.<br>
**Link:** [https://www.usenix.org/conference/atc23/presentation/ladd](https://www.usenix.org/conference/atc23/presentation/ladd)  <br> 
**Presentation Slides:** [pdf](../files/Portunus.pdf)</details>

<span src="" style="float:right;width:100px;height:100px;margin-top:00px">
- 30th Aug 2023, 8:00pm (CST)  
Jun Wu (UESTC) <br>
**Revisiting Secondary Indexing in LSM-based Storage Systems with Persistent Memory**  <details>**Conference:**  ATC ’23<br>
**Abstract:** LSM-based storage systems are widely used for superior write performance on block devices. However, they currently fail to efficiently support secondary indexing, since a secondary index query operation usually needs to retrieve multiple small values, which scatter in multiple LSM components. In this work, we revisit secondary indexing in LSM-based storage systems with byte-addressable persistent memory (PM). Existing PM-based indexes are not directly competent for efficient secondary indexing. We propose PERSEID, an efficient PMbased secondary indexing mechanism for LSM-based storage systems, which takes into account both characteristics of PM and secondary indexing. PERSEID consists of (1) a specifically designed secondary index structure that achieves highperformance insertion and query, (2) a lightweight hybrid PM-DRAM and hash-based validation approach to filter out obsolete values with subtle overhead, and (3) two adapted optimizations on primary table searching issued from secondary indexes to accelerate non-index-only queries. Our evaluation shows that PERSEID outperforms existing PM-based indexes by 3-7× and achieves about two orders of magnitude performance of state-of-the-art LSM-based secondary indexing techniques even if on PM instead of disks.<br>
**Link:** [https://www.usenix.org/conference/atc23/presentation/wang-jing](https://www.usenix.org/conference/atc23/presentation/wang-jing)  <br> 
**Presentation Slides:** [pdf](../files/PERSEID.pdf)</details>

<span src="" style="float:right;width:100px;height:100px;margin-top:00px">
- 16th Aug 2023, 8:00pm (CST)  
Yuhui Chen (XMU) <br>
**Sponge: Fast Reactive Scaling for Stream Processing with Serverless Frameworks**  <details>**Conference:**  ATC ’23<br>
**Abstract:** Streaming workloads deal with data that is generated in real-time. This data is often unpredictable and changes rapidly in volume. To deal with these fluctuations, current systems aim to dynamically scale in and out, redistribute, and migrate computing tasks across a cluster of machines. While many prior works have focused on reducing the overhead of system reconfiguration and state migration on pre-allocated cluster resources, these approaches still face significant challenges in meeting latency SLOs at low operational costs, especially upon facing unpredictable bursty loads.<br>In this paper, we propose Sponge, a new stream processing system that enables fast reactive scaling of long-running stream queries by leveraging serverless framework (SF) instances. Sponge absorbs sudden, unpredictable increases in input loads from existing VMs with low latency and cost by taking advantage of the fact that SF instances can be initiated quickly, in just a few hundred milliseconds. Sponge efficiently tracks a small number of metrics to quickly detect bursty loads and make fast scaling decisions based on these metrics. Moreover, by incorporating optimization logic at compile-time and triggering fast data redirection and partial-state merging mechanisms at runtime, Sponge avoids optimization and state migration overheads during runtime while efficiently offloading bursty loads from existing VMs to new SF instances. Our evaluation on AWS EC2 and Lambda using the NEXMark benchmark shows that Sponge promptly reacts to bursty input loads, reducing 99th-percentile tail latencies by 88% on average compared to other stream query scaling methods on VMs. Sponge also reduces cost by 83% compared to methods that over-provision VMs to handle unpredictable bursty loads.<br>
**Link:** [https://www.usenix.org/conference/atc23/presentation/song](https://www.usenix.org/conference/atc23/presentation/song)  <br> 
**Presentation Slides:** [pdf](../files/20230823_reading_ATC'23_Sponge.pdf)</details>

<span src="" style="float:right;width:100px;height:100px;margin-top:00px">
- 23nd Aug 2023, 8:00pm (CST)  
Jia Zhang (UESTC) <br>
**On-demand Container Loading in AWS Lambda**  <details>**Conference:**  ATC ’23<br>
**Abstract:** AWS Lambda is a serverless event-driven compute service, part of a category of cloud compute offerings sometimes called Function-as-a-service (FaaS). When we first released AWS Lambda, functions were limited to 250MB of code and dependencies, packaged as a simple compressed archive. In 2020, we released support for deploying container images as large as 10GiB as Lambda functions, allowing customers to bring much larger code bases and sets of dependencies to Lambda. Supporting larger packages, while still meeting Lambda’s goals of rapid scale (adding up to 15,000 new containers per second for a single customer, and much more in aggregate), high request rate (millions of requests per second), high scale (millions of unique workloads), and low start-up times (as low as 50ms) presented a significant challenge.<br>We describe the storage and caching system we built, optimized for delivering container images on-demand, and our experiences designing, building, and operating it at scale. We focus on challenges around security, efficiency, latency, and cost, and how we addressed these challenges in a system that combines caching, deduplication, convergent encryption, erasure coding, and block-level demand loading.<br>Since building this system, it has reliably processed hundreds of trillions of Lambda invocations for over a million AWS customers, and has shown excellent resilience to load and infrastructure failures.<br>
**Link:** [https://www.usenix.org/conference/atc23/presentation/brooker](https://www.usenix.org/conference/atc23/presentation/brooker)  <br> 
**Presentation Slides:** [pdf](../files/aws-lambda.pdf)</details>

<span src="" style="float:right;width:100px;height:100px;margin-top:00px">
- 9th Aug 2023, 8:00pm (CST)  
Wenxi Zhu (XMU) <br>
**FarReach: Write-back Caching in Programmable Switches**  <details>**Conference:**  ATC ’23<br>
**Abstract:** Skewed write-intensive key-value storage workloads are increasingly observed in modern data centers, yet they also incur server overloads due to load imbalance. Programmable switches provide viable solutions for realizing load-balanced caching on the I/O path, and hence implementing write-back caching in programmable switches is a natural direction to absorb frequent writes for high write performance. However, enabling in-switch write-back caching is non-trivial, as it not only is challenged by the strict programming rules and limited stateful memory of programmable switches, but also necessitates reliable protection against data loss due to switch failures. We propose FarReach, a new caching framework that supports fast, available, and reliable in-switch write-back caching. FarReach carefully co-designs both the control and data planes for cache management in programmable switches, so as to achieve high data-plane performance with lightweight control-plane management. Experiments on a Tofino switch testbed show that FarReach achieves a throughput gain of up to 6.6× over a state-of-the-art in-switch caching approach under skewed write-intensive workloads.<br>
**Link:** [https://www.usenix.org/conference/atc23/presentation/sheng](https://www.usenix.org/conference/atc23/presentation/sheng)  <br> 
**Presentation Slides:** [pdf](../files/FarReach.pdf)</details>

<span src="" style="float:right;width:100px;height:100px;margin-top:00px">
- 2nd Aug 2023, 8:00pm (CST)  
Junhao Li (UESTC) <br>
**Adaptive Online Cache Capacity Optimization via Lightweight Working Set Size Estimation at Scale**  <details>**Conference:**  ATC ’23<br>
**Abstract:** Big data applications extensively use cache techniques to accelerate data access. A key challenge for improving cache utilization is provisioning a suitable cache size to fit the dynamic working set size (WSS) and understanding the related item repetition ratio (IRR) of the trace. We propose Cuki, an approximate data structure for efficiently estimating online WSS and IRR for variable-size item access with proven accuracy guarantee. Our solution is cache-friendly, thread-safe, and light-weighted in design. Based on that, we design an adaptive online cache capacity tuning mechanism. Moreover, Cuki can also be adapted to accurately estimate the cache miss ratio curve (MRC) online. We built Cuki as a lightweight plugin of the widely-used distributed file caching system Alluxio. Evaluation results show that Cuki has higher accuracy than four state-of-the-art algorithms by over an order of magnitude and with better stability in performance. The end-to-end data access experiments show that the adaptive cache tuning framework using Cuki reduces the table querying latency by 79% and improves the file reading throughput by 29% on average. Compared with the cutting-edge MRC approach, Cuki uses less memory and improves accuracy by around 73% on average. Cuki is deployed on one of the world’s largest social platforms to run the Presto query workloads.<br>
**Link:** [https://www.usenix.org/conference/atc23/presentation/gu](https://www.usenix.org/conference/atc23/presentation/gu)  <br> 
**Presentation Slides:** [pdf]()</details>

<span src="" style="float:right;width:100px;height:100px;margin-top:00px">
- 24th May 2023, 8:00pm (CST)  
Wenxi Zhu (XMU) <br>
**Speculative Recovery: Cheap, Highly Available Fault Tolerance with Disaggregated Storage**  <details>**Conference:**  ATC ’22<br>
**Abstract:** The ubiquity of disaggregated storage in cloud computing has led to a nascent technique for fault tolerance: instead of utilizing application-level replication, newly-launched backup instances recover application state from disaggregated storage (REDS) after a primary's failure. Attractively, REDS provides fault tolerance at a much lower cost than traditional replication schemes, wherein at least two instances are running. Failover in REDS is slow, however, because it sequentially first detects primary failure and only then starts recovery on a backup.<br>We propose speculative recovery to accelerate failover and thus increase the availability of applications using REDS. Instead of proceeding with failover sequentially, speculative recovery safely and efficiently parallelizes detecting primary failure and running recovery on a backup, by employing our new super and collapse primitives for disaggregated storage. Our implementation and evaluation of speculative recovery demonstrate that it considerably reduces failover time.<br>
**Link:** [https://www.usenix.org/conference/atc22/presentation/li-nanqinqin](https://www.usenix.org/conference/atc22/presentation/li-nanqinqin)  <br> 
**Presentation Slides:** [pdf](../files/SpecREDS.pdf)</details>

<span src="" style="float:right;width:100px;height:100px;margin-top:00px">
- 17th May 2023, 8:00pm (CST)  
Fang Zou (UESTC) <br>
**Memory deduplication for serverless computing with Medes**  <details>**Conference:**  EuroSys ’22<br>
**Abstract:** Serverless platforms today impose rigid trade-offs between resource use and user-perceived performance. Limited controls, provided via toggling sandboxes between warm and cold states and keep-alives, force operators to sacrifice significant resources to achieve good performance. We present a serverless framework, Medes, that breaks the rigid trade-off and allows operators to navigate the trade-off space smoothly. Medes leverages the fact that the warm sandboxes running on serverless platforms have a high fraction of duplication in their memory footprints. We exploit these redundant chunks to develop a new sandbox state, called a dedup state, that is more memory-efficient than the warm state and faster to restore from than the cold state. We develop novel mechanisms to identify memory redundancy at minimal overhead while ensuring that the dedup containers' memory footprint is small. Finally, we develop a simple sandbox management policy that exposes a narrow, intuitive interface for operators to trade-off performance for memory by jointly controlling warm and dedup sandboxes. Detailed experiments with a prototype using real-world serverless workloads demonstrate that Medes can provide up to 1×-2.75× improvements in the end-to-end latencies. The benefits of Medes are enhanced in memory pressure situations, where Medes can provide up to 3.8× improvements in end-to-end latencies. Medes achieves this by reducing the number of cold starts incurred by 10--50% against the state-of-the-art baselines. <br>
**Link:** [https://dl.acm.org/doi/abs/10.1145/3492321.3524272](https://dl.acm.org/doi/abs/10.1145/3492321.3524272)  <br> 
**Presentation Slides:** [pdf](../files/Medes.pdf)</details>

<span src="" style="float:right;width:100px;height:100px;margin-top:00px">
- 3rd May 2023, 8:00pm (CST)  
Yuhui Chen (XMU) <br>
**EdgeWise: A Better Stream Processing Engine for the Edge**  <details>**Conference:**  ATC ’19<br>
**Abstract:** Many Internet of Things (IoT) applications would benefit if streams of data could be analyzed rapidly at the Edge, near the data source. However, existing Stream Processing Engines (SPEs) are unsuited for the Edge because their designs assume Cloud-class resources and relatively generous throughput and latency constraints.<br>This paper presents EdgeWise, a new Edge-friendly SPE, and shows analytically and empirically that EdgeWise improves both throughput and latency. The key idea of EdgeWise is to incorporate a congestion-aware scheduler and a fixed-size worker pool into an SPE. Though this idea has been explored in the past, we are the first to apply it to modern SPEs and we provide a new queue-theoretic analysis to support it. In our single-node and distributed experiments we compare EdgeWise to the state-of-the-art Storm system. We report up to a 3x improvement in throughput while keeping latency low.<br>
**Link:** [https://www.usenix.org/conference/atc19/presentation/fu](https://www.usenix.org/conference/atc19/presentation/fu)  <br> 
**Presentation Slides:** [pdf](../files/ATC'19_EdgeWise_reading.pdf)</details>

<span src="" style="float:right;width:100px;height:100px;margin-top:00px">
- 26th April 2023, 8:00pm (CST)  
Jingyuan Yang (UESTC) <br>
**Lock-Free Collaboration Support for Cloud Storage Services with Operation Inference and Transformation**  <details>**Conference:**  FAST ’20<br>
**Abstract:** This paper studies how today’s cloud storage services support collaborative file editing. As a tradeoff for transparency/user-friendliness, they do not ask collaborators to use version control systems but instead implement their own heuristics for handling conflicts, which however often lead to unexpected and undesired experiences. With measurements and reverse engineering, we unravel a number of their design and implementation issues as the root causes of poor experiences. Driven by the findings, we propose to reconsider the collaboration support of cloud storage services from a novel perspective of operations without using any locks. To enable this idea, we design intelligent approaches to the inference and transformation of users’ editing operations, as well as optimizations to the maintenance of files’ historic versions. We build an open-source system UFC2 (User-Friendly Collaborative Cloud) to embody our design, which can avoid most (98%) conflicts with little (2%) time overhead. <br>
**Link:** [https://www.usenix.org/conference/fast20/presentation/chen](https://www.usenix.org/conference/fast20/presentation/chen) <br> 
**Presentation Slides:** [pdf](../files/Lock-free.pdf)</details>

<span src="" style="float:right;width:100px;height:100px;margin-top:00px">
- 19th April 2023, 8:00pm (CST)  
Wenxi Zhu (XMU) <br>
**StreamBox-TZ: Secure Stream Analytics at the Edge with TrustZone**  <details>**Conference:** ATC ’19<br>
**Abstract:** While it is compelling to process large streams of IoT data on the cloud edge, doing so exposes the data to a sophisticated, vulnerable software stack on the edge and hence security threats. To this end, we advocate isolating the data and its computations in a trusted execution environment (TEE) on the edge, shielding them from the remaining edge software stack which we deem untrusted.<br>This approach faces two major challenges: (1) executing high-throughput, low-delay stream analytics in a single TEE, which is constrained by a low trusted computing base (TCB) and limited physical memory; (2) verifying execution of stream analytics as the execution involves untrusted software components on the edge. In response, we present StreamBox-TZ (SBT), a stream analytics engine for an edge platform that offers strong data security, verifiable results, and good performance. SBT contributes a data plane designed and optimized for a TEE based on ARM TrustZone. It supports continuous remote attestation for analytics correctness and result freshness while incurring low overhead. SBT only adds 42.5 KB executable to the TCB (16% of the entire TCB). On an octa core ARMv8 platform, it delivers the state-of-the-art performance by processing input events up to 140 MB/sec (12M events/sec) with sub-second delay. The overhead incurred by SBT’s security mechanism is less than 25%.<br>
**Link:** [https://www.usenix.org/conference/atc19/presentation/park-heejin](https://www.usenix.org/conference/atc19/presentation/park-heejin) <br> 
**Presentation Slides:** [pdf](../files/SBT.pdf)</details>

<span src="" style="float:right;width:100px;height:100px;margin-top:00px">
- 12th April 2023, 8:00pm (CST)  
Fang Zou (UESTC) <br>
**HotDedup: Managing Hot Data Storage at Network Edge through Optimal Distributed Deduplication**  <details>**Conference:**  INFOCOM ’20<br>
**Abstract:** The rapid growth of computing capabilities at network edge calls for efficient management frameworks that not only considers placing hot data on edge storage for best accessibility and performance, but also makes optimal utilization of edge storage space. In this paper, we solve a joint optimization problem by exploiting both data popularity (for optimal data access performance) and data similarity (for optimal storage space efficiency). We show that the proposed optimization is NP- hard and develop a 2⌈2Γ⌉ - 1 + ϵ-approximation algorithm by (i) making novel use of δ-similarity graph to capture pairwise data similarity and (ii) leveraging the k-MST algorithm to solve a Prize Collecting Steiner Tree problem on the graph. The proposed algorithm is prototyped using an open-source distributed storage system, Cassandra. We evaluate its performance extensively on a real-world testbed and with respect to real-world IoT datasets. The algorithm is shown to achieve over 55% higher edge service rate and reduces request response time by about 30%. <br>
**Link:** [https://ieeexplore.ieee.org/abstract/document/9155233/](https://ieeexplore.ieee.org/abstract/document/9155233/) <br> 
**Presentation Slides:** [pdf](../files/HotDedup.pdf)</details>

<span src="" style="float:right;width:100px;height:100px;margin-top:00px">
- 5th April 2023, 8:00pm (CST)  
Yuhui Chen (XMU) <br>
**InftyDedup: Scalable and Cost-Effective Cloud Tiering with Deduplication**  <details>**Conference:**  FAST ’23<br>
**Abstract:** Cloud tiering is the process of moving selected data from on-premise storage to the cloud, which has recently become important for backup solutions. As subsequent backups usually contain repeating data, deduplication in cloud tiering can significantly reduce cloud storage utilization, and hence costs.<br>In this paper, we introduce InftyDedup, a novel system for cloud tiering with deduplication. Unlike existing solutions, it maximizes scalability by utilizing cloud services not only for storage but also for computation. Following a distributed batch approach with dynamically assigned cloud computation resources, InftyDedup can deduplicate multi-petabyte backups from multiple sources at costs on the order of a couple of dollars. Moreover, by selecting between hot and cold cloud storage based on the characteristics of each data chunk, our solution further reduces the overall costs by up to 26%–44%. InftyDedup is implemented in a state-of-the-art commercial backup system and evaluated in the cloud of a hyperscaler. <br>
**Link:** [https://www.usenix.org/conference/fast23/presentation/kotlarska](https://www.usenix.org/conference/fast23/presentation/kotlarska) <br> 
**Presentation Slides:** [pdf](../files/FAST'23_InftyDedup_reading_2.pdf)</details>

<span src="" style="float:right;width:100px;height:100px;margin-top:00px">
- 29th March 2023, 8:00pm (CST)  
Jingyuan Yang (UESTC) <br>
**Data Domain Cloud Tier: Backup here, backup there, deduplicated everywhere!** <details>**Conference:** ATC ’19 <br>
**Abstract:** Data Domain has added a cloud tier capability to its onpremises storage appliance, allowing clients to achieve the cost benefits of deduplication in the cloud. While there were many architectural changes necessary to support a cloud tier in a mature storage product, in this paper, we focus on innovations needed to support key functionality for customers. Consider typical customer interactions: First, a customer determines which files to migrate to the cloud by estimating how much space will be freed on the on-premises Data Domain appliance. Second, a customer transfers selected files to the cloud and later restores files back. Finally, a customer deletes a file in the cloud when its retention period has expired. Each of these operations requires significant architectural changes and new algorithms to address both the impact of deduplicated storage and the latency and expense of cloud object storage. We also present analysis from deployed cloud tier systems. As an example, some customers have moved more than 20PB of logical data to the cloud tier and achieved a total compression factor (deduplication * local compression) of 40× or more, resulting in millions of dollars of cost savings. <br>
**Link:** [https://www.usenix.org/conference/atc19/presentation/duggal](https://www.usenix.org/conference/atc19/presentation/duggal) <br> 
**Presentation Slides:** [pdf](../files/data_domain_cloud_tier.pdf)</details>


<!-- <iframe width="560" height="315" src="https://www.youtube.com/embed/Dn_NkH-IEVA" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe> -->

### Organizers

<span style="background-image:url('../images/ljw.jpg');background-size: cover;background-position-y: -20px; float:right;width:80px;height:90px;margin-top:00px"></span>
- **Jingwei Li**  
Researcher of [School of Computer Science and Engineering](https://www.scse.uestc.edu.cn/)<br>
 University of Electronic Science and Technology of China (UESTC)<br> [https://jingwei87.github.io/](https://jingwei87.github.io/)

<span style="background-image:url('../images/tl.jpg');background-size: cover; float:right;width:80px;height:100px;margin-top:00px"></span>
- **Lu Tang**  
Assistant Professor of [Department of Computer Science and Technology](https://cs.xmu.edu.cn/index.htm)<br>Xiamen University (XMU)<br>
[https://grace-tl.github.io/](https://grace-tl.github.io/)



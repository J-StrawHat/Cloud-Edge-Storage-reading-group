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

<span src="" style="float:right;width:100px;height:100px;margin-top:00px">
- 26th April 2023, 8:00pm (CST)  
Jingyuan Yang (UESTC) <br>
**Lock-Free Collaboration Support for Cloud Storage Services with Operation Inference and Transformation**  <details>**Conference:**  FAST ’20<br>
**Abstract:** This paper studies how today’s cloud storage services support collaborative file editing. As a tradeoff for transparency/user-friendliness, they do not ask collaborators to use version control systems but instead implement their own heuristics for handling conflicts, which however often lead to unexpected and undesired experiences. With measurements and reverse engineering, we unravel a number of their design and implementation issues as the root causes of poor experiences. Driven by the findings, we propose to reconsider the collaboration support of cloud storage services from a novel perspective of operations without using any locks. To enable this idea, we design intelligent approaches to the inference and transformation of users’ editing operations, as well as optimizations to the maintenance of files’ historic versions. We build an open-source system UFC2 (User-Friendly Collaborative Cloud) to embody our design, which can avoid most (98%) conflicts with little (2%) time overhead. <br>
**Link:** [https://www.usenix.org/conference/fast20/presentation/chen](https://www.usenix.org/conference/fast20/presentation/chen) </details>

<span src="" style="float:right;width:100px;height:100px;margin-top:00px">
- 3rd May 2023, 8:00pm (CST)  
Yuhui Chen (XMU) <br>
**TBD**  <details>**Conference:**  <br>
**Abstract:** <br>
**Link:** []() </details>

### Past Seminars

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



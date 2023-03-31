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
- 5th April 2023, 8:00pm (CST)  
Yuhui Chen (XMU) <br>
**InftyDedup: Scalable and Cost-Effective Cloud Tiering with Deduplication**  <details>**Conference:**  FAST ’23<br>
**Abstract:** Cloud tiering is the process of moving selected data from on-premise storage to the cloud, which has recently become important for backup solutions. As subsequent backups usually contain repeating data, deduplication in cloud tiering can significantly reduce cloud storage utilization, and hence costs.<br>In this paper, we introduce InftyDedup, a novel system for cloud tiering with deduplication. Unlike existing solutions, it maximizes scalability by utilizing cloud services not only for storage but also for computation. Following a distributed batch approach with dynamically assigned cloud computation resources, InftyDedup can deduplicate multi-petabyte backups from multiple sources at costs on the order of a couple of dollars. Moreover, by selecting between hot and cold cloud storage based on the characteristics of each data chunk, our solution further reduces the overall costs by up to 26%–44%. InftyDedup is implemented in a state-of-the-art commercial backup system and evaluated in the cloud of a hyperscaler. <br>
**Link:** [https://www.usenix.org/conference/fast23/presentation/kotlarska](https://www.usenix.org/conference/fast23/presentation/kotlarska) </details>

<span src="" style="float:right;width:100px;height:100px;margin-top:00px">
- 12th April 2023, 8:00pm (CST)  
Fang Zou (UESTC) <br>
**TBD**  <details>**Conference:**  <br>
**Abstract:**  <br>
**Link:** []() </details>




### Past Seminars

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



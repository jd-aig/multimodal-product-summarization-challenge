# Shared Task in NLPCC 2022: Multimodal Product Summarization 
The multimodal product summarization task aims at generating a condensed textual summary for a given product. The input contains a detailed product description, a product knowledge base, and a product image. 

## Table of Contents
- [Dataset](#Dataset)
	- [Dataset statistics](#Dataset_statistics)
	- [An example in the dataset](#An_example_in_the_dataset)
- [Baselines](#Baselines)
 	- [Text-only version](#Text-only_version)
	- [Multimodal version](#Multimodal_version)
- [Evaluation](#Evaluation)
	- [Human Evaluation](#Human_Evaluation)
- [Participation](#Participation)
- [Award](#award)
- [Important Dates](#Important_Dates)
- [Reference](#Reference)

<a name="Dataset"/>

## Dataset 
The dataset for this task is collected from JD.COM, a mainstream Chinese e-commerce platform. Each sample is a (product textual description, product knowledge base, product image, product summary) tuple. The dataset contains three product categories, including Cases&Bags, Home Appliances, and Clothing. 

<a name="Dataset_statistics"/>

### Dataset statistics 
<table>
   <tr>
      <th></th>
      <th>Cases&Bags</th>
      <th>Home Appliances</th>
      <th>Clothing</th>
   </tr>
   <tr>
      <td>Train</td>
      <td>50,000</td>
      <td>100,000</td>
      <td>200,000</td>
   </tr>
     <tr>
      <td>Valid</td>
      <td>10,000</td>
      <td>10,000</td>
      <td>10,000</td>
   </tr>
     <tr>
      <td>Test</td>
      <td>10,000</td>
      <td>10,000</td>
      <td>10,000</td>
   </tr>
     <tr>
      <td>Input token/sample</td>
      <td>319.0</td>
      <td>336.6</td>
      <td>294.8</td>
   </tr>
    <tr>
      <td>Product attribute/sample</td>
      <td>14.8</td>
      <td>7.8</td>
      <td>7.3</td>
   </tr>
      <tr>
      <td>Product image/sample</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
   </tr>
</table>

<a name="An_example_in_the_dataset"/>

### An example in the dataset
<table>
   <tr>
      <td>Input text</td>
      <td width=433>TCL D49A630U 49英寸超薄金属机身30核HDR 4K超清智能电视机（黑色）一个化繁为简的系统，暗的更暗，亮的更亮，您再也不会埋怨影片不够看了，4K超高清+全生态HDR，金属压铸支架，浑然天成的品质感，4K超高清屏幕，这是89万像素RGB真4K，30核心，性能再度升级，4K大屏新旗舰电视，让场景接近您感受的真实度，64位电视处理器，20000转/分高速打磨，硬解码，腾讯视频，全新升级，电视不止更薄，显示还更出色，金属纤薄机身，丰富接口，45°纹钻切工艺，4K超高清内容，一体成型LG0，强大的扩展能力，HDr实时转化，全生态HDR，24小时更新不断，金属外观设计，精美的UI设计，海量影视资源，集成了主页、影视、生活等</td>
   </tr>
   <tr>
      <td>Product image</td>
      <td><img src="https://user-images.githubusercontent.com/8317385/158300829-e7a26413-5812-4d22-a0ec-32150ac848d6.png"/></td>
   </tr>
   <tr>
      <td>Product attribute</td>
      <td>能效等级：3级   <br>  电视类型：4K超清 <br> 屏幕尺寸：49英寸  <br>     HDR显示：支持HDR</td>
   </tr>
   <tr>
      <td>Output summary</td>
      <td>这款TCL智能液晶电视，海量片库，任你观看。4K高清画质，画面更加清晰，给你身临其境之感。搭载画质新宠HDR技术，还原真实自然的画面。</td>
   </tr>
</table>

<a name="Baselines"/>

## Baselines
K-PLUG: Knowledge-injected Pre-trained Language Model for Natural Language Understanding and Generation in E-Commerce. (Findings of EMNLP 2021). 

<a name="Text-only_version"/>

### Text-only version
[code](https://github.com/jd-aig/k-plug)

<a name="Multimodal_version"/>

### Multimodal version
[code](https://github.com/jd-aig/m-kplug)

> Note: submission of the baselines are NOT acceptable.

<a name="Evaluation"/>

## Evaluation
The results need to be submitted to the [leaderboard](https://TODO) of the challenge. The evaluation consists of two stages, an automatic evaluation, and a human evaluation. For automatic evaluation, we adopt the metric of ROUGE. We select the top-5 teams regarding the average score of ROUGE-1, ROUGE-2, and ROUGE-L to advance to the second round of evaluation, i.e., the human evaluation. For the human evaluation, we evaluate faithfulness, readability, non-redundancy, and importance, for 100 random sampled summaries each category. The final ranking is determined by the average score of the human evaluation.

<a name="Human_Evaluation"/>

### Human Evaluation
<table>
   <tr>
      <td>Metrics</td>
      <td>Scores</td>
   </tr>
    <tr>
      <td>Faithfulness</td>
      <td>0=unfaithful to the input <br> 2=faithful to the input   </td>
   </tr>
   <tr>
      <td>Readability</td>
      <td>0=hard to understand <br> 1=partially hard to understand <br> 2=easy to understand</td>
   </tr>
    <tr>
      <td>Non-redundancy</td>
      <td>0=full of redundant information <br>  1=partially redundant information <br> 2=no redundant information</td>
   </tr>
   <tr>
      <td>Importance</td>
      <td>0=no useful information <br> 1=partially useful information <br> 2=totally useful information</td>
   </tr>
</table>

<a name="Participation"/>

## Participation
If you are interested in our challenge, please fill out the [application form](https://nlp-object-store.s3.cn-north-1.jdcloud-oss.com/multimodal-product-summarization-challenge/Application_terms.docx) and email lihaoran24 at jd.com (Please email us with your organization's email and note that you participate in the challenge). The dataset will be sent to you. 

<a name="award"/>

## Award
The top 3 participating teams will be certificated by NLPCC and CCF-NLP, as well as awarded cash rewards.

The first prize (*1): ￥3000 

The second prize (*1): ￥2000

The third prize (*1): ￥1000

<a name="Important_Dates"/>

## Important Dates
Announcement of shared tasks and call for participation:	2022/3/15

Registration open:	2022/3/15

Release of detailed task guidelines & training data:	2022/3/15

First submission of results on the blind test data:	2022/5/1

Registration deadline:	2022/5/5

Participants’ results submission deadline:	2022/6/3

Evaluation results release and call for system reports and conference paper:	2022/6/10

Conference paper submission deadline (only for shared tasks):	2022/6/20

Conference paper accept/reject notification:	2022/7/4

Camera-ready paper submission deadline:	2022/7/18

<a name="Reference"/>

### WeChat group for this shared task
 <img src="https://user-images.githubusercontent.com/8317385/164393399-b7c7d3d9-9d6c-416a-bba0-500742938710.png" width = "300" align=center />


## Reference
[1] Li et. al., [Aspect-Aware Multimodal Summarization for Chinese E-Commerce Products](https://scholar.archive.org/work/743ewpj4pfh3fcdk7paqfrd7pi/access/wayback/https://aaai.org/ojs/index.php/AAAI/article/download/6332/6188). AAAI 2020.

[2] Yuan et. al., [On the Faithfulness for E-commerce Product Summarization](https://aclanthology.org/2020.coling-main.502/). COLING 2020.

[3] Xu et. al., [Self-Attention Guided Copy Mechanism for Abstractive Summarization](https://aclanthology.org/2020.acl-main.125/). ACL 2020.

[4] Xu et. al., [K-PLUG: Knowledge-injected Pre-trained Language Model for Natural Language Understanding and Generation in E-Commerce](https://aclanthology.org/2021.findings-emnlp.1/). Findings of ACL: EMNLP 2021.


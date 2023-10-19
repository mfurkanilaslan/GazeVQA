<h2>GazeVQA: A Video Question Answering Dataset for Multiview Eye-Gaze Task-Oriented Collaborations</h2>

<h3><a href="https://2023.emnlp.org/"> GazeVQA Paper </a> :page_with_curl:</h3>
<h3><a href="https://nusu-my.sharepoint.com/:f:/g/personal/e0816604_u_nus_edu/EqS0Iaat4nNFsBOJSHwRj9YBLbIYq8ZF2bNvaMCZfdlm3Q"> GazeVQA Dataset </a> :book: & :clapper: </h3>
<h3><a href="https://github.com/showlab/AssistGaze"> Codes for AssistGaze </a> :computer: </h3>
<h3><a href="https://twitter.com/muhammetfi"> Twitter </a> :bird: </h3>


<p>Thrilled to release GazeVQA which is a video question answering dataset for multiview eye-gaze task-oriented collaborations and an AI assistant called AssistGaze is designed to answer the questions with three different answer types, namely textual, image, and video. Please check out our paper "GazeVQA: A Video Question Answering Dataset for Multiview Eye-Gaze Task-Oriented Collaborations"!</p>

<p>Please, if you have any questions, do not hesitate to contact me. (m.furkanilaslan@gmail.com)</p>

<h3>Overview</h3>

<h4>1. GazeVQA Dataset</h4>
<p>We build a novel task-oriented VQA dataset, called GazeVQA, for collaborative tasks where gaze information is captured during the task process. The GazeVQA is designed with a novel QA format that covers thirteen different reasoning types to capture different aspects of task information and user intent. For each participant, the GazeVQA consists of more than 1,100 textual questions and more than 500 labeled images that were annotated with the assistance of the Segment Anything Model. In total, 2,967 video clips, 12,491 labeled images, and 25,040 questions from 22 participants were included in the dataset.</p>

<img width="1158" alt="Screenshot 2023-10-16 at 14 56 29" src="https://github.com/mfurkanilaslan/GazeVQA/assets/70204805/01f7ff19-aab3-4894-99c5-c1fc0c287d96">
<p>Figure 1. GazeVQA Architecture: It consists of three different parts. QA Lists, Labeled images, and Video Clips. There are 22 participants, and each participant has their own sub-structures that are divided into assembly and disassembly parts for QA lists and Labeled images. additionally, they have 4 different video clips (TPV-sideward, TPV-enface, FPVgaze, and FPVraw) which explain why they were collected separately in the Dataset part of the paper. Each step has its own QA lists, labeled images, and video clips.</p>

<p>Videos are prepared in a logical manner. It follows the 5 steps/action pattern as Step1-5, Step2-6 ... The reason is to increase the number of videos and the usage of videos as inputs. Additionally, the videos are prepared in that manner because we want to increase the challenges for the model to make it talented to tough questions and tasks.</p>

<p> The video clips propose unique opportunities for task-collaborative projects. After downloading the videos, video clips could be cropped as action-by-action to be used in different studies. Additionally, the video clips' annotation file has been provided. You can find the raw videos, ELAN-Annotation file, raw and processed QA pair lists, and Task structures in the dataset.</p>


<h4>2. AssistGaze</h4>
<p>Inspired by the assisting models and common ground theory for industrial task collaboration applications, we propose a new AI model called AssistGaze that is designed to answer the questions with three different answer types, namely textual, image, and video. AssistGaze can effectively ground the perceptual input into semantic information while reducing ambiguities.</p>

<img width="1162" alt="Screenshot 2023-10-16 at 14 58 49" src="https://github.com/mfurkanilaslan/GazeVQA/assets/70204805/8bf1bc94-5951-42c5-9cf7-b74abdbbec0a">
<p>Figure 2. AssistGaze Model: Firstly, the features of questions and videos are taken as inputs; additionally, the features of textual answers and labeled images are extracted. Then the encoder structure is where the feature representations are obtained by input encoders. Finally, it performs answer prediction by contrastive loss check.</p>


<h4>3. Details of GazeVQA</h4>

<p>The GazeVQA dataset has been created to investigate collaborative tasks by multi-modal QAs and multi-view videos for industrial applications.GazeVQA is a dataset based on simulated scenarios for industrial applications of human-robot collaboration. In our industrial study including assembly and disassembly tasks, the 3D version of the Type C Gearbox-AGNEE Shaft Mounted Speed Reducer (SMSR) product was used. The experiments were realized according to the assembly and disassembly stages from the manual of the product.</p>


<img width="1160" alt="Screenshot 2023-10-16 at 15 24 54" src="https://github.com/mfurkanilaslan/GazeVQA/assets/70204805/ee5fc564-200a-4b12-846a-06b13e675c83">
<p>Figure 3. Assembly Steps and Protocols: The assembly task has 20 steps. However, we deleted the "pressing the white pins" step, which is 14, because it was not a common task among the subjects. Some tasks are separated and realized by the subject in two different steps. For instance, there are two oil level indicators, so screwing two oil level indicators is shown as one step in the figure, but some subjects have realized this in two steps. Thus, we have a maximum of 22 steps in the assembly task.</p>


<img width="1160" alt="Screenshot 2023-10-16 at 15 25 19" src="https://github.com/mfurkanilaslan/GazeVQA/assets/70204805/8f128eff-726f-4cc2-9003-4663b3c7f941">
<p>Figure 4. Disassembly Steps and Protocols: The disassembly task has 17 steps. However, some tasks are separated and realized by the subject in two different steps. For instance, there are two oil level indicators, so removing two oil level indicators is shown as one step in the figure, but some subjects have realized this in two steps. Thus, we have a maximum of 19 steps in the disassembly task. The picture on the right-bottom is the annotation example to show how to annotate the steps as atomic actions.</p>


<img width="1162" alt="Screenshot 2023-10-16 at 15 46 57" src="https://github.com/mfurkanilaslan/GazeVQA/assets/70204805/83fa9ce3-f45b-4f3c-b54f-99552fb63add">
<p>Figure 5. Assembly Video Clip: GazeVQA assembly action includes synchronized multi-view video clips of assembling the gearbox.</p>


<img width="1162" alt="Screenshot 2023-10-16 at 15 47 15" src="https://github.com/mfurkanilaslan/GazeVQA/assets/70204805/ab0b999a-0caf-4aa3-8548-71550b648030">
<p>Figure 6. Disassembly Video Clip: GazeVQA disassembly action includes synchronized multi-view video clips of disassembling the gearbox.</p>

<p>Different Angle Videos: None of the 22 participants in the study had any knowledge about this industrial product. While the applications of two participants were recorded with two camera angles (FPV and TPV), the applications of all the remaining participants were observed and recorded with three different camera angles (FPV and two different TPV angles). The use of these different videos has five different goals.</p>
<ol>
  <li>First, TPV videos are positioned as shown in Figures 7 and 8, providing us with spatial depth. As a future study projection, this depth provided by the angle differences of the cameras can also be used for 3D environment extraction in another project.</li>
  <li>Second, it is used to spatially locate small components that are not visible from an angle.</li>
  <li>Third, the frames taken from FPV videos can be positioned in such a way that they do not contain the answer to the question asked. This is due to the fact that the subject focuses on many different points during the experiment, which is a crucial situation and one of the biggest challenges. Since the human brain is highly talented for semantic understanding, AI models are not as skilled as the human brain because operation modes are different. Therefore, human gaze location changes between objects cannot be captured by FPV videos.</li>
  <li>Fourth, FPV videos provide information about the user's perspective and provide more semantic and genuine answers.</li>
  <li>Finally, eye gaze can be made available in FPV videos, which may have unique value to the field of VQA.</li> 
  </ol>
<p>Gaze information is collected from subjects by using eye-tracking glasses as a unique modality so that the questions are understood and answers maintain the ground truths. This gaze information, in particular, provides semantic information about the steps performed in the task and the user's intention by answering questions such as "Where did the subject look?" and "Which object will be assembled or disassembled after the current object is assembled or disassembled?" This unique information cannot be obtained from TPVs.</p>


<img width="1118" alt="Screenshot 2023-10-16 at 15 56 43" src="https://github.com/mfurkanilaslan/GazeVQA/assets/70204805/05175b53-0d7e-458b-a944-53e58aad4b2a">
<p>Figure 7. Experiment Environment: Spatial layout for GazeVQA data collection, and the images of QA tasks with the opening scene.</p>



<h4>4. Statistics and Analysis</h4>

<p>The GazeVQA is composed of the assembly task, which includes a maximum of 22 steps, and the disassembly task, which includes a maximum of 19 steps (not symmetrical). The participant data is used for detailed analysis, while the number of questions for the assembly task is 631; the number of textual, image, and video answers is 563, 306, and 479, respectively. The number of questions for the disassembly task is 521, while the number of textual, image, and video answers is 474, 266, and 389, respectively. The numbers of them for each participant are more than 1,000 textual, 550 images, and 850 video answers.</p>

<p>The total number of questions is 25,040 which are 8,509 "What", 3,017 "Which", 2,798 "Where", 785 "When", 44 "Who", 2,392 "How", 7,407 "Did", 44 "Is" and 44 "Was". The number of unique textual questions is 1,091. The detailed analyses of the QA pairs are shown in the appendix. In total, there are more than 22,000 textual answers, 12,400 labeled images that are used by one participant's experiment to increase the challenges, and 2,967 video clips in the dataset. Additionally, 18,700 video answers are expected, according to the questions.</p>


![Screenshot 2023-10-16 at 16 01 29](https://github.com/mfurkanilaslan/GazeVQA/assets/70204805/33b6cef3-79fe-455a-9869-2f5738530994)
<p> Figure 8. Diagram of the Most Frequent Words of the GazeVQA: "Subject" is the word that is most frequently used in the dataset as a subject, and then "did" is used to check whether the actions/tasks are completed or not. If the diagrams or the datasets are checked more than 20 action verbs are used, and the frequency of them is moderately higher than the other words are used. The reason is that the usage of more verbs could be helpful to increase the possibility of the usage of the GazeVQA QA list on the other industrial projects’ applications. Consequently, it could increase the generalizability of the GazeVQA.</p>


![Screenshot 2023-10-16 at 16 01 53](https://github.com/mfurkanilaslan/GazeVQA/assets/70204805/55a1f030-3e6d-497e-9859-06e6a79a1d32)
<p> Figure 9. Diagram of the Question Frequency of the GazeVQA: "What" and "Did" are the most frequent questions that are used to prove the application realization, object, and action recognition. On the other hand, "Which" and "Where" questions are helpful to object localization to increase the answers’ accuracy of the spatial questions. The importance of the "How" question is to show the completion of the tasks.</p>


<h4>5. QA Lists</h4>

<p>Protocol. The experiment was designed to be completed by two partners in order to work on the industrial counterpart of the efforts to create a common ground in task cooperation. While one of the partners in the experiment is an instructor, the other is a novice or subject to be trained. During the experiment, the subjects can ask for clarifications and help with instructions given by the instructor. The subject can be warned and assisted by the instructor in cases of incomplete action. One of the key rules is that the current step must be completed by the subject. Thus, it is impossible to go back to the previous stage.</p>

<p>VQA studies usually require a large number of QA lists to train a powerful inferential model. Questions to be asked should be able to assist the subjects with the necessary information to perform the task. Particularly, the research on eye-gaze solutions for VQA tasks should be more meticulous. Not only is the eye-gaze information semantically valuable, but it is also mostly noisy because of the fast thinking ability of humans. Questions answered by eye-gaze information need the necessary action words. Unnecessary words could not provide adequate information for the correct answers. While preparing the protocol, questions were prepared for challenges such as temporal action segmentation, action recognition, and object recognition, which can also be answered with TPV videos, as well as using gaze information as a unique method to improve our VQA dataset.</p>

![Screenshot 2023-10-16 at 21 29 11](https://github.com/mfurkanilaslan/GazeVQA/assets/70204805/438db7d4-5cac-4fba-b0e0-64aa829ed3aa)
<p>Figure 10. QA pairs list of step 1 of assembly steps: This question list belongs to one of the subjects. Each subject has a unique task-completion style. Therefore, each list was prepared manually to analyze the instructional video properly. Detailed understanding could be experienced by checking the dataset.</p>


<h4>6. Comparisons</h4>

<p>GazeVQA works on common grounding for collaborative interactions by using gaze information. It is formulated based on collaborative applications and aims to make predictions with text, image, and video answers. GazeVQA serves as a bridge to show how assembly-disassembly datasets could be combined with VQA applications by improving their functionalities.</p>

![Screenshot 2023-10-16 at 17 09 53](https://github.com/mfurkanilaslan/GazeVQA/assets/70204805/195c4a35-90f4-4dc5-b84b-e6fc62406cf2)
<p>Table 1. Dataset Comparison 1:Comparison of the GazeVQA and other action datasets in the context of total hours of video clips, number of videos, average length of video clips (in minutes), and number of verbs, actions, and objects.</p>

![Screenshot 2023-10-16 at 17 10 30](https://github.com/mfurkanilaslan/GazeVQA/assets/70204805/4c20ca66-826e-4192-92db-588b8f310228)
<p>Table 2. Dataset Comparison 2: Comparison of GazeVQA and existing VQA datasets by evaluating the number of videos, QA pairs, and annotation types.</p>

![Screenshot 2023-10-16 at 17 10 46](https://github.com/mfurkanilaslan/GazeVQA/assets/70204805/9ff29c94-015c-4edf-83d7-4daa9372a082)
<p>Table 3. Dataset Comparison 3: Existing VQA datasets and GazeVQA target to obtain all answer formats with Multiple Choices (MC) answer types by using novel gaze information.</p>

![Screenshot 2023-10-16 at 17 12 57](https://github.com/mfurkanilaslan/GazeVQA/assets/70204805/fbc11560-4c17-47cd-a120-768b13a5152d)
<p>Figure 11. Dataset Comparison on Reasoning Types: GazeVQA focuses on visual, semantic, spatial, location, temporal, and action-object relationships, as well as social interaction information extracted from questions that are asked from 13 different reasoning types. The figure is prepared to compare the current dataset by benefiting from AGQA.</p>


<h4>7. Benchmark & Baseline Results</h4>

<p> Table 4: Benchmarking: The results for baseline methods which are prepared in different frames with CLIP (Devlin et al., 2019) features and FPV video additions to the TPV videos. The benchmark has been done with the VIOLET (Fu et al., 2021) model by considering only the textual answer type. Not only does our novel multiple-answering approach, but our single-type answering approach also performs better against the SOTA textual answer models.</p>

| Methods                                    |Answering Type        | mAP           |
| -------------                              | -------------        |-------------  |
|Random Guess                                |Text                  | 0.07117       |
|VIOLET                                      |Text                  | 0.25499       |
|(Ours) 8 Frames of CLIP Features            |Text + Image + Video  | 0.27173       |
|(Ours) 16 Frames of CLIP Features           |Text + Image + Video  | 0.49190       |
|(Ours) FPV Video Add TPV Video              |Text + Image + Video  | 0.50400       |
|(Ours) 8 Frames of CLIP Features (standard) |Text + Image + Video  | 0.67199       |


<p> Table 5. Ablation studies are conducted by using the VIOLET Model (Fu et al., 2021). It shows the Fine-tuning of the VIOLET model’s fully connected layer with different learning rates. The last column represents the fine-tuned linear layer of the VIOLET (Fu et al., 2021) by unfreezing the last layer of the BERT (Devlin et al., 2018). LR: Learning Rate.</p>

|Epoch          |mAP, when LR: 1.2e-5  | mAP, when LR: 8e-4 |  mAP, when LR: 8e-4 and Unfrozen Layer of BERT|
| ------------- | -------------        |-------------       |-------------                    |
|1              | 0.09393              | 0.10475            | 0.23186                         |
|2              | 0.09776              | 0.10428            | 0.25420                         |
|3              | 0.10062              | 0.10396            | 0.25066                         |
|4              |     -                | 0.10564            | 0.25499                         |


<p>Table 6. Ablation studies and results for the usage of different multi-view inputs (FPV, TPV, and Eye-Gaze).</p>

| Video Inputs  | Video Inputs         | Video Inputs       | Metrics |
| ------------- | -------------        |-------------       |-------  |
| FPV           |TPV                   | EyeGaze            |  mAP    |
|&check;        | &check;              | &cross;            | 0.50047 |
|&cross;        | &check;              | &check;            | 0.50611 |
|&check;        | &cross;              | &check;            | 0.49826 |
|&check;        | &check;              | &check;            | 0.67199 |


<p>Table 7. The results of the usage of different answer types which are video, textual, and image.</p>

| Answer Types  |Answer Types          | Answer Types       | Metrics |
| ------------- | -------------        |-------------       |-------  |
| Video         |Text                  | Image              |  mAP    |
|&cross;        | &cross;              | &check;            | 0.33219 |
|&cross;        | &check;              | &check;            | 0.44828 |
|&cross;        | &check;              | &cross;            | 0.27173 |
|&check;        | &check;              | &cross;            | 0.29876 |
|&check;        | &cross;              | &cross;            | 0.22744 |
|&check;        | &cross;              | &check;            | 0.35233 |
|&check;        | &check;              | &check;            | 0.67199 |



<p>Table 8. Ablation studies on feature encoders to determine the use case differences of CLIP (Devlin et al., 2019) and MViTv2 (Li et al., 2022) for Textual and Video features, while Faster R-CNN (Ren et al., 2015) is used for object features.</p>

| Encoders      |Encoders         | Encoders        | Metrics |
| ------------- | -------------   |-------------    |-------  |
| Video         |Text             | Object          |  mAP    |
|MViTv2         | BERT            | Faaster R-CNN   | 0.39930 |
|CLIP (Visual)  | CLIP (Textual)  | Faaster R-CNN   | 0.67199 |


<p>Table 9. Ablation studies for the usage of different numbers of encoder layers to get accurate results.</p>

| Metrics       |# of Encoder Layers | # of Encoder Layers  | # of Encoder Layers |
| ------------- | -------------      |-------------         |-------              |
| Numbers       | 2                  | 3                    |  4                  |
| mAP           | 0.45579            |  0.67199             | 0.52896             |



<h4>8. Example</h4>

<p>Questions prepared from semantic perspectives could be answered by the egocentric view, which has gaze information since it provides a more instinctive approach. The proposed model uses the information captured from the eye-gaze-labeled image to predict the answer to the questions about the next step. The figure shows how semantic knowledge is used by the model.</p>

![Screenshot 2023-10-16 at 17 11 39](https://github.com/mfurkanilaslan/GazeVQA/assets/70204805/239adb23-c3e3-46fd-9f47-f11910a1d8a1)
<p>Figure 12. An example of GazeVQA and AssistGaze. The GazeVQA dataset contains gaze info with ego/exocentric videos to answer the questions that have semantic knowledge about human-robot studies.</p>


<h4>9. Citation</h4>

<p>[UPDATE SOON] If you found this repository useful, please consider citing our paper:</p>


<h4>10. References</h4>

<ol>
  <li>Kristen Grauman, et.al.  2022. Ego4d: Around the world in 3,000 hours of egocentric video. In IEEE/CVF Conference on Computer Vision and Pattern Recognition, CVPR 2022, New Orleans, LA, USA, June 18-24, 2022, pages 18973–18990. IEEE.</li> 
  <li>Francesco Ragusa, Antonino Furnari, Salvatore Livatino, and Giovanni Maria Farinella. 2021. The MECCANO dataset: Understanding human-object interactions from egocentric videos in an industrial like domain. In IEEE Winter Conference on Applications of Computer Vision, WACV 2021, Waikoloa, HI, USA, January 3-8, 2021, pages 1568–1577, "Waikoloa, HI, USA". IEEE.</li> 
  <li>Yizhak Ben-Shabat, Xin Yu, Fatemeh Sadat Saleh, Dylan Campbell, Cristian Rodriguez Opazo, Hongdong Li, and Stephen Gould. 2021. The IKEA ASM dataset: Understanding people assembling furniture through actions, objects and pose. In IEEE Winter Conference on Applications of Computer Vision, WACV 2021, Waikoloa, HI, USA, January 3-8, 2021, pages 846–858, "Waikoloa, HI, USA". IEEE.</li>
  <li>Fadime Sener, Dibyadip Chatterjee, Daniel Shelepov, Kun He, Dipika Singhania, Robert Wang, and Angela Yao. 2022. Assembly101: A large-scale multi-view video dataset for understanding procedural activities. In IEEE/CVF Conference on Computer Vision and Pattern Recognition, CVPR 2022, New Orleans, LA, USA, June 18-24, 2022, pages 21064–21074, "New Orleans, LA, USA". IEEE.</li>
  <li>Dima Damen, Hazel Doughty, Giovanni Maria Farinella, Sanja Fidler, Antonino Furnari, Evangelos Kazakos, Davide Moltisanti, Jonathan Munro, Toby Perrett, Will Price, and Michael Wray. 2021. The EPIC-KITCHENS dataset: Collection, challenges and baselines. IEEE Trans. Pattern Anal. Mach. Intell., 43(11):4125–4141.</li>
   <li>Dejing Xu, Zhou Zhao, Jun Xiao, Fei Wu, Hanwang Zhang, Xiangnan He, and Yueting Zhuang. 2017. Video question answering via gradually refined attention over appearance and motion. In Proceedings of the 2017 ACM on Multimedia Conference, MM 2017, Mountain View, CA, USA, October 23-27, 2017, pages 1645–1653, "Mountain View, CA". ACM.</li>
   <li>Jie Lei, Licheng Yu, Tamara Berg, and Mohit Bansal. 2020. TVQA+: Spatio-temporal grounding for video question answering. In Proceedings of the 58th Annual Meeting of the Association for Computational Linguistics, pages 8211–8225, Online. Association for Computational Linguistics.</li>
    <li>Anthony Colas, Seokhwan Kim, Franck Dernoncourt, Siddhesh Gupte, Zhe Wang, and Doo Soon Kim. 2020. TutorialVQA: Question answering dataset for tutorial videos. In Proceedings of the Twelfth Language Resources and Evaluation Conference, pages 5450–5455, Marseille, France. European Language Resources Association.</li>
    <li>Zhou Yu, Dejing Xu, Jun Yu, Ting Yu, Zhou Zhao, Yueting Zhuang, and Dacheng Tao. 2019. Activitynet-qa: A dataset for understanding complex web videos via question answering. In The Thirty-Third AAAI Conference on Artificial Intelligence, AAAI 2019, The Thirty-First Innovative Applications of Artificial Intelligence Conference, IAAI 2019, The Ninth AAAI Symposium on Educational Advances in Artificial Intelligence, EAAI 2019, Honolulu, Hawaii, USA, January 27 - February 1, 2019, pages 9127–9134, "Honolulu, Hawaii, USA". AAAI Press.</li>
    <li>Kexin Yi, Chuang Gan, Yunzhu Li, Pushmeet Kohli, Jiajun Wu, Antonio Torralba, and Joshua B. Tenenbaum. 2020. CLEVRER: collision events for video representation and reasoning. In 8th International Conference on Learning Representations, ICLR 2020, Addis Ababa, Ethiopia, April 26-30, 2020, "Addis Ababa, Ethiopia". OpenReview.net.</li>
    <li>Madeleine Grunde-McLaughlin, Ranjay Krishna, and Maneesh Agrawala. 2021. AGQA: A benchmark for compositional spatio-temporal reasoning. In IEEE Conference on Computer Vision and Pattern Recognition, CVPR 2021, virtual, June 19-25, 2021, pages 11287–11297, "Virtual". Computer Vision Foundation / IEEE.</li>
    <li>Junbin Xiao, Xindi Shang, Angela Yao, and Tat-Seng Chua. 2021. Next-qa: Next phase of question answering to explaining temporal actions. In IEEE Conference on Computer Vision and Pattern Recognition, CVPR 2021, virtual, June 19-25, 2021, pages 9777–9786, "Virtual". Computer Vision Foundation / IEEE.</li>
    <li>Antoine Miech, Dimitri Zhukov, Jean-Baptiste Alayrac, Makarand Tapaswi, Ivan Laptev, and Josef Sivic. 2019. Howto100m: Learning a text-video embedding by watching hundred million narrated video clips. In 2019 IEEE/CVF International Conference on Computer Vision, ICCV 2019, Seoul, Korea (South), October 27 - November 2, 2019, pages 2630–2640, "Seoul, Korea (South)". IEEE.</li>
    <li>Alec Radford, Jong Wook Kim, Chris Hallacy, Aditya Ramesh, Gabriel Goh, Sandhini Agarwal, Girish Sastry, Amanda Askell, Pamela Mishkin, Jack Clark, Gretchen Krueger, and Ilya Sutskever. 2021. Learning transferable visual models from natural language supervision. In Proceedings of the 38th International Conference on Machine Learning, ICML 2021, 18-24 July 2021, Virtual Event, volume 139 of Proceedings of Machine Learning Research, pages 8748–8763, "Virtual". PMLR.</li>
    <li>Tsu-Jui Fu, Linjie Li, Zhe Gan, Kevin Lin, William Yang Wang, Lijuan Wang, and Zicheng Liu. 2021. VIOLET : End-to-end video-language transformers with masked visual-token modeling. CoRR, abs/2111.12681.</li>
    <li>Jacob Devlin, Ming-Wei Chang, Kenton Lee, and Kristina Toutanova. 2018. BERT: pre-training of deep bidirectional transformers for language understanding. CoRR, abs/1810.04805.</li>
    <li>Ze Liu, Jia Ning, Yue Cao, Yixuan Wei, Zheng Zhang, Stephen Lin, and Han Hu. 2022. Video swin transformer. In IEEE/CVF Conference on Computer Vision and Pattern Recognition, CVPR 2022, New Orleans, LA, USA, June 18-24, 2022, pages 3192–3201. IEEE.</li> 
  </ol>

<h2>Please, if you have any questions, do not hesitate to contact me. (m.furkanilaslan@gmail.com)</h2>


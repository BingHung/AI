# AI

## Retrain_Inception_Resenet_V2 Tutorial
tensorflow平台模型網址 https://tfhub.dev/s?module-type=image-classification  <br />

--建立虛擬環境:  <br />
conda create –n tf python=3.6		
 
--安裝tensorflow  <br />
pip install tensorflow tensorflow_hub

--1.切換工作目錄  <br />
cd /d C:\Users\n000022785\Downloads\TL
activate tf

--2.訓練模型語法  <br />
python retrain.py --image_dir flower_photos <br />
[ok] python retrain_IRV2.py --image_dir FHI_RT <br />
[ok] python retrain_IRV2.py --image_dir FHIRTTrain <br />
[ok] python retrain.py --image_dir FHI_RT 

--3.測試影像語法  <br />
--單張  <br />
python label_image.py --graph=c:\tmp\output_graph.pb --labels=c:\tmp\output_labels.txt --input_layer=Placeholder --output_layer=final_result --image=RT_test/51.jpg

--多張  <br />
python label_image_loop.py --graph=c:\tmp\output_graph.pb --labels=c:\tmp\output_labels.txt --input_layer=Placeholder --output_layer=final_result --image=RT_test  <br />
python fhi_test.py --graph=c:\tmp\output_graph.pb --labels=c:\tmp\output_labels.txt --input_layer=Placeholder --output_layer=final_result --image=test1

--imagenet/inception_resnet_v2/classification  <br />
https://tfhub.dev/google/imagenet/inception_resnet_v2/classification/1

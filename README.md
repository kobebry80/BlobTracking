
A background subtraction based tracking algorithm using OpenCV. It depends on OpenCv (http://opencv.org/) and Boost libraries (http://www.boost.org/).

Usage
------------

In order to run the tracker, use the following command:

### Windows ###

BlobTracker.exe -d config.cfg

### Linux ###
./BlobTracker -d config.cfg

### Config Params ###

config.cfg has all the configurations for running the tracker, here are the few things that you would have to change.

      * "Input_Video_Directory"   		---> where the video files are stored
      * "Input_Video_Name_List"   		---> name of the video files (comma separated)
      * "Input_Camera_ID_List"	  		---> camera id for internal usage( use sequential numbers)
      * "Start_Frame_Index"		  		---> starting frame for the video to be processed (0 to start from the beginning)
      * "Number_Of_Frames"		  		---> number of frames to be tracked (-1 for the entire video)

      * "OutPut_Video_Directory"  		---> where the output files will be stored (also the track outputs in text format)
      * "Log_File_Name"			  		---> name of the log file (log file will be generated in the output folder)
      * "Display_Intermediate_Result"   ---> whether to display intermediate output on the dialog box or not
      * "Save_Intermediate_Result"		---> whether to save the intermediate results on the output directory

      * "Down_Scale_Image"				---> whether to downscale the image by a factor or 2 or not (use it for speed)

      * "FG_Train_Frames"				---> number of frames used for training the background model

### Output ###

Output videos will be created in the specified output folder ("OutPut_Video_Directory").

      * input_file_name.extension_BT.avi contains the learned background video
      * input_file_name.extension_FG.avi shows the foreground region

      * input_file_name.extension_record.txt stores the tracking results in the following format:[ frameNumber, xCentroid, yCentroid, width, height, objectId, timestamp(seconds) ]


### Contact ###
[1] Santhoshkumar Sunderrajan( santhosh@ece.ucsb.edu)
Website: http://santhoshsunderrajan.com/

### Bibtex ###
If you use the code in any of your research works, please cite the following papers:
~~~
@ARTICLE{sunderrajan2015context, 
  author={Sunderrajan, S. and Manjunath, B.S.}, 
  journal={Multimedia, IEEE Transactions on}, 
  title={Context-Aware Hypergraph Modeling for Re-identification and Summarization}, 
  year={2016}, 
  volume={18}, 
  number={1}, 
  pages={51-63}, 
  keywords={Cameras;Clothing;Histograms;Image color analysis;Indexes;Topology;Training;Camera network;person re-identification;search;summarization}, 
  doi={10.1109/TMM.2015.2496139}, 
  ISSN={1520-9210}, 
  month={Jan}
}

@inproceedings{sunderrajan2013context,
  title={Context-Aware Graph Modeling for Object Search and Retrieval in a Wide Area Camera Network},
  author={Sunderrajan, Santhoshkumar and Xu, Jiejun and Manjunath, BS},
  booktitle={Proc. International Conference on Distributed Smart Cameras},
  year={2013}
}

@article{xu2013graph,
  title={Graph-Based Topic-Focused Retrieval in Distributed Camera Network},
  author={Xu, Jiejun and Jagadeesh, Vignesh and Ni, Zefeng and Sunderrajan, Santhoshkumar and Manjunath, BS},
  year={2013},
  publisher={IEEE}
}

@article{sunderrajanucsb,
  title={UCSB UCR VCG TRECVID 2012},
  author={Sunderrajan, Santhoshkumar and Hasan, Mahmudul and Pourian, Niloufar and Zhu, Yingying and Manjunath, BS and Chowdhury, Amit Roy}
}
~~~

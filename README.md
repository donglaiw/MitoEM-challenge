# MitoEM-challenge
starter code for mitoEM ISBI2021 Challenge

## Data Visualization
Here's the neuroglancer link for [[MitoEM-R](https://neuroglancer-demo.appspot.com/#!%7B%22dimensions%22:%7B%22x%22:%5B8e-9%2C%22m%22%5D%2C%22y%22:%5B8e-9%2C%22m%22%5D%2C%22z%22:%5B3e-8%2C%22m%22%5D%7D%2C%22position%22:%5B1979.8197021484375%2C1443.3648681640625%2C0.5%5D%2C%22crossSectionScale%22:4.450634482642984%2C%22projectionScale%22:4096%2C%22layers%22:%5B%7B%22type%22:%22image%22%2C%22source%22:%22precomputed://https://rhoana.rc.fas.harvard.edu/ng/MitoEM-R%22%2C%22tab%22:%22source%22%2C%22name%22:%22MitoEM-R%22%7D%5D%2C%22selectedLayer%22:%7B%22layer%22:%22MitoEM-R%22%2C%22visible%22:true%7D%2C%22layout%22:%22xy%22%2C%22partialViewport%22:%5B0%2C0%2C1%2C1%5D%7D)], [[MitoEM-H](https://neuroglancer-demo.appspot.com/#!%7B%22dimensions%22:%7B%22x%22:%5B8e-9%2C%22m%22%5D%2C%22y%22:%5B8e-9%2C%22m%22%5D%2C%22z%22:%5B3e-8%2C%22m%22%5D%7D%2C%22position%22:%5B2048.5%2C2048.5%2C500.5%5D%2C%22crossSectionScale%22:1%2C%22projectionScale%22:4096%2C%22layers%22:%5B%7B%22type%22:%22image%22%2C%22source%22:%22precomputed://https://rhoana.rc.fas.harvard.edu/ng/MitoEM-H%22%2C%22tab%22:%22source%22%2C%22name%22:%22MitoEM-H%22%7D%5D%2C%22selectedLayer%22:%7B%22layer%22:%22MitoEM-H%22%2C%22visible%22:true%7D%2C%22layout%22:%22xy%22%2C%22partialViewport%22:%5B0%2C0%2C1%2C1%5D%7D)]

## Auxiliary code to generate H5 files
If you have mitochondria predictions images in a folder, sorted by name, you can convert them into a H5 file following the [code](https://github.com/donglaiw/MitoEM-challenge/blob/main/aux/convert_images_into_h5.py). 

Notice some points of the script:
  - The volume is created with a downsampled (by 2) version of the original images 
  - Connected components is used to label the different mitochondria instances. However, another labelling method are also allowed (please describe it in the submission comments or in supplementary files)
  - LZF compression is applied in order to save space and submission time

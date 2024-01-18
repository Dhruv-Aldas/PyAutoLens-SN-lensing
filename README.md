#  PyAutoLens package set up
Strong lensing model code for MACS J0138 Supernova system using PyAutoLens. 

Note: There is an error on Windows for the dynesty package which gives the "file already exists error". A previous commit was uploaded with this issue in the notebook. It has been updated with a working file now.

To fix the issue on Windows: 
1. Go to Users/{Username}/anaconda3/Lib/dynesty/
2. Open utils.py
3. Go to line 2325 and below the pickle.module.dump(D, fp) insert the following code:
   if os.path.exists(fname):
     os.remove(fname)
4. Save the changes and the MACS_J0138.ipynb file should work on Windows now

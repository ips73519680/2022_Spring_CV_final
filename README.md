# Facial landmark detection
### Environment Setting
```bash=
pip install -r requirements.txt
```

### Training
```bash=
python train.py \
--PDB_mode \
--model_path ./checkpoint/model.pkl \
--dataroot ${train_file_path} \
--val_dataroot ${validation_file_path}
``` 

### Inference
```bash=
python test.py \
--model_path ./checkpoint/model.pkl \
--test_root ${test_file_path}
# our best model
python test.py \
--model_path \
./checkpoint/best_shuffle_un.pkl \
--test_root ${test_file_path}
```
# dvc-tutorial

### Followed [Data Version Control With Python and DVC](https://github.com/realpython/data-version-control)

##### DVC remote: `/Users/stefanpetrescu/dvc_remote`

`conda create --name dvc python=3.8.2 -y` <br>
`conda activate dvc` <br>
`python -m pip install dvc scikit-learn scikit-image pandas numpy`<br>
`curl https://s3.amazonaws.com/fast-ai-imageclas/imagenette2-160.tgz \ -O imagenette2-160.tgz`<br>
`tar -xzvf imagenette2-160.tgz`<br>
`mv imagenette2-160/train data/raw/train`<br>
`mv imagenette2-160/val data/raw/val`<br>
`rm -rf imagenette2-160`<br>
`rm imagenette2-160.tgz`<br>

# 
`git checkout -b "first_experiment"` <br>
`dvc init` <br>
`dvc config core.analytics false` <br>
`dvc remote add -d remote_storage /Users/stefanpetrescu/dvc_remote` <br>
`dvc add data/raw/train` <br>
`dvc add data/raw/val` <br>
`git add .`<br>
`git commit -m "First commit with setup and DVC files"`<br>
`dvc push`


## Quickly change git username
`git config --local credential.helper ""`<br>
`git push origin master`<br>
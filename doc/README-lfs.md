Move all the pdf files to lfs:

```
curl -s https://packagecloud.io/install/repositories/github/git-lfs/script.deb.sh | sudo bash
sudo apt-get install git-lfs
git lfs install

git lfs track "*.pdf"
git add .gitattributes
git lfs migrate import --include="**.pdf"
git pu -f
```

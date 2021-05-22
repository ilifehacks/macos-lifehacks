# Clear Finder icon cache

[source](https://gist.github.com/ismyrnow/e92c6010cda9325b2d8811387a05f224)

```sh
sudo rm -rfv /Library/Caches/com.apple.iconservices.store;
sudo find /private/var/folders/ \( -name com.apple.dock.iconcache -or -name com.apple.iconservices \) -exec rm -rfv {} \; ; 
sleep 3;
sudo touch /Applications/*; 
killall Dock; 
killall Finder;
```


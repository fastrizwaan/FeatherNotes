# FeatherNotes Flatpak
Qt5 based good note taking application

### Build
```
sudo flatpak remote-add --if-not-exists flathub https://flathub.org/repo/flathub.flatpakrepo
sudo flatpak install flathub org.kde.Sdk/x86_64/5.15 org.kde.Platform/x86_64/5.15

git clone https://github.com/fastrizwaan/FeatherNotes_flatpak.git
cd FeatherNotes/
flatpak-builder --force-clean build-dir io.github.FeatherNotes.yml
flatpak-builder --install --user --force-clean build-dir io.github.FeatherNotes.yml
```
#### Run
`flatpak run io.github.FeatherNotes`

#### Build a flatpak bundle file from the above built repo:
```
flatpak-builder --repo="repo" --force-clean "build" io.github.FeatherNotes.yml
flatpak --user remote-add --no-gpg-verify "io.github.FeatherNotes" "repo"
flatpak build-bundle "repo" "io.github.FeatherNotes.flatpak" io.github.FeatherNotes  --runtime-repo="https://flathub.org/repo/flathub.flatpakrepo"

flatpak --user install io.github.FeatherNotes.flatpak
flatpak run io.github.FeatherNotes
```

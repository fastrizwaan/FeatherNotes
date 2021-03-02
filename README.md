# FeatherNotes
Qt5 based good note taking application

### Build
sudo flatpak remote-add --if-not-exists flathub https://flathub.org/repo/flathub.flatpakrepo
sudo flatpak install flathub org.kde.Sdk/x86_64/5.15 org.kde.Platform/x86_64/5.15

git clone https://github.com/fastrizwaan/FeatherNotes.git
cd FeatherNotes/
flatpak-builder --force-clean build-dir io.github.FeatherNotes.yml
flatpak-builder --install --user --force-clean build-dir io.github.FeatherNotes.yml

#### Run
flatpak run io.github.FeatherNotes

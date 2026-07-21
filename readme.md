pacman -Ql libayatana-appindicator | grep -E '\.pc$|app-indicator\.h$'

sudo mkdir -p /usr/include/libappindicator
sudo ln -sf /usr/include/libayatana-appindicator3-0.1/libayatana-appindicator/app-indicator.h \
            /usr/include/libappindicator/app-indicator.h

sudo ln -sf /usr/lib/pkgconfig/ayatana-appindicator3-0.1.pc /usr/lib/pkgconfig/appindicator3-0.1.pc


ls -la /usr/include/libappindicator/
pkg-config --cflags --libs appindicator3-0.1

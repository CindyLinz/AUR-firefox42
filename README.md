# AUR firefox42

This is a archlinux package file, for firefox42.

I'll install Firefox version 42.0 and named `firefox42`.
So that you can still install and use other firefox versions without conflictions.

# Install

```shell
git clone https://github.com/CindyLinz/AUR-firefox42.git
cd AUR-firefox42
makepkg -sri
```

# Usage

```shell
firefox42
```

# Uninstall

```shell
sudo pacman -Rs firefox42
```

# Reason

Because 42 is a good number.. (X)

為了使用 [Linux專用版 WebATM plugin(64-bit)](https://netbank.esunbank.com.tw/webatm/cabs/esb_xcsp_for_firefox-1.0.4.5-fx-Linux_x86_64-gcc3.xpi) 這個沒有簽名的 plugin.. 所以裝一個 42 版來使用它.

Firefox 一般版 version 43 以後會強制拒絕安裝沒有簽名的 plugin. 不過尚可以手動把解開 xpi 把裡面的 `libnpWebATM.so` 放在 `$HOME/.mozilla/plugins/` 裡面, 就仍然可以使用, 一直到 version 52 以後 Firefox 移除 NPAPI 才會完全不能使用. 不過反正這一個 firefox 只會拿來使用玉山 WebATM 的話, 其實也沒什麼必要用新的, 用 42 版安裝步驟比較省事.. :p

**不過, 我還是好希望可以在 current Firefox 使用啊.... QQ**

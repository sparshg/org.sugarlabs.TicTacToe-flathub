# TicTacToe Flatpak

A simple Tic-Tac-Toe game.

To know more refer: https://github.com/sugarlabs/tictactoe

## How To Build

```
git clone https://github.com/flathub/org.sugarlabs.TicTacToe.git
cd org.sugarlabs.TicTacToe
flatpak -y --user install org.gnome.{Platform,Sdk}//44
flatpak-builder --user --force-clean --install build org.sugarlabs.TicTacToe.json
```

## Check For Updates

Install the flatpak external data checker
```
flatpak --user install org.flathub.flatpak-external-data-checker
```

Now to update every single module to the latest stable version use
```
cd org.sugarlabs.TicTacToe
flatpak run --filesystem=$PWD org.flathub.flatpak-external-data-checker org.sugarlabs.TicTacToe.json
```

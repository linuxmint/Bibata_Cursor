# Bibata Cursor

[![build](https://github.com/ful1e5/Bibata_Cursor/actions/workflows/build.yml/badge.svg)](https://github.com/ful1e5/Bibata_Cursor/actions/workflows/build.yml)

TLDR; This cursor set is the masterpiece of cursors available on the internet,
Hand designed by [Abdulkaiz Khatri](https://twitter.com/ful1e5).

Bibata is open source, compact, and material designed cursor set. This project masterelop for
improve cursor experience.

Bibata is one of the most popular cursors set in the Linux community so far and is now available
for freely with multiple colors and size options for Windows as well. The aim of this project is to
provide the personalized cursors to users.

## Bibata needs your Input

Until 2021 my cursors projects were well funded by [pling.com](https://www.pling.com) but since the
[pling-factor](https://www.pling.com/terms/payout) on the website has decreased and monthly payments
are <500$, It is now dependent on community funding and sponsorships. If you want to help me to maintain
Bibata and my other open source projects actively, consider sponsoring my work on [GitHub Sponsor](https://github.com/sponsors/ful1e5)
or DM me on [Twitter](https://twitter.com/ful1e5) if your company would like to support my projects,
I will gladly look into it and post your avatar in the project's README.

I appreciate all the wonderful people who patronize and sponsoring my work.

## Sponsors

<!-- Add your name or avatar here with the Pull Request in case I missed it. -->

N/A

---

![Bibata Amber](https://i.imgur.com/2DEYWDC.png)
![Bibata Classic](https://i.imgur.com/C8mMQ3j.png)
![Bibata Ice](https://i.imgur.com/ovzTw6u.png)

> **Note**
> All cursor's `.svg` files are found in [svg](./svg) directory or you can also find them on
> [Figma](https://www.figma.com/file/Y9RKZLXhSvaxpUzsKGJkp6/Bibata-Cursor?node-id=0%3A1).

## Variants:

- **Bibata Original Amber:** Yellowish and sharp edge bibata cursors.
- **Bibata Modern Amber:** Yellowish and rounded edge bibata cursors.
- **Bibata Original Classic:** Black and sharp edge bibata cursors.
- **Bibata Modern Classic:** Black and rounded edge bibata cursors.
- **Bibata Original Ice:** White and sharp edge bibata cursors.
- **Bibata Modern Ice:** White and rounded edge bibata cursors

## Cursor Sizes

### Xcursor Sizes:

<kbd>22</kbd>
<kbd>24</kbd>
<kbd>28</kbd>
<kbd>32</kbd>
<kbd>40</kbd>
<kbd>48</kbd>
<kbd>56</kbd>
<kbd>64</kbd>
<kbd>72</kbd>
<kbd>80</kbd>
<kbd>88</kbd>
<kbd>96</kbd>

### Windows Cursor Size:

- <kbd>16x16</kbd> - Small
- <kbd>24x24</kbd> - Regular
- <kbd>32x32</kbd> - Large
- <kbd>48x48</kbd> - Extra Large

## Colors:

### Bibata Amber

- Base Color - `#FF8300` (Amber)
- Outline Color - `#FFFFFF` (White)
- Watch Background Color - `#001524` (Rich Black)

### Bibata Classic

- Base Color - `#000000` (Black)
- Outline Color - `#FFFFFF` (White)
- Watch Background Color - `#000000` (Black)

### Bibata Ice

- Base Color - `#FFFFFF` (White)
- Outline Color - `#000000` (Black)
- Watch Background Color - `#FFFFFF` (White)

## How to get it

### Easiest Way

You can download latest `stable` & `development` releases from
[Release Page](https://github.com/ful1e5/Bibata_Cursor/releases).

### Packages

> **Note**
> If you're having trouble with the packages please submit a request to the package maintainer
> before creating an issue.

#### Arch Linux/Manjaro

Arch Linux/Manjaro users can install from the [AUR](https://aur.archlinux.org/packages/bibata-cursor-theme)
currently maintained by [_@Shatur_](https://aur.archlinux.org/packages/?K=Shatur&SeB=m) &
[_@yochananmarqos_](https://aur.archlinux.org/packages/?K=yochananmarqos&SeB=m).
Can be installed via Pamac (preinstalled in Manjaro), Paru or any other
[AUR helper](https://wiki.archlinux.org/index.php/AUR_helpers).

```bash
paru -S bibata-cursor-theme
```

Alternatively, Bibata binaries can be also installed using the PKGBUILD `bibata-theme-bin`,
available on the AUR.

#### Fedora

##### copr-repo by @peterwu (recommended)

```bash
sudo dnf copr enable peterwu/rendezvous
sudo dnf install bibata-cursor-themes
```

##### copr-repo by @muhalantabli

```bash
sudo dnf copr enable muhalantabli/copr-repo
sudo dnf install bibata-cursor-theme
```

## Installing Bibata Cursor

#### Linux/X11

**Installation:**

```bash
tar -xvf Bibata.tar.gz                # extract `Bibata.tar.gz`
mv Bibata-* ~/.icons/                 # Install to local users
sudo mv Bibata-* /usr/share/icons/    # Install to all users
```

**Uninstallation:**

```bash
rm ~/.icons/Bibata-*                  # Remove from local users
sudo rm /usr/share/icons/Bibata-*     # Remove from all users
```

#### Windows

**Installation:**

1. Unzip `.zip` file
2. Open unziped directory in Explorer, and **right click** on `install.inf`.
3. Click 'Install' from the context menu, and authorize the modifications to your system.
4. Open Control Panel > Personalization and Appearance > Change mouse pointers,
   and select **Bibata Cursors**.
5. Click '**Apply**'.

**Uninstallation:**

Run the `uninstall.bat` script packed with the `.zip` archive

**OR** follow these steps:

1. Go to **Registry Editor** by typing the same in the _start search box_.
2. Expand `HKEY_CURRENT_USER` folder and expand `Control Panel` folder.
3. Go to `Cursors` folder and click on `Schemes` folder - all the available custom cursors that are
   installed will be listed here.
4. **Right Click** on the name of cursor file you want to uninstall; for eg.: _Bibata Cursors_ and
   click `Delete`.
5. Click '**yes**' when prompted.

## Build From Source

#### Notes

- Bibata build configuration and cursor hotspot settings are bundled in the `build.toml` file.
- Check out the scripts section in [package.json](./package.json) to see how we build the cursor theme,
  excluding the render scripts. They are useful for converting `.svg` files to `.png` files.
- yarn is optional, For building XCursors and Windows cursors from `.png` files or resizing them
  you don't need that. If you want to develop/modify Bibata's colors, and bitmaps, or generate a png
  file from a svg, Then you can use yarn because bitmapper is written in TypeScript.
- Since Bibata Modern and Bibata Original are designed similarly, they share the same hotspot settings so a
  single configuration file `build.toml` is responsible for building all variants. Due to this, you will have
  to change the following options in `ctgen` to build the appropriate variant:
  - **-d**: bitmaps directory
  - **-n**: The name you want to give to the generated theme.
  - **-c**: Theme comment.
  - See `ctgen --help` for all available options.

### Build prerequisites

- Python version 3.7 or higher
- [clickgen](https://github.com/ful1e5/clickgen)>=2.1.2 (`pip install clickgen`)
- [yarn](https://github.com/yarnpkg/yarn)

### Quick start

1. Install [build prerequisites](#build-prerequisites) on your system
2. `git clone https://github.com/ful1e5/Bibata_Cursor`
3. `cd Bibata_Cursor && yarn build`
4. See [Installing Bibata Cursor](#installing-bibata-cursor).

### Building

> **Note**
> Bitmaps are already generated in the `bitmaps` directory and **managed by the maintainer**
> (do not edit them directly).

First make sure you installed the [build prerequisites](#build-prerequisites).
Now that you have the dependencies, you can try build individual themes from bitmaps and
customize sizes, target platform, and etc. with the `ctgen` CLI (packed with `clickgen`).

#### `yarn build` aberration

Here are the default commands we used to build the Bibata's variants and packed them into `yarn build`:

```bash
ctgen build.toml -d 'bitmaps/Bibata-Modern-Amber' -n 'Bibata-Modern-Amber' -c 'Yellowish and rounded edge bibata cursors.'
ctgen build.toml -d 'bitmaps/Bibata-Modern-Classic' -n 'Bibata-Modern-Classic' -c 'Black and rounded edge Bibata cursors.'
ctgen build.toml -d 'bitmaps/Bibata-Modern-Ice' -n 'Bibata-Modern-Ice' -c 'White and rounded edge Bibata cursors.'

ctgen build.toml -d 'bitmaps/Bibata-Original-Amber' -n 'Bibata-Original-Amber' -c 'Yellowish and sharp edge Bibata cursors.'
ctgen build.toml -d 'bitmaps/Bibata-Original-Classic' -n 'Bibata-Original-Classic' -c 'Black and sharp edge Bibata cursors.'
ctgen build.toml -d 'bitmaps/Bibata-Original-Ice' -n 'Bibata-Original-Ice' -c 'White and sharp edge Bibata cursors.'
```

Afterwards, the themes can be found in the `themes` directory.

#### Customize Sizes

> **Note**
> You can change the cursor size up to 200 because pngs are rendered with 200x200.
> If the cursor is resized by more than rendered png size, the final cursor will be blurred.

##### Customize Windows Cursor size

To build Windows cursor with size `16`:

> **Warning**
> Windows cursor supports only one size, if multiple sizes are given with `-s` the first size will
> be considered in build.

```bash
ctgen build.toml -s 16 -p windows -d 'bitmaps/Bibata-Modern-Ice' -n 'Bibata-Modern-Ice' -c 'White and rounded egde bibata cusors with size 16'
```

You can also customize output directory with `-o` option:

```bash
ctgen build.toml -s 16 -p windows -d 'bitmaps/Bibata-Modern-Ice' -o 'out' -n 'Bibata-Modern-Ice' -c 'White and rounded egde Bibata cursors with size 16'
```

##### Customize XCursor size

To build XCursor with size `16`:

```bash
ctgen build.toml -s 16 -p x11 -d 'bitmaps/Bibata-Modern-Ice' -n 'Bibata-Modern-Ice' -c 'White and rounded egde Bibata cursors with size 16'
```

You can also assign multiple sizes to `ctgen` for XCursors build:

```bash
ctgen build.toml -s 16 24 32 -p x11 -d 'bitmaps/Bibata-Modern-Ice' -n 'Bibata-Modern-Ice' -c 'Custom white and rounded egde Bibata cursors'
```

#### Customize Colors

To customize bibata's color you have to install node dependencies with `yarn install` command.
After installing dependencies you can customize the colors via `npx cbmp` Node CLI App which packed with
[cbmp](https://github.com/ful1e5/cbmp) node package.

##### `yarn render` aberration

Here are the default commands we used for generating the Bibata's bitmaps and packed them into `yarn render`:

```bash
npx cbmp -d 'svg/modern' -n 'Bibata-Modern-Amber' -bc '#FF8300' -oc '#FFFFFF' -wc '#001524'
npx cbmp -d 'svg/modern' -n 'Bibata-Modern-Classic' -bc '#000000' -oc '#FFFFFF'
npx cbmp -d 'svg/modern' -n 'Bibata-Modern-Ice' -bc '#FFFFFF' -oc '#000000'
npx cbmp -d 'svg/original' -n 'Bibata-Original-Amber' -bc '#FF8300' -oc '#FFFFFF' -wc '#001524'
npx cbmp -d 'svg/original' -n 'Bibata-Original-Classic' -bc '#000000' -oc '#FFFFFF'
npx cbmp -d 'svg/original' -n 'Bibata-Original-Ice' -bc '#FFFFFF' -oc '#000000'
```

#### Examples

Lets generate modern Bibata with green base color and black outline:

```bash
npx cbmp -d 'svg/modern' -n 'Bibata-Hacker' -bc '#00FE00' -oc '#000000' -wc '#001524'
```

After rendering custom color you have to build cursor through `ctgen`:

```bash
ctgen build.toml -d 'bitmaps/Bibata-Hacker' -n 'Bibata-Hacker' -c 'Green and black Bibata cursors.'
```

Afterwards, Generated theme can be found in the `themes` directory.

###### Bibata Gruvbox

```bash
npx cbmp -d 'svg/original' -n 'Bibata-Gruvbox' -bc '#282828' -oc '#EBDBB2' -wc '#000000'
ctgen build.toml -d 'bitmaps/Bibata-Gruvbox' -n 'Bibata-Gruvbox' -c 'Groovy Bibata cursors.'
```

###### Bibata Solarized Dark

```bash
npx cbmp -d 'svg/original' -n 'Bibata-Solarized-Dark' -bc '#002b36' -oc '#839496' -wc '#000000'
ctgen build.toml -d 'bitmaps/Bibata-Solarized-Dark' -n 'Bibata-Solarized-Dark' -c 'Solarized Dark Bibata cursors.'
```

###### Bibata Solarized Light

```bash
npx cbmp -d 'svg/original' -n 'Bibata-Solarized-Light' -bc '#839496' -oc '#002b36'
ctgen build.toml -d 'bitmaps/Bibata-Solarized-Light' -n 'Bibata-Solarized-Light' -c 'Solarized Light Bibata cursors.'
```

###### Bibata Dracula

```bash
npx cbmp -d 'svg/original' -n 'Bibata-Dracula' -bc '#282a36' -oc '#f8f8f2'
ctgen build.toml -d 'bitmaps/Bibata-Dracula' -n 'Bibata-Dracula' -c 'Dracula Bibata cursors.'
```

## You may also like...

- [**Bibata Adapta**](https://gitlab.com/cscs/Bibata_AdaptaBreath_Cursors) - Bibata Based Cursor Made for AdaptaBreath and Manjaro.
- [**Bibata Extra**](https://github.com/ful1e5/Bibata_Extra_Cursor) - More Bibata!
- [**Bibata Rainbow**](https://github.com/ful1e5/Bibata_Cursor_Rainbow) - 'Semi-Animated' Bibata cursors with rainbow colors
- [**Bibata Zebra**](https://github.com/ful1e5/Bibata-Zebra-Cursor) - Bibata cursor with a semi-animated strip
- [**Bibata Bee**](https://github.com/ful1e5/Bibata-Bee-Cursor) - 'Semi-Animated' Bibata cursors with bee stripes
- [**Bibata Translucent**](https://github.com/Silicasandwhich/Bibata_Cursor_Translucent) - Bibata translucent is a translucent flavor of the Bibata.

## Credit

[Wedge Loading Animation](https://loading.io/spinner/wedges/-pie-wedge-pizza-circle-round-rotate) ·
[Adwaita](https://github.com/GNOME/adwaita-icon-theme) ·
[Dmz](https://github.com/GalliumOS/dmz-cursor-theme) ·
[Yaru](https://github.com/ubuntu/yaru)

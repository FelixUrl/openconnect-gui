# OpenConnect GUI (fork with custom User-Agent)

> **This is a fork of [openconnect/openconnect-gui](https://gitlab.com/openconnect/openconnect-gui) on GitLab.**
>
> The only functional change is a new per-profile **User Agent** option.
> Some Cisco (AnyConnect / ASA) servers have policies that reject or complain
> about unknown VPN clients based on the HTTP `User-Agent`. With this option you
> can set the string the client sends (for example `AnyConnect`) so such
> servers accept the connection.
>
> ### Usage
>
> Open a profile in the edit dialog and fill in the **User Agent** field.
> Leave it empty to keep the default behaviour. A pasted command-line style
> value such as `--useragent="AnyConnect"` is accepted too; the prefix and
> quotes are stripped automatically.
>
> The value is stored in the profile as `user-agent` and applied through
> `openconnect_set_useragent()`, which requires libopenconnect API 5.8 or newer.
> With older libopenconnect versions the option is ignored.
>
> Everything else is identical to upstream. See the upstream project for
> documentation, releases and support.

---

This is the development space of OpenConnect VPN graphical client (GUI).
See the [OpenConnect VPN GUI web site](https://gui.openconnect-vpn.net/)
for detailed description, screen shots and other related projects.

## Development info
- [Compilation](docs/dev.md)
- [Development with QtCreator](docs/dev_QtCreator.md)

## Other
- [Creating release package](docs/release.md)
- [OpenConnect library compilation and dependencies](docs/openconnect.md)
- [Web page maintenance](https://gitlab.com/openconnect/openconnect-gui-web)
- [Snapshot builds](docs/snapshots.md)
- [AppVeyor CI builds](https://ci.appveyor.com/project/nmav/openconnect-gui/history)

# License
The content of this project itself is licensed under the [GNU General Public License v2](LICENSE.txt)

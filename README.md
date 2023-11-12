<p align="center">
  <a href="#build-framework">
   <img src="https://raw.githubusercontent.com/armbian/build/master/.github/armbian-logo.png" alt="Armbian logo" width="144">
  </a><br>
  <strong>Armbian OS</strong><br>
<br>
<a href=https://github.com/armbian/os/actions/workflows/complete-artifact-matrix-all.yml><img alt="GitHub Workflow Status" src="https://img.shields.io/github/actions/workflow/status/armbian/os/complete-artifact-matrix-all.yml?logo=githubactions&label=Artifacts%20make&style=for-the-badge&branch=main"></a>
<a href=https://github.com/armbian/os/actions/workflows/repository-update.yml><img alt="GitHub Workflow Status" src="https://img.shields.io/github/actions/workflow/status/armbian/os/repository-update.yml?logo=githubactions&label=Repository%20update&style=for-the-badge&branch=main"></a>
<a href=https://github.com/armbian/os#latest-smoke-tests-results><img alt="GitHub Workflow Status" src="https://img.shields.io/github/actions/workflow/status/armbian/os/smoke-tests.yml?logo=githubactions&label=Smoke%20tests&style=for-the-badge&branch=main"></a>
</p>


# What does this project do?

- Keeps build framework [packages artifacts](https://github.com/orgs/armbian/packages) cache up to date
- Keeps stable [apt.armbian.com](https://apt.armbian.com) and nightly [beta.armbian.com](https://beta.armbian.com) packages repository up to date
- Builds [nightly](https://github.com/armbian/os/releases) and [stable images](https://www.armbian.com/download/) and uploads them to Armbian CDN
- Keep synchronizing the selection of [3rd party](external) applications with Armbian repositories
- Tests install of all packages added onto stable and testing Debian and Ubuntu releases

# How to enable images?

If you want to enable build configurations, edit [yaml config files](userpatches) and send a pull request. ([example](https://github.com/armbian/os/commit/70f3be4f3d96e9a301be751d3ecf3a24394356f9) )

# When is this happening?

- Artifacts cache is updated every eight hours, starting at 0:00 AM UTC
- Repository update starts after **artifacts cache update** is done succesfully.
- Smoke tests starts **manually**.
- Nightly images are build once per day, at 2:00 AM UTC, or if [build config is changed](https://github.com/armbian/os/blob/main/userpatches/targets-release-nightly.yaml)
- Manually, when Armbian [release manager](https://github.com/orgs/armbian/teams/release-manager) executes a build action

# Latest smoke tests results:

- installs kernels, dtb and headers that are defined and supported by the board
- runs network and computing performance tests (7z benchmark)
- store armbianmonitor logs

<!--START_SECTION:data-section-->
<table width="100%"><tr><td align="left"><a id=Board ID href=#Board ID><b>Board name</b></a> Board type</td><td align=left><b>Logs</b></td><td align=right><b>Branch</b></td><td align=right><b>Iperf</b></td><td align=right><b>7z -b</b></td><td align=right><b>Repo</b></td></tr><tr><td align="left"><a id=pineh64 href=#pineh64>Pine H64</a> csc</td><td align=left>https://paste.armbian.com/puhajadaza</td><td align=right>current</td><td align=right>660</td><td align=right>4269</td><td align=right>beta</td></tr><tr><td align="left"><a id=pineh64 href=#pineh64>Pine H64</a> csc</td><td align=left>https://paste.armbian.com/exumizeziy</td><td align=right>current</td><td align=right>881</td><td align=right>4189</td><td align=right>stable</td></tr><tr><td align="left"><a id=pineh64 href=#pineh64>Pine H64</a> csc</td><td align=left>https://paste.armbian.com/uzucawavuf</td><td align=right>edge</td><td align=right>874</td><td align=right>4154</td><td align=right>beta</td></tr><tr><td align="left"><a id=pineh64 href=#pineh64>Pine H64</a> csc</td><td align=left>https://paste.armbian.com/kupewalega</td><td align=right>edge</td><td align=right>615</td><td align=right>4250</td><td align=right>stable</td></tr><tr><td align="left"><a id=zeropi href=#zeropi>ZeroPi</a> csc</td><td align=left>https://paste.armbian.com/omexeyigop</td><td align=right>legacy</td><td align=right>562</td><td align=right>2658</td><td align=right>beta</td></tr><tr><td align="left"><a id=orangepiprime href=#orangepiprime>Orange Pi Prime</a> conf</td><td align=left>https://paste.armbian.com/bacuwohati</td><td align=right>legacy</td><td align=right>812</td><td align=right>2329</td><td align=right>beta</td></tr><tr><td align="left"><a id=clearfogpro href=#clearfogpro>Clearfog Pro</a> conf</td><td align=left>n/a</td><td align=right>current</td><td align=right>n/a</td><td align=right>n/a</td><td align=right></td></tr><tr><td align="left"><a id=clearfogpro href=#clearfogpro>Clearfog Pro</a> conf</td><td align=left>n/a</td><td align=right>current</td><td align=right>n/a</td><td align=right>n/a</td><td align=right></td></tr><tr><td align="left"><a id=clearfogpro href=#clearfogpro>Clearfog Pro</a> conf</td><td align=left>n/a</td><td align=right>edge</td><td align=right>n/a</td><td align=right>n/a</td><td align=right></td></tr><tr><td align="left"><a id=clearfogpro href=#clearfogpro>Clearfog Pro</a> conf</td><td align=left>n/a</td><td align=right>edge</td><td align=right>n/a</td><td align=right>n/a</td><td align=right></td></tr><tr><td align="left"><a id=bananapim2ultra href=#bananapim2ultra>Banana Pi M2 Ultra</a> csc</td><td align=left>https://paste.armbian.com/ohelihuvag</td><td align=right>current</td><td align=right>804</td><td align=right>2717</td><td align=right>beta</td></tr><tr><td align="left"><a id=bananapim2ultra href=#bananapim2ultra>Banana Pi M2 Ultra</a> csc</td><td align=left>https://paste.armbian.com/tucalepexi</td><td align=right>current</td><td align=right>782</td><td align=right>2704</td><td align=right>stable</td></tr><tr><td align="left"><a id=lepotato href=#lepotato>Le potato</a> conf</td><td align=left>n/a</td><td align=right>current</td><td align=right>n/a</td><td align=right>n/a</td><td align=right></td></tr><tr><td align="left"><a id=lepotato href=#lepotato>Le potato</a> conf</td><td align=left>n/a</td><td align=right>current</td><td align=right>n/a</td><td align=right>n/a</td><td align=right></td></tr><tr><td align="left"><a id=lepotato href=#lepotato>Le potato</a> conf</td><td align=left>n/a</td><td align=right>edge</td><td align=right>n/a</td><td align=right>n/a</td><td align=right></td></tr><tr><td align="left"><a id=lepotato href=#lepotato>Le potato</a> conf</td><td align=left>n/a</td><td align=right>edge</td><td align=right>n/a</td><td align=right>n/a</td><td align=right></td></tr><tr><td align="left"><a id=odroidm1 href=#odroidm1>ODROID M1</a> wip</td><td align=left>n/a</td><td align=right>edge</td><td align=right>n/a</td><td align=right>n/a</td><td align=right></td></tr><tr><td align="left"><a id=odroidm1 href=#odroidm1>ODROID M1</a> wip</td><td align=left>n/a</td><td align=right>edge</td><td align=right>n/a</td><td align=right>n/a</td><td align=right></td></tr><tr><td align="left"><a id=orangepi5 href=#orangepi5>Orange Pi 5</a> conf</td><td align=left>https://paste.armbian.com/piyugalomi</td><td align=right>legacy</td><td align=right>890</td><td align=right>15668</td><td align=right>beta</td></tr><tr><td align="left"><a id=orangepi5 href=#orangepi5>Orange Pi 5</a> conf</td><td align=left>https://paste.armbian.com/tugaxuwore</td><td align=right>legacy</td><td align=right>700</td><td align=right>15533</td><td align=right>stable</td></tr><tr><td align="left"><a id=nanopineo3 href=#nanopineo3>NanoPi Neo 3</a> csc</td><td align=left>n/a</td><td align=right>current</td><td align=right>n/a</td><td align=right>n/a</td><td align=right></td></tr><tr><td align="left"><a id=nanopineo3 href=#nanopineo3>NanoPi Neo 3</a> csc</td><td align=left>n/a</td><td align=right>current</td><td align=right>n/a</td><td align=right>n/a</td><td align=right></td></tr><tr><td align="left"><a id=nanopineo3 href=#nanopineo3>NanoPi Neo 3</a> csc</td><td align=left>n/a</td><td align=right>edge</td><td align=right>n/a</td><td align=right>n/a</td><td align=right></td></tr><tr><td align="left"><a id=nanopineo3 href=#nanopineo3>NanoPi Neo 3</a> csc</td><td align=left>n/a</td><td align=right>edge</td><td align=right>n/a</td><td align=right>n/a</td><td align=right></td></tr><tr><td align="left"><a id=uefi-x86 href=#uefi-x86>UEFI x86</a> conf</td><td align=left>n/a</td><td align=right>legacy</td><td align=right>n/a</td><td align=right>n/a</td><td align=right></td></tr><tr><td align="left"><a id=uefi-x86 href=#uefi-x86>UEFI x86</a> conf</td><td align=left>n/a</td><td align=right>legacy</td><td align=right>n/a</td><td align=right>n/a</td><td align=right></td></tr><tr><td align="left"><a id=uefi-x86 href=#uefi-x86>UEFI x86</a> conf</td><td align=left>n/a</td><td align=right>current</td><td align=right>n/a</td><td align=right>n/a</td><td align=right></td></tr><tr><td align="left"><a id=uefi-x86 href=#uefi-x86>UEFI x86</a> conf</td><td align=left>n/a</td><td align=right>current</td><td align=right>n/a</td><td align=right>n/a</td><td align=right></td></tr><tr><td align="left"><a id=uefi-x86 href=#uefi-x86>UEFI x86</a> conf</td><td align=left>n/a</td><td align=right>edge</td><td align=right>n/a</td><td align=right>n/a</td><td align=right></td></tr><tr><td align="left"><a id=uefi-x86 href=#uefi-x86>UEFI x86</a> conf</td><td align=left>n/a</td><td align=right>edge</td><td align=right>n/a</td><td align=right>n/a</td><td align=right></td></tr><tr><td align="left"><a id=rockpi-4b href=#rockpi-4b>Rockpi 4B</a> csc</td><td align=left>n/a</td><td align=right>current</td><td align=right>n/a</td><td align=right>n/a</td><td align=right></td></tr><tr><td align="left"><a id=rockpi-4b href=#rockpi-4b>Rockpi 4B</a> csc</td><td align=left>n/a</td><td align=right>current</td><td align=right>n/a</td><td align=right>n/a</td><td align=right></td></tr><tr><td align="left"><a id=rockpi-4b href=#rockpi-4b>Rockpi 4B</a> csc</td><td align=left>n/a</td><td align=right>edge</td><td align=right>n/a</td><td align=right>n/a</td><td align=right></td></tr><tr><td align="left"><a id=rockpi-4b href=#rockpi-4b>Rockpi 4B</a> csc</td><td align=left>n/a</td><td align=right>edge</td><td align=right>n/a</td><td align=right>n/a</td><td align=right></td></tr><tr><td align="left"><a id=khadas-vim2 href=#khadas-vim2>Khadas VIM2</a> conf</td><td align=left>n/a</td><td align=right>current</td><td align=right>n/a</td><td align=right>n/a</td><td align=right></td></tr><tr><td align="left"><a id=khadas-vim2 href=#khadas-vim2>Khadas VIM2</a> conf</td><td align=left>n/a</td><td align=right>current</td><td align=right>n/a</td><td align=right>n/a</td><td align=right></td></tr><tr><td align="left"><a id=khadas-vim2 href=#khadas-vim2>Khadas VIM2</a> conf</td><td align=left>n/a</td><td align=right>edge</td><td align=right>n/a</td><td align=right>n/a</td><td align=right></td></tr><tr><td align="left"><a id=khadas-vim2 href=#khadas-vim2>Khadas VIM2</a> conf</td><td align=left>n/a</td><td align=right>edge</td><td align=right>n/a</td><td align=right>n/a</td><td align=right></td></tr><tr><td align="left"><a id=khadas-vim1 href=#khadas-vim1>Khadas VIM1</a> conf</td><td align=left>n/a</td><td align=right>current</td><td align=right>n/a</td><td align=right>n/a</td><td align=right></td></tr><tr><td align="left"><a id=khadas-vim1 href=#khadas-vim1>Khadas VIM1</a> conf</td><td align=left>n/a</td><td align=right>current</td><td align=right>n/a</td><td align=right>n/a</td><td align=right></td></tr><tr><td align="left"><a id=khadas-vim1 href=#khadas-vim1>Khadas VIM1</a> conf</td><td align=left>n/a</td><td align=right>edge</td><td align=right>n/a</td><td align=right>n/a</td><td align=right></td></tr><tr><td align="left"><a id=khadas-vim1 href=#khadas-vim1>Khadas VIM1</a> conf</td><td align=left>n/a</td><td align=right>edge</td><td align=right>n/a</td><td align=right>n/a</td><td align=right></td></tr><tr><td align="left"><a id=bigtreetech-cb1 href=#bigtreetech-cb1>BigTreeTech CB1</a> conf</td><td align=left>n/a</td><td align=right>legacy</td><td align=right>n/a</td><td align=right>n/a</td><td align=right></td></tr><tr><td align="left"><a id=bigtreetech-cb1 href=#bigtreetech-cb1>BigTreeTech CB1</a> conf</td><td align=left>n/a</td><td align=right>legacy</td><td align=right>n/a</td><td align=right>n/a</td><td align=right></td></tr><tr><td align="left"><a id=orangepizero2 href=#orangepizero2>Orange Pi Zero2</a> conf</td><td align=left>n/a</td><td align=right>current</td><td align=right>n/a</td><td align=right>n/a</td><td align=right></td></tr><tr><td align="left"><a id=orangepizero2 href=#orangepizero2>Orange Pi Zero2</a> conf</td><td align=left>n/a</td><td align=right>current</td><td align=right>n/a</td><td align=right>n/a</td><td align=right></td></tr><tr><td align="left"><a id=orangepizero2 href=#orangepizero2>Orange Pi Zero2</a> conf</td><td align=left>n/a</td><td align=right>edge</td><td align=right>n/a</td><td align=right>n/a</td><td align=right></td></tr><tr><td align="left"><a id=orangepizero2 href=#orangepizero2>Orange Pi Zero2</a> conf</td><td align=left>n/a</td><td align=right>edge</td><td align=right>n/a</td><td align=right>n/a</td><td align=right></td></tr><tr><td align="left"><a id=orangepi4-lts href=#orangepi4-lts>Orange Pi 4 LTS</a> conf</td><td align=left>n/a</td><td align=right>current</td><td align=right>n/a</td><td align=right>n/a</td><td align=right></td></tr><tr><td align="left"><a id=orangepi4-lts href=#orangepi4-lts>Orange Pi 4 LTS</a> conf</td><td align=left>n/a</td><td align=right>current</td><td align=right>n/a</td><td align=right>n/a</td><td align=right></td></tr><tr><td align="left"><a id=orangepi4-lts href=#orangepi4-lts>Orange Pi 4 LTS</a> conf</td><td align=left>n/a</td><td align=right>edge</td><td align=right>n/a</td><td align=right>n/a</td><td align=right></td></tr><tr><td align="left"><a id=orangepi4-lts href=#orangepi4-lts>Orange Pi 4 LTS</a> conf</td><td align=left>n/a</td><td align=right>edge</td><td align=right>n/a</td><td align=right>n/a</td><td align=right></td></tr><tr><td align="left"><a id=odroidc2 href=#odroidc2>Odroid C2</a> conf</td><td align=left>n/a</td><td align=right>current</td><td align=right>n/a</td><td align=right>n/a</td><td align=right></td></tr><tr><td align="left"><a id=odroidc2 href=#odroidc2>Odroid C2</a> conf</td><td align=left>n/a</td><td align=right>current</td><td align=right>n/a</td><td align=right>n/a</td><td align=right></td></tr><tr><td align="left"><a id=odroidc2 href=#odroidc2>Odroid C2</a> conf</td><td align=left>n/a</td><td align=right>edge</td><td align=right>n/a</td><td align=right>n/a</td><td align=right></td></tr><tr><td align="left"><a id=odroidc2 href=#odroidc2>Odroid C2</a> conf</td><td align=left>n/a</td><td align=right>edge</td><td align=right>n/a</td><td align=right>n/a</td><td align=right></td></tr><tr><td align="left"><a id=rockpro64 href=#rockpro64>RockPro 64</a> conf</td><td align=left>n/a</td><td align=right>current</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>beta</td></tr><tr><td align="left"><a id=rockpro64 href=#rockpro64>RockPro 64</a> conf</td><td align=left>n/a</td><td align=right>current</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>beta</td></tr><tr><td align="left"><a id=rockpro64 href=#rockpro64>RockPro 64</a> conf</td><td align=left>n/a</td><td align=right>edge</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>beta</td></tr><tr><td align="left"><a id=rockpro64 href=#rockpro64>RockPro 64</a> conf</td><td align=left>n/a</td><td align=right>edge</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>beta</td></tr><tr><td align="left"><a id=odroidc4 href=#odroidc4>Odroid C4</a> csc</td><td align=left>https://paste.armbian.com/luzexoveba</td><td align=right>current</td><td align=right>880</td><td align=right>5640</td><td align=right>beta</td></tr><tr><td align="left"><a id=odroidc4 href=#odroidc4>Odroid C4</a> csc</td><td align=left>https://paste.armbian.com/oxuhanajap</td><td align=right>current</td><td align=right>880</td><td align=right>5598</td><td align=right>stable</td></tr><tr><td align="left"><a id=odroidc4 href=#odroidc4>Odroid C4</a> csc</td><td align=left>https://paste.armbian.com/upafafuxij</td><td align=right>edge</td><td align=right>890</td><td align=right>5623</td><td align=right>beta</td></tr><tr><td align="left"><a id=odroidc4 href=#odroidc4>Odroid C4</a> csc</td><td align=left>https://paste.armbian.com/vutemuvane</td><td align=right>edge</td><td align=right>880</td><td align=right>5638</td><td align=right>stable</td></tr><tr><td align="left"><a id=orangepizero href=#orangepizero>Orange Pi Zero</a> csc</td><td align=left>n/a</td><td align=right>current</td><td align=right>n/a</td><td align=right>n/a</td><td align=right></td></tr><tr><td align="left"><a id=orangepizero href=#orangepizero>Orange Pi Zero</a> csc</td><td align=left>n/a</td><td align=right>current</td><td align=right>n/a</td><td align=right>n/a</td><td align=right></td></tr><tr><td align="left"><a id=orangepi-r1 href=#orangepi-r1>Orange Pi R1</a> conf</td><td align=left>n/a</td><td align=right>current</td><td align=right>n/a</td><td align=right>n/a</td><td align=right></td></tr><tr><td align="left"><a id=orangepi-r1 href=#orangepi-r1>Orange Pi R1</a> conf</td><td align=left>n/a</td><td align=right>current</td><td align=right>n/a</td><td align=right>n/a</td><td align=right></td></tr><tr><td align="left"><a id=orangepi-r1 href=#orangepi-r1>Orange Pi R1</a> conf</td><td align=left>n/a</td><td align=right>edge</td><td align=right>n/a</td><td align=right>n/a</td><td align=right></td></tr><tr><td align="left"><a id=orangepi-r1 href=#orangepi-r1>Orange Pi R1</a> conf</td><td align=left>n/a</td><td align=right>edge</td><td align=right>n/a</td><td align=right>n/a</td><td align=right></td></tr><tr><td align="left"><a id=orangepizeroplus href=#orangepizeroplus>Orange Pi Zero Plus</a> conf</td><td align=left>n/a</td><td align=right>current</td><td align=right>n/a</td><td align=right>n/a</td><td align=right></td></tr><tr><td align="left"><a id=orangepizeroplus href=#orangepizeroplus>Orange Pi Zero Plus</a> conf</td><td align=left>n/a</td><td align=right>current</td><td align=right>n/a</td><td align=right>n/a</td><td align=right></td></tr><tr><td align="left"><a id=orangepizeroplus href=#orangepizeroplus>Orange Pi Zero Plus</a> conf</td><td align=left>n/a</td><td align=right>edge</td><td align=right>n/a</td><td align=right>n/a</td><td align=right></td></tr><tr><td align="left"><a id=orangepizeroplus href=#orangepizeroplus>Orange Pi Zero Plus</a> conf</td><td align=left>n/a</td><td align=right>edge</td><td align=right>n/a</td><td align=right>n/a</td><td align=right></td></tr><tr><td align="left"><a id=tinkerboard href=#tinkerboard>Tinker Board</a> conf</td><td align=left>n/a</td><td align=right>current</td><td align=right>n/a</td><td align=right>n/a</td><td align=right></td></tr><tr><td align="left"><a id=tinkerboard href=#tinkerboard>Tinker Board</a> conf</td><td align=left>n/a</td><td align=right>current</td><td align=right>n/a</td><td align=right>n/a</td><td align=right></td></tr><tr><td align="left"><a id=tinkerboard-2 href=#tinkerboard-2>Tinker Board 2</a> csc</td><td align=left>n/a</td><td align=right>current</td><td align=right>n/a</td><td align=right>n/a</td><td align=right></td></tr><tr><td align="left"><a id=tinkerboard-2 href=#tinkerboard-2>Tinker Board 2</a> csc</td><td align=left>n/a</td><td align=right>current</td><td align=right>n/a</td><td align=right>n/a</td><td align=right></td></tr><tr><td align="left"><a id=odroidn2 href=#odroidn2>Odroid N2</a> csc</td><td align=left>n/a</td><td align=right>current</td><td align=right>n/a</td><td align=right>n/a</td><td align=right></td></tr><tr><td align="left"><a id=odroidn2 href=#odroidn2>Odroid N2</a> csc</td><td align=left>n/a</td><td align=right>current</td><td align=right>n/a</td><td align=right>n/a</td><td align=right></td></tr><tr><td align="left"><a id=odroidn2 href=#odroidn2>Odroid N2</a> csc</td><td align=left>n/a</td><td align=right>edge</td><td align=right>n/a</td><td align=right>n/a</td><td align=right></td></tr><tr><td align="left"><a id=odroidn2 href=#odroidn2>Odroid N2</a> csc</td><td align=left>n/a</td><td align=right>edge</td><td align=right>n/a</td><td align=right>n/a</td><td align=right></td></tr><tr><td align="left"><a id=odroidxu4 href=#odroidxu4>Odroid XU4</a> conf</td><td align=left>n/a</td><td align=right>current</td><td align=right>n/a</td><td align=right>n/a</td><td align=right></td></tr><tr><td align="left"><a id=odroidxu4 href=#odroidxu4>Odroid XU4</a> conf</td><td align=left>n/a</td><td align=right>current</td><td align=right>n/a</td><td align=right>n/a</td><td align=right></td></tr><tr><td align="left"><a id=bananapicm4io href=#bananapicm4io>Banana Pi CM4IO</a> conf</td><td align=left>https://paste.armbian.com/bumahusifi</td><td align=right>current</td><td align=right>890</td><td align=right>9269</td><td align=right>beta</td></tr><tr><td align="left"><a id=bananapicm4io href=#bananapicm4io>Banana Pi CM4IO</a> conf</td><td align=left>https://paste.armbian.com/biwitakoda</td><td align=right>current</td><td align=right>880</td><td align=right>8992</td><td align=right>stable</td></tr><tr><td align="left"><a id=bananapicm4io href=#bananapicm4io>Banana Pi CM4IO</a> conf</td><td align=left>https://paste.armbian.com/izuvivesab</td><td align=right>edge</td><td align=right>870</td><td align=right>8921</td><td align=right>beta</td></tr><tr><td align="left"><a id=bananapicm4io href=#bananapicm4io>Banana Pi CM4IO</a> conf</td><td align=left>https://paste.armbian.com/zusikozeko</td><td align=right>edge</td><td align=right>870</td><td align=right>8765</td><td align=right>stable</td></tr><tr><td align="left"><a id=udoo href=#udoo>Udoo</a> csc</td><td align=left>https://paste.armbian.com/milagubagi</td><td align=right>current</td><td align=right>371</td><td align=right>2399</td><td align=right>beta</td></tr><tr><td align="left"><a id=udoo href=#udoo>Udoo</a> csc</td><td align=left>https://paste.armbian.com/eyebukerer</td><td align=right>current</td><td align=right>368</td><td align=right>2400</td><td align=right>stable</td></tr><tr><td align="left"><a id=rock-5b href=#rock-5b>Rock 5B</a> conf</td><td align=left>https://paste.armbian.com/ujotutaxud</td><td align=right>legacy</td><td align=right>2450</td><td align=right>15661</td><td align=right>beta</td></tr><tr><td align="left"><a id=rock-5b href=#rock-5b>Rock 5B</a> conf</td><td align=left>https://paste.armbian.com/hiniguxagi</td><td align=right>legacy</td><td align=right>2250</td><td align=right>15350</td><td align=right>stable</td></tr><tr><td align="left"><a id=khadas-edge2 href=#khadas-edge2>Khadas Edge2</a> conf</td><td align=left>n/a</td><td align=right>legacy</td><td align=right>n/a</td><td align=right>n/a</td><td align=right></td></tr><tr><td align="left"><a id=khadas-edge2 href=#khadas-edge2>Khadas Edge2</a> conf</td><td align=left>n/a</td><td align=right>legacy</td><td align=right>n/a</td><td align=right>n/a</td><td align=right></td></tr></table>
<!--END_SECTION:data-section-->

## Would you like to join spare hardware to this automated testings?

All you need to do is:

- deploy any latest Armbian image to hardware
- provide IP address
- [contact us](https://www.armbian.com/contact/)

Device has to be always on and easily accesible for you to re-image in case of failed upgrade.

## Development

- [Pull request](https://github.com/armbian/build/pulls)
- [Weekly developers meetings](https://forum.armbian.com/events/)
- [Forums for developers](https://forum.armbian.com/forum/4-advanced-users-development/)

## OS download

- [Download](https://www.armbian.com/download/)

## Support

- [Using Armbian](https://forum.armbian.com/forum/23-using-armbian/)

## Contact

- [Forums](https://forum.armbian.com) for Participate in Armbian
- IRC: `#armbian` on Libera.chat
- Discord: [https://discord.gg/armbian](https://discord.gg/armbian)
- Follow [@armbian](https://twitter.com/armbian) on X (formerly known as Twitter), [Fosstodon](https://fosstodon.org/@armbian) or [LinkedIn](https://www.linkedin.com/company/armbian).
- Bugs: [issues](https://github.com/armbian/build/issues) / [JIRA](https://armbian.atlassian.net/jira/dashboards/10000)
- Office hours: [Wednesday, 12 midday, 18 afternoon, CET](https://calendly.com/armbian/office-hours)

## License

This software is published under the GPL-2.0 License license.

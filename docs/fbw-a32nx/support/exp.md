# Experimental Version

The Experimental version is a test version to find problems, issues and to improve functionality based on your feedback. It is <span style=color:red>**not**</span> meant to be used for **daily use or serious flights with** an Online ATC service.

{--

Currently experimental is geared toward testing the initial version of VNAV. Please use the appropriate discord thread **#cFMS LNAV+VNAV Issue Reports** to discuss any issues.

--}

!!! danger "No Support for Experimental - use at own risk"
    Please do not seek support for the Experimental Version on Discord and only report issues if you have read this page and the reported and known issues.

## Implemented Features for Testing

### Vertical Guidance

- Speed and altitude predictions in the flight plan page, including magenta or amber asterisks.
- Reworked fuel burn and time predictions in the flight plan page (no flight plan B page).
- Pseudowaypoints in the flight plan (SPD/LIM, T/C, T/D, S/C, S/D, DECEL).
- Display of pseudowaypoints on the ND (T/C, T/D, predicted speed changes, etc.)
- Partial implementation of step climbs/descent.
- Linear deviation indication during the descent.
- Following of speed and altitude constraints in the climb phase (credits to tracernz).
- Partial implementation of descent guidance.
- Ability to enter winds for climb, cruise, and descent.

#### ^^Vertical Guidance Planned Implementations^^

These features are not yet available but will be implemented at a later time.

- Time constraints, RTA
- Flight plan B
- Constant Mach segments
- Vertical guidance for RNAV approaches

### flyPadOS Version 3 (EFB)

- Completely new design
- Improved Dashboard
    - Flight info
    - Customizable info section for:
        - Weather
        - Pinned charts
        - Pinned checklists 
        - Maintenance 
- Stateful (remembers tabs and content of pages)
- Improved ground service pages
- Improved pushback tool
- Improved performance calculators
- Improved navigation charts page
    - Improved Navigraph chart support 
        - Current position on chart
        - Fullscreen mode
        - Easier search and selection
    - Support for pinning of charts
- Improved online ATC page
- Improved failure support incl. categories and search
- Interactive checklists incl. autofill and option to pin to dashboard
- Presets for customizable lighting settings and predefined aircraft states
- Improved settings (better structure and more configuration options)
- Onscreen keyboard
- Themes
    - Blue
    - Dark
    - Light

#### ^^EFB Planned Implementations^^

These features are not yet available but are generally planned and might be implemented at a later time.

- Support for local files (PFD, images) - requires local-api server (not yet merged)
- Tooltips and built-in help
- Improvements to pushback page

## Known Issues

### Vertical Guidance Issues

- LNAV does not use VNAV speed predictions yet. This means that an approach path will not be forecasted properly. Furthermore, the T/D (Top of Descent) could be misplaced, since the system expects more track miles.
- The descent guidance does not use the speed margins properly yet. The aircraft does not speed up to catch a profile below it.
- The linear deviation indication (green "yoyo") on the PFD might jump around during the descent. This effect is particularly noticable when new waypoints are sequenced.
- Layout inaccuracies in the MCDU, mostly on the PERF page.
- Predicted speed changes in the descent might seem to show up erratically. The same for the level off arrow while in descent mode.
- Fuel predictions in the MCDU are not very accurate.
- Descent guidance is sensitive to QNH changes. This is partially due to an inaccuracy in MSFS' atmospheric model.
- Winds are not yet taken into account for all phases of flight.

### flyPadOSv3 Issues

- Local files does not work yet. Needs additional feature PR ([local-api](https://github.com/flybywiresim/a32nx/pull/6411/){target=new})
- Fuel page: During flight only Instant is available - buttons do not reflect this (should be greyed out)
- Date in the top left corner shows the wrong day of the week

## How to Report Issues

<!--
!!! warning
    We are not taking issue reports at this time.
-->

!!! warning
    Please read the above Known Issues list and also use the search of Discord to see if your issue has already been reported.

    At this time please only report issues via our Discord channel threads:

    [cFMS LNAV+VNAV Issue Reports [NO SUPPORT]](https://discord.com/channels/738864299392630914/926586416820011098){target=new .md-button}

    [flyPadOS3 Experimental - Issue Reports [NO SUPPORT]](https://discord.com/channels/738864299392630914/926586416820011098){target=new .md-button}

    {--

    Do not expect support or immediate solutions for your issues. We will collect all issues to fix and improve features in testing continuously.

    --}

**Do not open any issues on GitHub for the Experimental Version!**

### Download and Install

See [Installation Guide](../installation.md#downloads).


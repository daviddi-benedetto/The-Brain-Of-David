## January 06, 2024 - Transition to Electron
![[01-06-24 Planr Mockup.png]]
### Key Changes
- Have successfully incorporated Planr into Electron, setup: [[Creating An App With Electron]]
- Has a new local-only content security policy (CSP). Need to transfer all online-transmitted content like fonts, icons, and pictures to locally stored. Below was included in the ```<head>```.
```
<meta http-equiv="Content-Security-Policy" content="default-src 'self'; img-src https://*; child-src 'none';" />
```
## December 12, 2023 - First Log

![[12-23-23 Planr Mockup.png]]
### Key Changes
- First update entry
- Focus on completing the tasks section

# If you suffer from "I literally changed nothing.. why does my app not work anymore!" syndrome... This alias is for you

```
alias nuke='rm -rf node_modules && rm -rf ios/build  && rm -rf ios/Pods && rm -rf android/build && rm -rf --interactive=never ${TMPDIR}react-* ||: && rm -rf --interactive=never ${TMPDIR}metro-* ||: && watchman watch-del-all && yarn cache clean && yarn install --frozen-lockfile && cd ios && pod install && cd .. && cd android && ./gradlew clean && cd ..'
```
You can add this to your terminal profile (.bash_profile, .zshrc, etc..) and watch your apps magically work again after running ```$ nuke``` inside the root folder of your react native project

## Common issues:
If you get an error saying command not found: watchman:
  1. Install watchman (```$ brew install watchman```)
  2. Remove the ```watchman watch-del-all``` bit from the alias
  
If you get any issues with temp folders:
  1. You should know enough to know what command to remove
  2. Who cares about temp folder anyways
  

## Disclaimer: Just for fun. Please don't hold me responsible if something breaks :)

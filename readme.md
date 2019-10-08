This repo is prepared like this:

First get on a network that allows ssh connections to github.com (port 22)

git clone https://github.com/expo/expo --recurse-submodules

git checkout sdk-35  # change 35 to whatever

cd expo
yarn

cd ../tools-public
yarn

cd ../tools
yarn

cd expo-tools
yarn

At this point add any patches you might have to the java code

cd ../../android
./gradle assembleRelease

cd tools/expo-tools
node bin/expo-tools.js abp --sdk-version XX.0.0   #Where XX is the sdk-version

cd ../..

The updated expokit package can be found in the expokit-npm-package directory.

Now make new branch of this repo (expokit) copy the files from expokit-npm-package in and commit/push




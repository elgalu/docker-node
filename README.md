# Leo notes
Remember to edit file [ancient/Dockerfile](./ancient/Dockerfile) and change node version there.

## NodeJS
Example for version 4.2.6, remember to change `lgallucci`

Note some arbitrary directory where this source is cloned:

    cd ~/oss/stups-node/ancient

Note team name used `tip` but use yours, always.

    IMG="registry-write.opensource.zalan.do/tip/node:4.2.6-p0"
    docker build -t ${IMG} .
    docker run -ti ${IMG} node --version #=> v4.2.6

Note username used `lgallucci` as an example

    pierone login --url registry-write.opensource.zalan.do --user lgallucci
    docker push ${IMG}

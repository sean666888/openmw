pipeline {
  agent any
  stages {
    stage('set up deps') {
      steps {
        sh '''add-apt-repository ppa:openmw/openmw
apt-get update
apt-get install git libopenal-dev libopenscenegraph-3.4-dev  libsdl2-dev libqt4-dev libboost-filesystem-dev libboost-thread-dev  libboost-program-options-dev libboost-system-dev  libavcodec-dev libavformat-dev libavutil-dev libswscale-dev libswresample-dev  libbullet-dev libmygui-dev libunshield-dev cmake build-essential  libqt4-opengl-dev'''
      }
    }
    stage('Cmake') {
      steps {
        sh '''mkdir Build
cd Build
cmake ..'''
      }
    }
    stage('make') {
      steps {
        sh '''cd Build
make'''
      }
    }
  }
}
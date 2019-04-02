# Educational Assets Tracker

This is educational project that tracks assets in real time. Applications is designed to track a range of moving assets (such as vehicles) and visualize them on a live map. The applications use a mixture of technologies.

Note: This application implements asset tracking. For use in a production environment, you therefore need a Google Maps APIs Premium Plan license. For more information, see the Google Maps APIs terms of service.

# Overview

The repository consists of a number of components, representing the individual moving parts of the bus tracking system. It includes an Android app, in /android, that's installed on Android devices and deployed on the tracked vehicles. There is /backend, written in Node.js, which receives the locations reported by the Android app, along with a time table provided in GTFS format, and makes regular updates to a Firebase Real Time Database. The client in /map receives the updates from the Firebase database and draws them.

# Directories in this repo

The project contains the following subdirectories, each housing a single component:

## android

The Android app that resides with each asset to be tracked. Once configured, this app keeps its location synced with Firebase, and reports on other metrics, such as battery life.

## backend

The server-side component that manages the state of the Firebase database.

## map

The public web interface that displays asset locations.

# Getting started

To get started with this project you should have **[Node.js](https://nodejs.org/en/)** and **NPM** (Node's package manager) installed.

In each of subdirectories(`/Android Client`, `/backend`, `/map`) you will find instructions on how to setup each component.

Note: **[Node-gyp](https://github.com/nodejs/node-gyp)** might be needed for compiling native addon modules for Node.js in `/backend` subdirectory.

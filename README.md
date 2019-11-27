# _Image Magick_ Open Microservice

> Wrapper for ImageMagick

[![Open Microservice Specification Version](https://img.shields.io/badge/Open%20Microservice-1.0-477bf3.svg)](https://openmicroservices.org) [![Open Microservices Spectrum Chat](https://withspectrum.github.io/badge/badge.svg)](https://spectrum.chat/open-microservices) [![Open Microservices Code of Conduct](https://img.shields.io/badge/Contributor%20Covenant-v1.4%20adopted-ff69b4.svg)](https://github.com/oms-services/.github/blob/master/CODE_OF_CONDUCT.md) [![Open Microservices Commitzen](https://img.shields.io/badge/commitizen-friendly-brightgreen.svg)](http://commitizen.github.io/cz-cli/) [![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](http://makeapullrequest.com) 
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)

## Introduction

This project is an example implementation of the [Open Microservice Specification](https://openmicroservices.org), a standard originally created at [Storyscript](https://storyscript.io) for building highly-portable "microservices" that expose the events, actions, and APIs inside containerized software.

## Getting Started

The `oms` command-line interface allows you to interact with Open Microservices. If you're interested in creating an Open Microservice the CLI also helps validate, test, and debug your `oms.yml` implementation!

See the [oms-cli](https://github.com/microservices/oms) project to learn more!

### Installation

```
npm install -g @microservices/oms
```

## Usage

### Open Microservices CLI Usage

Once you have the [oms-cli](https://github.com/microservices/oms) installed, you can run any of the following commands from within this project's root directory:

#### Actions

##### resize

> Resize image.
##### Action Arguments

| Argument Name | Type | Required | Default | Description |
|:------------- |:---- |:-------- |:--------|:----------- |
| input | `string` | `true` | None | The input image base64 data. |
| height | `int` | `true` | None | The height for resized image. |
| width | `int` | `true` | None | The width for resized image. |


``` shell
oms run resize \ 
    -a input='*****' \ 
    -a height='*****' \ 
    -a width='*****'
```

##### reflect

> Reflect image.
##### Action Arguments

| Argument Name | Type | Required | Default | Description |
|:------------- |:---- |:-------- |:--------|:----------- |
| input | `string` | `true` | None | The input image base64 data. |


``` shell
oms run reflect \ 
    -a input='*****'
```

##### extend

> Extend image size with background colour.
##### Action Arguments

| Argument Name | Type | Required | Default | Description |
|:------------- |:---- |:-------- |:--------|:----------- |
| input | `string` | `true` | None | The input image base64 data. |
| backgroundColour | `string` | `true` | None | The colour for extended image. |
| height | `int` | `true` | None | The height to extend image. |
| width | `int` | `true` | None | The width to extend image. |


``` shell
oms run extend \ 
    -a input='*****' \ 
    -a backgroundColour='*****' \ 
    -a height='*****' \ 
    -a width='*****'
```

##### transparent

> Transparent the selected colour from image.
##### Action Arguments

| Argument Name | Type | Required | Default | Description |
|:------------- |:---- |:-------- |:--------|:----------- |
| input | `string` | `true` | None | The input image base64 data. |
| transparentColour | `string` | `true` | None | The colour from image to transparent. |


``` shell
oms run transparent \ 
    -a input='*****' \ 
    -a transparentColour='*****'
```

##### format

> Convert image from one format to another.
##### Action Arguments

| Argument Name | Type | Required | Default | Description |
|:------------- |:---- |:-------- |:--------|:----------- |
| input | `string` | `true` | None | The input image base64 data. |
| inputExtension | `string` | `true` | None | The input image format. |
| outputExtension | `string` | `true` | None | The output image format. |


``` shell
oms run format \ 
    -a input='*****' \ 
    -a inputExtension='*****' \ 
    -a outputExtension='*****'
```

##### custom

> Customize the image with multiple image editing operations.
##### Action Arguments

| Argument Name | Type | Required | Default | Description |
|:------------- |:---- |:-------- |:--------|:----------- |
| input | `string` | `true` | None | The input image base64 data. |
| customizeInput | `list` | `true` | None | The input for customize image with multiple image process operations 'oilpaint','extend','resize','reflect'. |


``` shell
oms run custom \ 
    -a input='*****' \ 
    -a customizeInput='*****'
```

##### oilpaint

> Applies a special effect filter that simulates an oil painting.
##### Action Arguments

| Argument Name | Type | Required | Default | Description |
|:------------- |:---- |:-------- |:--------|:----------- |
| input | `string` | `true` | None | The input image base64 data. |
| radius | `float` | `true` | None | The radius of the circular neighborhood. |


``` shell
oms run oilpaint \ 
    -a input='*****' \ 
    -a radius='*****'
```

## Contributing

All suggestions in how to improve the specification and this guide are very welcome. Feel free share your thoughts in the Issue tracker, or even better, fork the repository to implement your own ideas and submit a pull request.

[![Edit image-magick on CodeSandbox](https://codesandbox.io/static/img/play-codesandbox.svg)](https://codesandbox.io/s/github/oms-services/image-magick)

This project is guided by [Contributor Covenant](https://github.com/oms-services/.github/blob/master/CODE_OF_CONDUCT.md). Please read out full [Contribution Guidelines](https://github.com/oms-services/.github/blob/master/CONTRIBUTING.md).

## Additional Resources

* [Install the CLI](https://github.com/microservices/oms) - The OMS CLI helps developers create, test, validate, and build microservices.
* [Example OMS Services](https://github.com/oms-services) - Examples of OMS-compliant services written in a variety of languages.
* [Example Language Implementations](https://github.com/microservices) - Find tooling & language implementations in Node, Python, Scala, Java, Clojure.
* [Storyscript Hub](https://hub.storyscript.io) - A public registry of OMS services.
* [Community Chat](https://spectrum.chat/open-microservices) - Have ideas? Questions? Join us on Spectrum.

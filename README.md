[//]: # "This README.md file is auto-generated, all changes to this file will be lost."
[//]: # "To regenerate it, use `python -m synthtool`."
<img src="https://avatars2.githubusercontent.com/u/2810941?v=3&s=96" alt="Google Cloud Platform logo" title="Google Cloud Platform" align="right" height="96" width="96"/>

# [Google Cloud Runtime Config: Node.js Client](https://github.com/googleapis/nodejs-rcloadenv)

[![release level](https://img.shields.io/badge/release%20level-preview-yellow.svg?style=flat)](https://cloud.google.com/terms/launch-stages)
[![npm version](https://img.shields.io/npm/v/@google-cloud/rcloadenv.svg)](https://www.npmjs.org/package/@google-cloud/rcloadenv)




**_THIS REPOSITORY AND PACKAGE WILL BE DEPRECATED IN JULY 2024_**

Node.js implementation of rcloadenv. Wraps execution of a given command and loads variables from the Google Cloud Runtime Config API into that process.


A comprehensive list of changes in each version may be found in
[the CHANGELOG](https://github.com/googleapis/nodejs-rcloadenv/blob/main/CHANGELOG.md).

* [Google Cloud Runtime Config Node.js Client API Reference][client-docs]
* [Google Cloud Runtime Config Documentation][product-docs]
* [github.com/googleapis/nodejs-rcloadenv](https://github.com/googleapis/nodejs-rcloadenv)

Read more about the client libraries for Cloud APIs, including the older
Google APIs Client Libraries, in [Client Libraries Explained][explained].

[explained]: https://cloud.google.com/apis/docs/client-libraries-explained

**Table of contents:**


* [Quickstart](#quickstart)

  * [Installing the client library](#installing-the-client-library)
  * [Using the client library](#using-the-client-library)
* [Samples](#samples)
* [Versioning](#versioning)
* [Contributing](#contributing)
* [License](#license)

## Quickstart

### Installing the client library

```bash
npm install @google-cloud/rcloadenv
```


### Using the client library

```javascript
// import the npm module
const rcloadenv = require('@google-cloud/rcloadenv');

async function quickstart() {
  // Just load raw variables from the Runtime Config service:
  const vars = await rcloadenv.getVariables('my-config');
  console.log(`${vars.length} variables found!`);
  vars.forEach(console.log);

  // Load the variables and apply them to the current environment
  await rcloadenv.getAndApply('my-config');
  console.log(process.env.fruit);

  // Load the variables and mix them into a provided object
  const newEnv = Object.assign({}, process.env);
  const env = await rcloadenv.getAndApply('my-config', newEnv);
  console.log(env.veggie);
}
quickstart();

```



## Samples

Samples are in the [`samples/`](https://github.com/googleapis/nodejs-rcloadenv/tree/main/samples) directory. Each sample's `README.md` has instructions for running its sample.

| Sample                      | Source Code                       | Try it |
| --------------------------- | --------------------------------- | ------ |
| Quickstart | [source code](https://github.com/googleapis/nodejs-rcloadenv/blob/main/samples/quickstart.js) | [![Open in Cloud Shell][shell_img]](https://console.cloud.google.com/cloudshell/open?git_repo=https://github.com/googleapis/nodejs-rcloadenv&page=editor&open_in_editor=samples/quickstart.js,samples/README.md) |



The [Google Cloud Runtime Config Node.js Client API Reference][client-docs] documentation
also contains samples.

## Supported Node.js Versions

Our client libraries follow the [Node.js release schedule](https://github.com/nodejs/release#release-schedule).
Libraries are compatible with all current _active_ and _maintenance_ versions of
Node.js.
If you are using an end-of-life version of Node.js, we recommend that you update
as soon as possible to an actively supported LTS version.

Google's client libraries support legacy versions of Node.js runtimes on a
best-efforts basis with the following warnings:

* Legacy versions are not tested in continuous integration.
* Some security patches and features cannot be backported.
* Dependencies cannot be kept up-to-date.

Client libraries targeting some end-of-life versions of Node.js are available, and
can be installed through npm [dist-tags](https://docs.npmjs.com/cli/dist-tag).
The dist-tags follow the naming convention `legacy-(version)`.
For example, `npm install @google-cloud/rcloadenv@legacy-8` installs client libraries
for versions compatible with Node.js 8.

## Versioning

This library follows [Semantic Versioning](http://semver.org/).







This library is considered to be in **preview**. This means it is still a
work-in-progress and under active development. Any release is subject to
backwards-incompatible changes at any time.


More Information: [Google Cloud Platform Launch Stages][launch_stages]

[launch_stages]: https://cloud.google.com/terms/launch-stages

## Contributing

Contributions welcome! See the [Contributing Guide](https://github.com/googleapis/nodejs-rcloadenv/blob/main/CONTRIBUTING.md).

Please note that this `README.md`, the `samples/README.md`,
and a variety of configuration files in this repository (including `.nycrc` and `tsconfig.json`)
are generated from a central template. To edit one of these files, make an edit
to its templates in
[directory](https://github.com/googleapis/synthtool).

## License

Apache Version 2.0

See [LICENSE](https://github.com/googleapis/nodejs-rcloadenv/blob/main/LICENSE)

[client-docs]: https://github.com/googleapis/nodejs-rcloadenv/blob/main/README.md
[product-docs]: https://cloud.google.com/deployment-manager/runtime-configurator/
[shell_img]: https://gstatic.com/cloudssh/images/open-btn.png
[projects]: https://console.cloud.google.com/project
[billing]: https://support.google.com/cloud/answer/6293499#enable-billing

[auth]: https://cloud.google.com/docs/authentication/getting-started

# Center of Excellence (CoE) command line interface (CLI) upgrade

Upgrade will depend on how you installed the CoE CLI.

## Download

If you downloaded the CoE CLI as a zip file or a Git clone from [coe-starter-kit](https://github.com/microsoft/coe-starter-kit).

- Download the new zip file.
- Unzip the zip file to a new folder.

OR

- Pull changes from Git.

   ```bash
   git pull
   ```

Once you have a local version of the coe-cli, go to the **coe-cli** folder.

   ```bash
   cd coe-cli

   ```

### Local Upgrade

In the **coe-cli** folder, run the following commands:

1. Install the dependencies.

   ```bash
   npm install

   ```

1. Build the new version.

   ```bash
   npm run build

   ```

1. Update coe-cli to the new version.

   ```bash
   npm link --force

   ```

## Docker image

In the coe-cli folder, run the following command:

1. Build a new docker image.

   ```bash
   docker build -t coe-cli

   ```

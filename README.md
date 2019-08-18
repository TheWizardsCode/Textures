# Open Source Textures for Unity 3D

This is a library of open source assets that you can use in early prototypes of your games and assets. They are all under a license that means you can use them in any environment and without restriction. This includes redistribution as individual assets. This means you can use them in demo scenes for your assets - something that is normally prohibitted. All you are required to do is provide a LICENSE and a NOTICE file in your project source.

The goal of this project is not to provide AAA quality assets but instead provide a library of assets that are "good enough" for game prototypes and demo scenes for your own published assets. Though you will be surprised at the quality of some of the models here.

# Use

  1. Import this package into your project.
  2. Open the `OpenSourceModels/Scenes/TexturesCatalog` scene
  3. Use the UI to filter the available models and select one for display (when viewing materials you can view the matieral in more detail by flipping to an inspector view with the 'F' key)
  4. When you find a model you like it will have been pinged in the Project view - go ahead and use it in your project as you would use any other model - but without license restrictions (see `NOTICE File` below)
  
## Installing Via Package Manager

Modify your manifest.json file found at /PROJECTNAME/Packages/manifest.json by including the following line

```json
{
	"dependencies": {
		...
		"org.3dtbd.textures": "https://github.com/3dtbd/Textures.git#release/stable",
		...
  }
}
```

## NOTICE file

When you use assets from this project you must copy the NOTICE and LICENSE files that can be found in the root of this project into your project. The NOTICE file must be placed in the root of your project while the LICENSE file can be placed anywhere convenient. 

If you already have NOTICE file simply append the contents of our NOTICE to yours.

In order to avoid confusion over which assets are covered by our LICENSE we recommend keeping all the assets you use in a directory called `3dtbd/OpenSource` or similar. You can then place the LICENSE file in this folder.

## User with Gaia

In the `OpenSourceModels/ProceduralWorlds` folder you will find various resource files that make it easier to work with these models inside the [Procedural Worlds](https://assetstore.unity.com/publishers/15277) suite of products. For example, you can find [Gaia](https://assetstore.unity.com/packages/tools/terrain/gaia-terrain-scene-generator-42618) resource packs and [GeNa](https://assetstore.unity.com/packages/tools/terrain/gena-2-terrain-scene-spawner-127636) spawners.

It is outside the scope of this document to provide tutorials for the use of these assets in those tools, we recommend you review the excellent online tutorials for these assets.

# Contribution

We welcome contributions of new models and integrations of these models into other assets.

FIXME: Contribution guide
FIXME: Reference to Discord

# Releasing

We use [Jeff Campbell's Unity Package Tools](https://github.com/jeffcampbellmakesgames/unity-package-tools) to help with building releases. Install these tools from the release package on GitHub (we don't install via package manager as we don't want them to be installed as a dependency of our projects).

[Full usage instructions](https://github.com/jeffcampbellmakesgames/unity-package-tools/blob/master/usage.md) are available, the below is a summary for convenience.

  1. Update the Package Version Number
  2. Review all other settings
  3. Click Export Package
  4. In bash, in the export directory run the following commands:
  
  ```bash
  git init
  git remote add origin git@github.com:3dtbd/Textures.git
  git checkout --orphan release/stable
  git add .
  git commit -m "Release vx.y.z"
  git push origin release/stable
  ```

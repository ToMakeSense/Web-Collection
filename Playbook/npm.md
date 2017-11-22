## NPM Basic
	--Typical NMP usage
	npm install
	npm start
	npm test XXscript.js

	--NPM help
	npm -h
	npm help install
	npm apihelp install
	npm install -h
	npm help-search *

	npm shortcuts(see document online)

	--Creating a Package.json
	npm init
	// quick create with default setting
	npm init -y

	--Setting in Package.json
	npm set XXX
	npm get XXX
	npm config delete XXX

	--install, list, uninstall, remove and update
	npm install XXX
	npm install XXX@version
	npm install XXX --save(-s)
	// devDependencies
	npm install XXX --save-dev(-D)

	npm list
	npm list --depth 0
	npm list --global true
	npm list --depth 0 --global true
	npm list --depth 0 --long true
	npm list --depth 0 --json true
	npm list --depth 0 --parseable true
	npm list --depth 0 --dev true
	npm list --depth 0 --prod true

	npm install underscore -global

	npm uninstall underscore
	npm uninstall underscore --save


	// ^(latest version of major release)
	// ~(latest version of minor release)
	npm install underscore@1.8.X
	npm install underscore@1.8

	npm install underscore@">=1.1.0 <1.4.0"

	// will not auto upgrade
	npm install underscore@1.8.2 --save --save-exact

	npm update
	npm update --dev
	npm update --prod
	npm update underscore
	npm update underscore@1.8.3
	npm update -g

## Advanced NPM
	npm install URL
	npm install URL --save

	npm install gist:hashcode
	npm install gist:hashcode --save

	npm install path
	npm install path --save

	// npm offical site:www.npmjs.com
	// npm registry:registry.npm.org/packageName
	// go to package page:npm/im/packageName

	npm search(very slow)

	npm prune
	npm prune --production

	npm repo underscore

	npm install npm@latest -g(Administrator privileges)

	"scripts" in package.json(document in npm)
		"test": "node  test.js"
		"start": "node index.js" 	
		"uglify":"gulp compress" --->excute it in CLI:npm run uglify

## Publishing your own package
	1. setuping an NPM account
		CLI: npm adduser

	2. preparing your project for publishing
		upload source code onto your github
		input infomation for your own package --> CLI:npm init

	3. publishing your packge
		npm publish, npm info XXX, npm repo XXX, 
	   	git tag 1.0.1 
	   	git push --tags

	4. publishing an update
		git add .
		git commit -m "commit message"
		npm version major(minor,patch)
		git status
		git log
		git tag(npm will commit once automatically, V1.X.X)

	5. release a Beta vesion
		git publish --tag beta

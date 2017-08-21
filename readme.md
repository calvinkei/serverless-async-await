# Serverless Async Await
Frictionless async await transpiler for Node 0.12 using async-to-gen

Transpile your entire project using async await. 

## Instalation

`npm install --save-dev serverless-async-await`

## Usage

`serverless package`

Or

`serverless deploy`

Both will transpile your code to the temporary folder and then get copied to the __.serverless__ folder.

## Consideration

When running 

`sls invoke local` 

the code is not transpiled , instead it uses your native node version.

The plugins will first transpile your code to a temporary `__build__` folder, before copying everything to the `.serverless` folder.

## Advantage over Typescript and Webpack / Babel

Unlike typescript plugin and webpack serverless async await will not compiled your code it will only get translated. You can see the test/handlers folder to get an idea of what your code will look like.

Hence Webpack and Typescript makes debugging hell. 

If you had a bad experience with those tools, this plugins will save you tons of time and energy with a frictionless transpiling !

The transpiling is ultra lightweight , only 25 characters are added to your code.

## Troubleshooting

Make sure a `__build__` folder does not exist when packaging or deploying.
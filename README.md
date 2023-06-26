#   Creating a Token & Deploying

In this project , we have initialised a hardhat js project and in Contracts , we have written our own smart contract which creates a token.

## Description 

The smart contract creates a token called a Sponge and also mints, transfer, burn, approves and check the balance of the tokens. Then , we are deploying it on the hardhat network in the deploy.js file

### Executing program
To run this program, you can download the project by downloading the zip file under code. OR

You can try running the following commands 

```shell
npm install
npm install @openzeppelin/contracts@4.9.0 -g
```

```shell
npm install @nomicfoundation/hardhat-toolbox -g
```

```shell
npx hardhat init
```

```shell
npx hardhat compile
```


```shell
npx hardhat run scripts/deploy.js
```

## Authors

Sruthika Sivakumar

@sruthikaaas@gmail.com

## License

This project is licensed under the MIT License - see the LICENSE.md file for details

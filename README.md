![](https://github.com/wniemiec-util-java/parser-balance/blob/master/docs/img/logo/logo.jpg)

<h1 align='center'>Parser Balance</h1>
<p align='center'>Performs the count of how many times a given open symbol has in a text subtracted from how many closed symbols that text has.</p>
<p align="center">
	<a href="https://github.com/wniemiec-util-java/parser-balance/actions/workflows/windows.yml"><img src="https://github.com/wniemiec-util-java/parser-balance/actions/workflows/windows.yml/badge.svg" alt=""></a>
	<a href="https://github.com/wniemiec-util-java/parser-balance/actions/workflows/macos.yml"><img src="https://github.com/wniemiec-util-java/parser-balance/actions/workflows/macos.yml/badge.svg" alt=""></a>
	<a href="https://github.com/wniemiec-util-java/parser-balance/actions/workflows/ubuntu.yml"><img src="https://github.com/wniemiec-util-java/parser-balance/actions/workflows/ubuntu.yml/badge.svg" alt=""></a>
	<a href="https://codecov.io/gh/wniemiec-util-java/parser-balance"><img src="https://codecov.io/gh/wniemiec-util-java/parser-balance/branch/master/graph/badge.svg?token=R2SFS4SP86" alt="Coverage status"></a>
	<a href="http://java.oracle.com"><img src="https://img.shields.io/badge/java-11+-D0008F.svg" alt="Java compatibility"></a>
	<a href="https://mvnrepository.com/artifact/io.github.wniemiec-util-java/parser-balance"><img src="https://img.shields.io/maven-central/v/io.github.wniemiec-util-java/parser-balance" alt="Maven Central release"></a>
	<a href="https://github.com/wniemiec-util-java/parser-balance/blob/master/LICENSE"><img src="https://img.shields.io/github/license/wniemiec-util-java/parser-balance" alt="License"></a>
</p>
<hr />

## ❇ Introduction
Parser Balance is a symbol counter, counting how many times a given open symbol has in a text subtracted from how many closed symbols that text has.

## ❓ How to use
1. Add one of the options below to the pom.xml file: 

#### Using Maven Central (recomended):
```
<dependency>
  <groupId>io.github.wniemiec-util-java</groupId>
  <artifactId>parser-balance</artifactId>
  <version>LATEST</version>
</dependency>
```

#### Using GitHub Packages:
```
<dependency>
  <groupId>wniemiec.io.java</groupId>
  <artifactId>parser-balance</artifactId>
  <version>LATEST</version>
</dependency>
```

2. Run
```
$ mvn install
```

3. Use it
```
[...]

import wniemiec.io.java.Balance;

[...]

Balance cbBalance = new CurlyBracketBalance();
Balance rbBalance = new RoundBracketBalance();

String example = "{Hello (World{";

cbBalance.parse(example);
rbBalance.parse(example);

System.out.println( cbBalance.getBalance() );
System.out.println( rbBalance.getBalance() );

[...]
```


## 📖 Documentation
|        Property        |Parameter type|Return type|Description|Default parameter value|
|----------------|-------------------------------|-----|------------------------|--------|
|parse |`void`|`void`|Analyzes a text and updates the balance | - |
|increaseBalance |`void`|`void`|Increases the balance| - |
|decreaseBalance |`void`|`boolean`|Decreases the balance| - |
|getBalance |`void`|`boolean`|Gets balance value| - |
|isBalanceEmpty | `void`|`void`|Checks whether the balance is empty| - |
|alreadyIncreased | `void`|`boolean`|Checks whether the balance has already been increased at any time| - |

## 🚩 Changelog
Details about each version are documented in the [releases section](https://github.com/williamniemiec/wniemiec-util-java/parser-balance/releases).

## 🤝 Contribute!
See the documentation on how you can contribute to the project [here](https://github.com/wniemiec-util-java/parser-balance/blob/master/CONTRIBUTING.md).

## 📁 Files

### /
|        Name        |Type|Description|
|----------------|-------------------------------|-----------------------------|
|dist |`Directory`|Released versions|
|docs |`Directory`|Documentation files|
|src     |`Directory`| Source files|

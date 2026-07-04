# AutoTrader Web Maven Repository (`com.dakshata:at-api`)

> Public Maven repository that hosts the **AutoTrader Web Java trading library** (`com.dakshata:at-api`). Add it to your Gradle or Maven build to place, modify, cancel and track orders across **40+ Indian brokers** from your own Java code. Part of **[AutoTrader Web](https://stocksdeveloper.in/)** by **Stocks Developer**.

[![Latest version](https://img.shields.io/badge/at--api-3.1.0-2ea44f)](https://raw.githubusercontent.com/stocks-developer/autotrader-maven-repo/main/com/dakshata/at-api/)
[![Brokers supported](https://img.shields.io/badge/brokers-40%2B-2ea44f)](https://stocksdeveloper.in/#supported-brokers)
[![Free trial](https://img.shields.io/badge/free%20trial-1%20month-blue)](https://webx.stocksdeveloper.in/register)
[![API docs](https://img.shields.io/badge/docs-API%20reference-8a2be2)](https://stocksdeveloper.in/documentation/api/)

---

## What is this repository?

This is the public Maven repository for the **AutoTrader Web Java library** (`com.dakshata:at-api`). It is served straight from raw GitHub files, so you can resolve the dependency in any Gradle or Maven project without extra setup.

The `at-api` library is a **broker-independent trading client** for the JVM: you write your strategy once and run it against any broker AutoTrader Web supports, across 40+ Indian brokers, with no broker-specific code.

## Add it to your project

**Gradle** (`build.gradle`):

```groovy
repositories {
    mavenCentral()
    maven { url "https://raw.githubusercontent.com/stocks-developer/autotrader-maven-repo/main" }
}

dependencies {
    implementation 'com.dakshata:at-api:3.1.0'
}
```

**Maven** (`pom.xml`):

```xml
<repositories>
    <repository>
        <id>stocks-developer</id>
        <url>https://raw.githubusercontent.com/stocks-developer/autotrader-maven-repo/main</url>
    </repository>
</repositories>

<dependency>
    <groupId>com.dakshata</groupId>
    <artifactId>at-api</artifactId>
    <version>3.1.0</version>
</dependency>
```

Then create one instance with your API key and place an order (the same call works on every supported broker):

```java
IAutoTrader autotrader = AutoTrader.createInstance("<your-api-key>");

IOperationResponse<String> response = autotrader.placeRegularOrder(
    "ACC_NAME", "<exchange>", "SBIN",
    TradeType.BUY, OrderType.MARKET, ProductType.INTRADAY,
    1, 0f, 0f);
```

Full step-by-step guide: **[Java library setup](https://stocksdeveloper.in/documentation/client-setup/java-library/)**. Every function is documented in the [API reference](https://stocksdeveloper.in/documentation/api/). Get your API key from your [account settings](https://webx.stocksdeveloper.in/register).

## What is AutoTrader Web?

**[AutoTrader Web](https://stocksdeveloper.in/)** by **Stocks Developer** is copy trading and multi-account software for Indian brokers. Monitor every broker account on one screen (live P&L, holdings, positions, orders and margins), place bulk orders across many accounts, copy trades two ways (PMS and master-child), automate your TradingView alerts, and build your own broker-independent system on our APIs.

- **8+ years in operation. 99.98% uptime. 40+ brokers. Under 100 ms data latency.**
- 🆓 **Free static IP included** with every account, saving up to ₹500 per broker account per month.
- 💸 **₹295 to ₹495 per account per month**, all taxes and static IP included. **Free 1-month trial** on supported brokers.
- 🔒 API credentials encrypted and stored in India, broker OAuth login and two-factor authentication, portfolio data never stored, plus a Kill Switch.

## Supported brokers

AutoTrader Web works with **40+ Indian brokers**:

5paisa · AC Agarwal · Aetram Trades · Alice Blue · Ambalal Shares · Anand Rathi · Angel One · Arham Share · ATS · AxisDirect · Choice · DBOnline · Dhan · Eureka Share · Finvasia · Flattrade · FYERS · Groww · IIFL Securities · Jainam (Prop & Retail) · Kotak Securities · Mastertrust · Mirae Asset Sharekhan · MLB Stock Broking · Motilal Oswal · Nuvama · PL Capital (PLIndia) · Profitmart · Pune E-Stock Broking (PESB) · Raghunandan Money · Religare · Share India (Prop & Retail) · SMC India · Stocko · SW Capital · Tradejini · Tradeswift · Upstox · Wisdom Capital · Zebu · Zerodha

*Plus any broker that supports the Symphony XTS API.* See the [full, always-current broker list](https://stocksdeveloper.in/#supported-brokers).

## Documentation and links

| Resource | Link |
|---|---|
| 🌐 Website | https://stocksdeveloper.in/ |
| ✨ Features | https://stocksdeveloper.in/features/ |
| 💰 Pricing | https://stocksdeveloper.in/pricing/ |
| 🏦 Supported brokers | https://stocksdeveloper.in/#supported-brokers |
| 📘 Documentation | https://stocksdeveloper.in/documentation/getting-started/ |
| 🧩 API reference | https://stocksdeveloper.in/documentation/api/ |
| ☕ Java library (source) | https://github.com/stocks-developer/autotrader-java-lib |
| ⚙️ Java library setup | https://stocksdeveloper.in/documentation/client-setup/java-library/ |
| 🆓 Start free (1-month trial) | https://webx.stocksdeveloper.in/register |
| ✉️ Contact us | https://stocksdeveloper.in/contact/ |

## About Stocks Developer

Stocks Developer is a technology company building software tools for Indian markets, shaped by 8+ years of trader feedback.

Stocks Developer provides software tools only. It gives no investment advice, tips, recommendations, or trading strategies, and it makes no trading decisions for you. All trading and investment decisions remain solely your responsibility. You set up and control every activity, and you can stop it at any time.

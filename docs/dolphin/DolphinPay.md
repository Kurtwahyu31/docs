# 🐬 DolphinPay

DolphinPay enables BYOT (Bring your own token) private payment for Polkadot ecosystem assets. Below is the overview of DolphinPay:

![overview](./private-payment/DolphinPay.svg)

## Try Dolphin (version Boto)

1. Download *Signer*, an native app to turbo-charge zero-knowledge proof generation.
   * [macOS](https://github.com/Manta-Network/manta-signer/releases/download/0.4.1/Manta.Signer_0.4.1_x64-macOS.dmg)
   * Ubuntu/Debian: in testing phase, to be released
   * Windows: in testing phase, to be released

   For macOS, you might need to go to `System Preferences -> Security & Privacy -> General` to run the *Signer* (we are working to get the app approved by Apple, but it takes time).

   ![signer-security](./private-payment/allow-signer.png)

   When you first open *Signer*, it will ask you to create a password and to memorize a 12-word mnemonic.

2. Get Testnet Tokens:
   * Join [Manta&Calamari's Discord](https://t.co/5BacMMLSCW)
   * Go to the `#dolphin-faucet` channel
   * Type `/gimme` and you will see a faucet options prompt:

   ![faucet](./private-payment/faucet.png)

   * You should first claim `DOL`, since you need `DOL` to pay gas fees. Then, you can claim your favorite testnet tokens like `BTC`, `ETH`, `DOT`, etc.

3. Go to [Dolphin App](https://app.dolphin.manta.network/), try these hot baked Dolphin (version Boto) features:
   * Convert public tokens to private:

   ![to-private](./private-payment/to-private.png)

   * You can see your private token balance by switching to `private` option:

   ![private-transfer](./private-payment/private-transfer.png)

   * Send private tokens: private tokens are attached to a `One-Time Shielded Address`, which means before sending tokens to your friend, you need to get their one time shielded address through some secure communication channel, such as Signal or Telegram.

   * To receive private tokens, get your own `One-Time Shielded Address` by going to `private -> receive -> new address`:

   ![shielded-address](./private-payment/shielded-address.png)

   * Convert private tokens to public tokens:

   ![to-public](./private-payment/to-public.png)

## FAQ

1. Why do I need a *Signer*? Can I trust it?

   _*Signer* serves two purposes: first is to protect your spending secrets, and second is to use native code to build zero-knowledge proofs. The *Signer* runs locally and will never share your secrets. The *Signer* is [fully open source software](https://github.com/Manta-Network/manta-signer) and will be audited for security._

2. Is the private token in *Signer* secure?

   _All the secrets used to spend private tokens is stored locally in your computer and encrypted using [AES](https://en.wikipedia.org/wiki/Advanced_Encryption_Standard). *Signer* will never send your secrets online._

3. What is a one time shielded address? How is the shielded address different from my generic Polkadot/Manta address?

   _Dolphin (Boto) uses a one-time shielded address. This is a one-time address for your private tokens. For privacy and security, the address is longer than a typical generic Polkadot/Manta address. In the next version of the testnet, we will switch to reusable shielded addresses._

4. How can I recover private tokens if I forgot my *Signer* password?

   _We will add recover feature to the *Signer* soon._

5. How does private payment work?

   _[Find out more.](PrivatePayment.md)_
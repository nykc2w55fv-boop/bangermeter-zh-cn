# 第三方声明 / Third-party notices

## Bangermeter · MIT

Copyright (c) 2026 Ryan Lenk. The full original notice is provided in [LICENSE](LICENSE). This fork adds Simplified Chinese localization and extends the Chrome extension’s content script to `pro.x.com`. Original project and history are available at [itsryanlenk/bangermeter](https://github.com/itsryanlenk/bangermeter/tree/b7681482346e08c5e010bddd64ce8e54fdfd1b87).

The original Japanese translations are by [sysCat (@sysCat64)](https://github.com/sysCat64/bangermeter-ja/tree/f989ddc), as credited in `extension/i18n.js`.

## X recommendation algorithm · Apache License 2.0

Bangermeter's original JavaScript scoring implementation adapts the published X value-model arithmetic. Bangermeter transcribes the published weights into JavaScript and supplies its own estimated probabilities when actual counts are unavailable. The scoring arithmetic and weight values in this edition are inherited from Bangermeter.

- [Published value-model scoring code](https://github.com/xai-org/x-algorithm/blob/b220448/xai-value-model/scoring.rs)
- [Published ranking weights](https://github.com/xai-org/x-algorithm/blob/b220448/home-mixer/params/param.rs)
- [Apache 2.0 license included in this distribution](LICENSE-APACHE-2.0.txt)

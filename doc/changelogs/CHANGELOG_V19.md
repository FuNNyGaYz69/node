# Node.js 19 ChangeLog

<!--lint disable maximum-line-length no-literal-urls prohibited-strings-->

<table>
<tr>
<th>Current</th>
</tr>
<tr>
<td>
<a href="#19.1.0">19.1.0</a><br/>
<a href="#19.0.0">19.0.0</a><br/>
</td>
</tr>
</table>

* Other Versions
  * [18.x](CHANGELOG_V18.md)
  * [17.x](CHANGELOG_V17.md)
  * [16.x](CHANGELOG_V16.md)
  * [15.x](CHANGELOG_V15.md)
  * [14.x](CHANGELOG_V14.md)
  * [13.x](CHANGELOG_V13.md)
  * [12.x](CHANGELOG_V12.md)
  * [11.x](CHANGELOG_V11.md)
  * [10.x](CHANGELOG_V10.md)
  * [9.x](CHANGELOG_V9.md)
  * [8.x](CHANGELOG_V8.md)
  * [7.x](CHANGELOG_V7.md)
  * [6.x](CHANGELOG_V6.md)
  * [5.x](CHANGELOG_V5.md)
  * [4.x](CHANGELOG_V4.md)
  * [0.12.x](CHANGELOG_V012.md)
  * [0.10.x](CHANGELOG_V010.md)
  * [io.js](CHANGELOG_IOJS.md)
  * [Archive](CHANGELOG_ARCHIVE.md)

<a id="19.1.0"></a>

## 2022-11-02, Version 19.1.0 (Current), @RafaelGSS

### Notable changes

#### fs.watch recursive support on Linux

`fs.watch` supports recursive watch using the `recursive: true` option.

```js
const watcher = fs.watch(testDirectory, { recursive: true });
watcher.on('change', function(event, filename) {
});
```

Contributed by Yagiz Nizipli in [#45098](https://github.com/nodejs/node/pull/45098)

#### Other notable changes

* **deps**
  * update ICU to 72.1 (Michaël Zasso) [#45068](https://github.com/nodejs/node/pull/45068)
* **doc**
  * add lukekarrys to collaborators (Luke Karrys) [#45180](https://github.com/nodejs/node/pull/45180)
  * add anonrig to collaborators (Yagiz Nizipli) [#45002](https://github.com/nodejs/node/pull/45002)
* **util**
  * (SEMVER-MINOR) add MIME utilities (Bradley Farias) [#21128](https://github.com/nodejs/node/pull/21128)

### Commits

* \[[`1a58b7c4cd`](https://github.com/nodejs/node/commit/1a58b7c4cd)] - **benchmark**: add blob benchmark (Yagiz Nizipli) [#44990](https://github.com/nodejs/node/pull/44990)
* \[[`c083250476`](https://github.com/nodejs/node/commit/c083250476)] - **bootstrap**: merge main thread and worker thread initializations (Joyee Cheung) [#44869](https://github.com/nodejs/node/pull/44869)
* \[[`e04602d121`](https://github.com/nodejs/node/commit/e04602d121)] - **buffer**: fix validation of options in `Blob` constructor (Antoine du Hamel) [#45156](https://github.com/nodejs/node/pull/45156)
* \[[`129d7b2115`](https://github.com/nodejs/node/commit/129d7b2115)] - **build**: support Python 3.11 (Luigi Pinca) [#45191](https://github.com/nodejs/node/pull/45191)
* \[[`ca73a24ea5`](https://github.com/nodejs/node/commit/ca73a24ea5)] - **build**: workaround for node-core-utils (Jiawen Geng) [#45199](https://github.com/nodejs/node/pull/45199)
* \[[`ba59911c22`](https://github.com/nodejs/node/commit/ba59911c22)] - **build**: fix icu-small build with ICU 72.1 (Steven R. Loomis) [#45195](https://github.com/nodejs/node/pull/45195)
* \[[`cccc873448`](https://github.com/nodejs/node/commit/cccc873448)] - **build**: remove unused language files (Ben Noordhuis) [#45138](https://github.com/nodejs/node/pull/45138)
* \[[`f1eca98bb7`](https://github.com/nodejs/node/commit/f1eca98bb7)] - **build**: add GitHub token to auto-start-ci workflow (Richard Lau) [#45185](https://github.com/nodejs/node/pull/45185)
* \[[`65d04ccc75`](https://github.com/nodejs/node/commit/65d04ccc75)] - **build**: restore Windows resource file (Richard Lau) [#45042](https://github.com/nodejs/node/pull/45042)
* \[[`c5705db892`](https://github.com/nodejs/node/commit/c5705db892)] - **build**: add version info to timezone update PR (Darshan Sen) [#45021](https://github.com/nodejs/node/pull/45021)
* \[[`c2cad0cd09`](https://github.com/nodejs/node/commit/c2cad0cd09)] - **child\_process**: validate arguments for null bytes (Darshan Sen) [#44782](https://github.com/nodejs/node/pull/44782)
* \[[`cf0524909c`](https://github.com/nodejs/node/commit/cf0524909c)] - **deps**: update corepack to 0.15.0 (Node.js GitHub Bot) [#45235](https://github.com/nodejs/node/pull/45235)
* \[[`687e3621b7`](https://github.com/nodejs/node/commit/687e3621b7)] - **deps**: update undici to 5.12.0 (Node.js GitHub Bot) [#45236](https://github.com/nodejs/node/pull/45236)
* \[[`1650b3e43f`](https://github.com/nodejs/node/commit/1650b3e43f)] - _**Revert**_ "**deps**: make V8 compilable with older glibc" (Michaël Zasso) [#45162](https://github.com/nodejs/node/pull/45162)
* \[[`77badc0f33`](https://github.com/nodejs/node/commit/77badc0f33)] - **deps**: update ICU to 72.1 (Michaël Zasso) [#45068](https://github.com/nodejs/node/pull/45068)
* \[[`983bc57bf9`](https://github.com/nodejs/node/commit/983bc57bf9)] - _**Revert**_ "**deps**: V8: forward declaration of `Rtl*FunctionTable`" (Michaël Zasso) [#45119](https://github.com/nodejs/node/pull/45119)
* \[[`cd1775b251`](https://github.com/nodejs/node/commit/cd1775b251)] - **deps**: update timezone (Node.js GitHub Bot) [#44950](https://github.com/nodejs/node/pull/44950)
* \[[`ad0871ca55`](https://github.com/nodejs/node/commit/ad0871ca55)] - **deps**: patch V8 to 10.7.193.16 (Michaël Zasso) [#45023](https://github.com/nodejs/node/pull/45023)
* \[[`fae47350b6`](https://github.com/nodejs/node/commit/fae47350b6)] - **dns**: fix port validation (Antoine du Hamel) [#45135](https://github.com/nodejs/node/pull/45135)
* \[[`58ae6fbf29`](https://github.com/nodejs/node/commit/58ae6fbf29)] - **doc**: add history section to `fetch`-related globals (Antoine du Hamel) [#45198](https://github.com/nodejs/node/pull/45198)
* \[[`67764581e8`](https://github.com/nodejs/node/commit/67764581e8)] - **doc**: clarify moderation in `onboarding.md` (Benjamin Gruenbaum) [#41930](https://github.com/nodejs/node/pull/41930)
* \[[`9f546f0eb5`](https://github.com/nodejs/node/commit/9f546f0eb5)] - **doc**: change make lint to make lint-md (RafaelGSS) [#45197](https://github.com/nodejs/node/pull/45197)
* \[[`500c15b281`](https://github.com/nodejs/node/commit/500c15b281)] - **doc**: add more lts update steps to release guide (Ruy Adorno) [#45177](https://github.com/nodejs/node/pull/45177)
* \[[`7173cd80a1`](https://github.com/nodejs/node/commit/7173cd80a1)] - **doc**: add bmuenzenmeyer to triagers (Brian Muenzenmeyer) [#45155](https://github.com/nodejs/node/pull/45155)
* \[[`396c391e39`](https://github.com/nodejs/node/commit/396c391e39)] - **doc**: update process.release (Filip Skokan) [#45170](https://github.com/nodejs/node/pull/45170)
* \[[`0af373e07c`](https://github.com/nodejs/node/commit/0af373e07c)] - **doc**: add link to triage guide (Brian Muenzenmeyer) [#45154](https://github.com/nodejs/node/pull/45154)
* \[[`e922124e14`](https://github.com/nodejs/node/commit/e922124e14)] - **doc**: mark Node.js 12 as End-of-Life (Rafael Gonzaga) [#45186](https://github.com/nodejs/node/pull/45186)
* \[[`26c9a3c736`](https://github.com/nodejs/node/commit/26c9a3c736)] - **doc**: add lukekarrys to collaborators (Luke Karrys) [#45180](https://github.com/nodejs/node/pull/45180)
* \[[`423307c115`](https://github.com/nodejs/node/commit/423307c115)] - **doc**: update mark release line lts on release guide (Ruy Adorno) [#45101](https://github.com/nodejs/node/pull/45101)
* \[[`2629fc2a80`](https://github.com/nodejs/node/commit/2629fc2a80)] - **doc**: be more definite and present tense-y (Ben Noordhuis) [#45120](https://github.com/nodejs/node/pull/45120)
* \[[`1d6f34fc01`](https://github.com/nodejs/node/commit/1d6f34fc01)] - **doc**: add major version note to release guide (Ruy Adorno) [#45054](https://github.com/nodejs/node/pull/45054)
* \[[`e20f1698ff`](https://github.com/nodejs/node/commit/e20f1698ff)] - **doc**: fix v14.x link maintaining openssl guide (RafaelGSS) [#45071](https://github.com/nodejs/node/pull/45071)
* \[[`e91bcc0783`](https://github.com/nodejs/node/commit/e91bcc0783)] - **doc**: add note about latest GitHub release (Michaël Zasso) [#45111](https://github.com/nodejs/node/pull/45111)
* \[[`07a2ec2ed2`](https://github.com/nodejs/node/commit/07a2ec2ed2)] - **doc**: mention v18.x openssl maintaining guide (Rafael Gonzaga) [#45070](https://github.com/nodejs/node/pull/45070)
* \[[`41f6ec1f6f`](https://github.com/nodejs/node/commit/41f6ec1f6f)] - **doc**: fix display of "problematic" ASCII characters (John Gardner) [#44373](https://github.com/nodejs/node/pull/44373)
* \[[`72e7c5cb23`](https://github.com/nodejs/node/commit/72e7c5cb23)] - **doc**: mark Node.js v17.x as EOL (KaKa) [#45110](https://github.com/nodejs/node/pull/45110)
* \[[`f4899d3d04`](https://github.com/nodejs/node/commit/f4899d3d04)] - **doc**: update Node.js 16 End-of-Life date (Richard Lau) [#45103](https://github.com/nodejs/node/pull/45103)
* \[[`62b73d1c7d`](https://github.com/nodejs/node/commit/62b73d1c7d)] - **doc**: fix typo in parseArgs default value (Tobias Nießen) [#45083](https://github.com/nodejs/node/pull/45083)
* \[[`765cf8e173`](https://github.com/nodejs/node/commit/765cf8e173)] - **doc**: updated security stewards (Michael Dawson) [#45005](https://github.com/nodejs/node/pull/45005)
* \[[`32480c4fce`](https://github.com/nodejs/node/commit/32480c4fce)] - **doc**: fix http and http2 writeEarlyHints() parameter (Fabian Meyer) [#45000](https://github.com/nodejs/node/pull/45000)
* \[[`7efbec7663`](https://github.com/nodejs/node/commit/7efbec7663)] - **doc**: run license-builder (github-actions\[bot]) [#45034](https://github.com/nodejs/node/pull/45034)
* \[[`907ed0e4f7`](https://github.com/nodejs/node/commit/907ed0e4f7)] - **doc**: improve the workflow to test release binaries (Rafael Gonzaga) [#45004](https://github.com/nodejs/node/pull/45004)
* \[[`0c7ca2ae9d`](https://github.com/nodejs/node/commit/0c7ca2ae9d)] - **doc**: fix undici version in changelog (Michael Dawson) [#44982](https://github.com/nodejs/node/pull/44982)
* \[[`cd96961c05`](https://github.com/nodejs/node/commit/cd96961c05)] - **doc**: add info on fixup to security release process (Michael Dawson) [#44807](https://github.com/nodejs/node/pull/44807)
* \[[`3a6123ed48`](https://github.com/nodejs/node/commit/3a6123ed48)] - **doc**: add anonrig to collaborators (Yagiz Nizipli) [#45002](https://github.com/nodejs/node/pull/45002)
* \[[`3f0bfca3c2`](https://github.com/nodejs/node/commit/3f0bfca3c2)] - **doc, http**: add Uint8Array as allowed type (Gerhard Stöbich) [#45167](https://github.com/nodejs/node/pull/45167)
* \[[`f48b51a771`](https://github.com/nodejs/node/commit/f48b51a771)] - **esm**: protect ESM loader from prototype pollution (Antoine du Hamel) [#45175](https://github.com/nodejs/node/pull/45175)
* \[[`4f7f228787`](https://github.com/nodejs/node/commit/4f7f228787)] - **esm**: protect ESM loader from prototype pollution (Antoine du Hamel) [#45044](https://github.com/nodejs/node/pull/45044)
* \[[`e858b3c6b4`](https://github.com/nodejs/node/commit/e858b3c6b4)] - **events**: add unique events benchmark (Yagiz Nizipli) [#44657](https://github.com/nodejs/node/pull/44657)
* \[[`e9e2b276c7`](https://github.com/nodejs/node/commit/e9e2b276c7)] - **fs**: update todo message (Yagiz Nizipli) [#45265](https://github.com/nodejs/node/pull/45265)
* \[[`d9d1dda4a4`](https://github.com/nodejs/node/commit/d9d1dda4a4)] - **fs**: fix opts.filter issue in cpSync (Tho) [#45143](https://github.com/nodejs/node/pull/45143)
* \[[`c4d674d484`](https://github.com/nodejs/node/commit/c4d674d484)] - **(SEMVER-MINOR)** **fs**: add recursive watch to linux (Yagiz Nizipli) [#45098](https://github.com/nodejs/node/pull/45098)
* \[[`bd6862117c`](https://github.com/nodejs/node/commit/bd6862117c)] - **fs**: trace more fs api (theanarkh) [#45095](https://github.com/nodejs/node/pull/45095)
* \[[`95377a3599`](https://github.com/nodejs/node/commit/95377a3599)] - **http**: headers(Distinct), trailers(Distinct) setters to be no-op (Madhuri) [#45176](https://github.com/nodejs/node/pull/45176)
* \[[`e52a049274`](https://github.com/nodejs/node/commit/e52a049274)] - **http**: add priority to common http headers (James M Snell) [#45045](https://github.com/nodejs/node/pull/45045)
* \[[`67eaf0fed8`](https://github.com/nodejs/node/commit/67eaf0fed8)] - **http2**: improve session close/destroy procedures (Santiago Gimeno) [#45115](https://github.com/nodejs/node/pull/45115)
* \[[`2e528fab44`](https://github.com/nodejs/node/commit/2e528fab44)] - **http2**: fix crash on Http2Stream::diagnostic\_name() (Santiago Gimeno) [#45123](https://github.com/nodejs/node/pull/45123)
* \[[`fb55f01594`](https://github.com/nodejs/node/commit/fb55f01594)] - **http2**: fix debugStream method (Santiago Gimeno) [#45129](https://github.com/nodejs/node/pull/45129)
* \[[`6f6a8ce21b`](https://github.com/nodejs/node/commit/6f6a8ce21b)] - **inspector**: refactor `inspector/promises` to be more robust (Antoine du Hamel) [#45041](https://github.com/nodejs/node/pull/45041)
* \[[`5d5c67381e`](https://github.com/nodejs/node/commit/5d5c67381e)] - **lib**: fix `AbortSignal.timeout` parameter validation (dnalborczyk) [#42856](https://github.com/nodejs/node/pull/42856)
* \[[`a1075a120a`](https://github.com/nodejs/node/commit/a1075a120a)] - **lib**: add lint rule to protect against `Object.prototype.then` pollution (Antoine du Hamel) [#45061](https://github.com/nodejs/node/pull/45061)
* \[[`0c6c2a7b98`](https://github.com/nodejs/node/commit/0c6c2a7b98)] - **lib**: add ability to add separate event name to defineEventHandler (James M Snell) [#45032](https://github.com/nodejs/node/pull/45032)
* \[[`893aaf3746`](https://github.com/nodejs/node/commit/893aaf3746)] - **lib**: fix typo in `pre_execution.js` (Antoine du Hamel) [#45039](https://github.com/nodejs/node/pull/45039)
* \[[`28b6fd5480`](https://github.com/nodejs/node/commit/28b6fd5480)] - **lib**: promise version of streams.finished call clean up (Naor Tedgi (Abu Emma)) [#44862](https://github.com/nodejs/node/pull/44862)
* \[[`0ea61a851f`](https://github.com/nodejs/node/commit/0ea61a851f)] - **lib**: make properties on Blob and URL enumerable (Khafra) [#44918](https://github.com/nodejs/node/pull/44918)
* \[[`126d300480`](https://github.com/nodejs/node/commit/126d300480)] - **lib**: support more attributes for early hint link (Yagiz Nizipli) [#44874](https://github.com/nodejs/node/pull/44874)
* \[[`de9dc2b541`](https://github.com/nodejs/node/commit/de9dc2b541)] - **meta**: update collaborator email address in README (Rich Trott) [#45251](https://github.com/nodejs/node/pull/45251)
* \[[`13aed59ae7`](https://github.com/nodejs/node/commit/13aed59ae7)] - **meta**: fix email address typo in README (Rich Trott) [#45250](https://github.com/nodejs/node/pull/45250)
* \[[`1af5dced9b`](https://github.com/nodejs/node/commit/1af5dced9b)] - **meta**: remove dont-land-on-v12 auto labeling (Moshe Atlow) [#45233](https://github.com/nodejs/node/pull/45233)
* \[[`65f3c61c1a`](https://github.com/nodejs/node/commit/65f3c61c1a)] - **meta**: update AUTHORS (Node.js GitHub Bot) [#45238](https://github.com/nodejs/node/pull/45238)
* \[[`cd49e493d7`](https://github.com/nodejs/node/commit/cd49e493d7)] - **meta**: move a collaborator to emeritus (Rich Trott) [#45160](https://github.com/nodejs/node/pull/45160)
* \[[`33168b287f`](https://github.com/nodejs/node/commit/33168b287f)] - **meta**: move one or more collaborators to emeritus (Node.js GitHub Bot) [#45036](https://github.com/nodejs/node/pull/45036)
* \[[`c542af5a24`](https://github.com/nodejs/node/commit/c542af5a24)] - **meta**: update AUTHORS (Node.js GitHub Bot) [#45020](https://github.com/nodejs/node/pull/45020)
* \[[`ddefc5dad8`](https://github.com/nodejs/node/commit/ddefc5dad8)] - **module**: ensure relative requires work from deleted directories (Bradley Farias) [#42384](https://github.com/nodejs/node/pull/42384)
* \[[`6c20fa5694`](https://github.com/nodejs/node/commit/6c20fa5694)] - **net**: remove \_readableState from debug statement (Rich Trott) [#45063](https://github.com/nodejs/node/pull/45063)
* \[[`21ea55c9bc`](https://github.com/nodejs/node/commit/21ea55c9bc)] - **node-api,test**: fix test\_reference\_double\_free crash (Vladimir Morozov) [#44927](https://github.com/nodejs/node/pull/44927)
* \[[`8a5f6d373c`](https://github.com/nodejs/node/commit/8a5f6d373c)] - **perf\_hooks**: align toStringTag with other Web Performance implementations (Daeyeon Jeong) [#45157](https://github.com/nodejs/node/pull/45157)
* \[[`a91b921189`](https://github.com/nodejs/node/commit/a91b921189)] - **report**: add rss and use/kernel cpu usage fields (theanarkh) [#45043](https://github.com/nodejs/node/pull/45043)
* \[[`d03619de3b`](https://github.com/nodejs/node/commit/d03619de3b)] - **report,doc**: define report version semantics (Gireesh Punathil) [#45050](https://github.com/nodejs/node/pull/45050)
* \[[`7ccabbf444`](https://github.com/nodejs/node/commit/7ccabbf444)] - **src**: trace threadpool event (theanarkh) [#44458](https://github.com/nodejs/node/pull/44458)
* \[[`db81931aca`](https://github.com/nodejs/node/commit/db81931aca)] - **src**: lock-free init\_process\_flags (Jérémy Lal) [#45221](https://github.com/nodejs/node/pull/45221)
* \[[`4a31d2ae5b`](https://github.com/nodejs/node/commit/4a31d2ae5b)] - **src**: call uv\_library\_shutdown before DisposePlatform (theanarkh) [#45226](https://github.com/nodejs/node/pull/45226)
* \[[`ffc95bc985`](https://github.com/nodejs/node/commit/ffc95bc985)] - **src**: fix `crypto.privateEncrypt` fails first time (liuxingbaoyu) [#42793](https://github.com/nodejs/node/pull/42793)
* \[[`3657f6a12a`](https://github.com/nodejs/node/commit/3657f6a12a)] - **src**: clarify OptionEnvvarSettings member names (Chengzhong Wu) [#45057](https://github.com/nodejs/node/pull/45057)
* \[[`db3d7cb6e7`](https://github.com/nodejs/node/commit/db3d7cb6e7)] - **src**: let http2 streams end after session close (Santiago Gimeno) [#45153](https://github.com/nodejs/node/pull/45153)
* \[[`49e80015d3`](https://github.com/nodejs/node/commit/49e80015d3)] - **src**: remap invalid file descriptors using `dup2` (Obiwac) [#44461](https://github.com/nodejs/node/pull/44461)
* \[[`27228b0a5f`](https://github.com/nodejs/node/commit/27228b0a5f)] - **src**: remove unused `contextify_global_private_symbol` (Daeyeon Jeong) [#45128](https://github.com/nodejs/node/pull/45128)
* \[[`c366b70a87`](https://github.com/nodejs/node/commit/c366b70a87)] - **src**: forbid running watch mode in REPL (Moshe Atlow) [#45058](https://github.com/nodejs/node/pull/45058)
* \[[`9186f509f4`](https://github.com/nodejs/node/commit/9186f509f4)] - **src**: fix test runner coverage (Moshe Atlow) [#45055](https://github.com/nodejs/node/pull/45055)
* \[[`aeaf653952`](https://github.com/nodejs/node/commit/aeaf653952)] - **src**: optimize ALPN callback (Ben Noordhuis) [#44875](https://github.com/nodejs/node/pull/44875)
* \[[`8896195728`](https://github.com/nodejs/node/commit/8896195728)] - **src**: simplify ALPN code, remove indirection (Ben Noordhuis) [#44875](https://github.com/nodejs/node/pull/44875)
* \[[`3954b7a56c`](https://github.com/nodejs/node/commit/3954b7a56c)] - **src**: iwyu in cleanup\_queue.cc (Shelley Vohr) [#44983](https://github.com/nodejs/node/pull/44983)
* \[[`1f2ffe8af3`](https://github.com/nodejs/node/commit/1f2ffe8af3)] - **src**: return void in InitializeInspector() (Joyee Cheung) [#44903](https://github.com/nodejs/node/pull/44903)
* \[[`30ca63be8d`](https://github.com/nodejs/node/commit/30ca63be8d)] - **src,lib**: retrieve parsed source map url from v8 (Chengzhong Wu) [#44798](https://github.com/nodejs/node/pull/44798)
* \[[`dfd75c1fbb`](https://github.com/nodejs/node/commit/dfd75c1fbb)] - **stream**: add compose operator (Raz Luvaton) [#44937](https://github.com/nodejs/node/pull/44937)
* \[[`874ea99b14`](https://github.com/nodejs/node/commit/874ea99b14)] - **stream**: fix duplexify premature destroy (Robert Nagy) [#45133](https://github.com/nodejs/node/pull/45133)
* \[[`747082761d`](https://github.com/nodejs/node/commit/747082761d)] - **stream**: fix web streams have no Symbol.toStringTag (Jithil P Ponnan) [#45117](https://github.com/nodejs/node/pull/45117)
* \[[`83e429128c`](https://github.com/nodejs/node/commit/83e429128c)] - **stream**: don't push null from closed promise #42694 (David Halls) [#45026](https://github.com/nodejs/node/pull/45026)
* \[[`7223c9399a`](https://github.com/nodejs/node/commit/7223c9399a)] - **test**: convert test-debugger-pid to async/await (Luke Karrys) [#45179](https://github.com/nodejs/node/pull/45179)
* \[[`60888299ba`](https://github.com/nodejs/node/commit/60888299ba)] - **test**: fix textdecoder test for small-icu builds (Richard Lau) [#45225](https://github.com/nodejs/node/pull/45225)
* \[[`c73d22839b`](https://github.com/nodejs/node/commit/c73d22839b)] - **test**: improve test coverage in `test-event-capture-rejections.js` (Juan José) [#45148](https://github.com/nodejs/node/pull/45148)
* \[[`20b0c1a639`](https://github.com/nodejs/node/commit/20b0c1a639)] - **test**: fix timeout of test-heap-prof.js in riscv devices (Yu Gu) [#42674](https://github.com/nodejs/node/pull/42674)
* \[[`34ae5380cc`](https://github.com/nodejs/node/commit/34ae5380cc)] - **test**: deflake test-http2-empty-frame-without-eof (Santiago Gimeno) [#45212](https://github.com/nodejs/node/pull/45212)
* \[[`10558c9893`](https://github.com/nodejs/node/commit/10558c9893)] - **test**: use common/tmpdir in watch-mode ipc test (Richard Lau) [#45211](https://github.com/nodejs/node/pull/45211)
* \[[`440b85fe2d`](https://github.com/nodejs/node/commit/440b85fe2d)] - **test**: use uv\_sleep() where possible (Santiago Gimeno) [#45124](https://github.com/nodejs/node/pull/45124)
* \[[`5d8f5b9a20`](https://github.com/nodejs/node/commit/5d8f5b9a20)] - **test**: fix typo in `test/parallel/test-fs-rm.js` (Tim Shilov) [#44882](https://github.com/nodejs/node/pull/44882)
* \[[`5be7aeebe2`](https://github.com/nodejs/node/commit/5be7aeebe2)] - **test**: remove a snapshot blob from test-inspect-address-in-use.js (Daeyeon Jeong) [#45132](https://github.com/nodejs/node/pull/45132)
* \[[`f3c08d5686`](https://github.com/nodejs/node/commit/f3c08d5686)] - **test**: add test for Module.\_stat (Darshan Sen) [#44713](https://github.com/nodejs/node/pull/44713)
* \[[`9a146ba787`](https://github.com/nodejs/node/commit/9a146ba787)] - **test**: watch mode inspect restart repeatedly (Moshe Atlow) [#45060](https://github.com/nodejs/node/pull/45060)
* \[[`2f9039d04e`](https://github.com/nodejs/node/commit/2f9039d04e)] - **test**: remove experimental-wasm-threads flag (Michaël Zasso) [#45074](https://github.com/nodejs/node/pull/45074)
* \[[`ec28e9b98d`](https://github.com/nodejs/node/commit/ec28e9b98d)] - **test**: remove unnecessary noop function args to `mustCall()` (Antoine du Hamel) [#45047](https://github.com/nodejs/node/pull/45047)
* \[[`ddf7001cd4`](https://github.com/nodejs/node/commit/ddf7001cd4)] - **test**: mark test-watch-mode\* as flaky on all platforms (Pierrick Bouvier) [#45049](https://github.com/nodejs/node/pull/45049)
* \[[`e24af82d81`](https://github.com/nodejs/node/commit/e24af82d81)] - **test**: wrap missing `common.mustCall` (Moshe Atlow) [#45064](https://github.com/nodejs/node/pull/45064)
* \[[`6892bd7603`](https://github.com/nodejs/node/commit/6892bd7603)] - **test**: remove mentions of `--experimental-async-stack-tagging-api` flag (Simon) [#45051](https://github.com/nodejs/node/pull/45051)
* \[[`7858e7093c`](https://github.com/nodejs/node/commit/7858e7093c)] - **test**: improve assertions in `test-repl-unsupported-option.js` (Juan José) [#44953](https://github.com/nodejs/node/pull/44953)
* \[[`a6a3439ac8`](https://github.com/nodejs/node/commit/a6a3439ac8)] - **test**: remove unnecessary noop function args to mustCall() (Rich Trott) [#45027](https://github.com/nodejs/node/pull/45027)
* \[[`cda3220bd4`](https://github.com/nodejs/node/commit/cda3220bd4)] - **test**: update WPT resources (Khaidi Chu) [#44948](https://github.com/nodejs/node/pull/44948)
* \[[`bc939c311e`](https://github.com/nodejs/node/commit/bc939c311e)] - **test**: skip test depending on `overlapped-checker` when not available (Antoine du Hamel) [#45015](https://github.com/nodejs/node/pull/45015)
* \[[`a6c3074b68`](https://github.com/nodejs/node/commit/a6c3074b68)] - **test**: improve test coverage for `os` package (Juan José) [#44959](https://github.com/nodejs/node/pull/44959)
* \[[`1e67dda623`](https://github.com/nodejs/node/commit/1e67dda623)] - **test**: add test to improve coverage in http2-compat-serverresponse (Cesar Mario Diaz) [#44970](https://github.com/nodejs/node/pull/44970)
* \[[`02a6a14e42`](https://github.com/nodejs/node/commit/02a6a14e42)] - **test**: improve test coverage in `test-child-process-spawn-argv0.js` (Juan José) [#44955](https://github.com/nodejs/node/pull/44955)
* \[[`5f4fdb378c`](https://github.com/nodejs/node/commit/5f4fdb378c)] - **test**: use CHECK instead of EXPECT where necessary (Tobias Nießen) [#44795](https://github.com/nodejs/node/pull/44795)
* \[[`61a41b31b1`](https://github.com/nodejs/node/commit/61a41b31b1)] - **test**: refactor promises to async/await (Madhuri) [#44980](https://github.com/nodejs/node/pull/44980)
* \[[`a4cb0f7f78`](https://github.com/nodejs/node/commit/a4cb0f7f78)] - **test,crypto**: update WebCryptoAPI WPT (Filip Skokan) [#45165](https://github.com/nodejs/node/pull/45165)
* \[[`7c544bfae3`](https://github.com/nodejs/node/commit/7c544bfae3)] - **test\_runner**: report tap subtest in order (Moshe Atlow) [#45220](https://github.com/nodejs/node/pull/45220)
* \[[`c837b26d39`](https://github.com/nodejs/node/commit/c837b26d39)] - **test\_runner**: call {before,after}Each() on suites (Colin Ihrig) [#45161](https://github.com/nodejs/node/pull/45161)
* \[[`293ffc1cea`](https://github.com/nodejs/node/commit/293ffc1cea)] - **test\_runner**: add extra fields in AssertionError YAML (Bryan English) [#44952](https://github.com/nodejs/node/pull/44952)
* \[[`3837560a24`](https://github.com/nodejs/node/commit/3837560a24)] - **tools**: refactor dynamic strings creation in shell scripts (Antoine du Hamel) [#45240](https://github.com/nodejs/node/pull/45240)
* \[[`d7dbe93b83`](https://github.com/nodejs/node/commit/d7dbe93b83)] - **tools**: update lint-md-dependencies (Node.js GitHub Bot) [#45237](https://github.com/nodejs/node/pull/45237)
* \[[`694ceadb17`](https://github.com/nodejs/node/commit/694ceadb17)] - **tools**: use Python 3.11 in GitHub Actions workflows (Luigi Pinca) [#45191](https://github.com/nodejs/node/pull/45191)
* \[[`f7d4f0aad0`](https://github.com/nodejs/node/commit/f7d4f0aad0)] - **tools**: fix `request-ci-failed` comment (Antoine du Hamel) [#45218](https://github.com/nodejs/node/pull/45218)
* \[[`d761fdee3b`](https://github.com/nodejs/node/commit/d761fdee3b)] - **tools**: keep Emeriti lists case-insensitive alphabetic (Rich Trott) [#45159](https://github.com/nodejs/node/pull/45159)
* \[[`30822c1087`](https://github.com/nodejs/node/commit/30822c1087)] - **tools**: update actions/setup-python to v4 (Yagiz Nizipli) [#45178](https://github.com/nodejs/node/pull/45178)
* \[[`f45dbc82fd`](https://github.com/nodejs/node/commit/f45dbc82fd)] - **tools**: update V8 gypfiles for RISC-V (Andreas Schwab) [#45149](https://github.com/nodejs/node/pull/45149)
* \[[`af2625887f`](https://github.com/nodejs/node/commit/af2625887f)] - **tools**: fix `create-or-update-pull-request-action` hash on GHA (Antoine du Hamel) [#45166](https://github.com/nodejs/node/pull/45166)
* \[[`5114797842`](https://github.com/nodejs/node/commit/5114797842)] - **tools**: update gr2m/create-or-update-pull-request-action (Luigi Pinca) [#45022](https://github.com/nodejs/node/pull/45022)
* \[[`7cd85b6979`](https://github.com/nodejs/node/commit/7cd85b6979)] - **tools**: do not use the set-output command in workflows (Luigi Pinca) [#45024](https://github.com/nodejs/node/pull/45024)
* \[[`dfccd595b9`](https://github.com/nodejs/node/commit/dfccd595b9)] - **tools**: update lint-md-dependencies (Node.js GitHub Bot) [#45019](https://github.com/nodejs/node/pull/45019)
* \[[`d5ada0ff87`](https://github.com/nodejs/node/commit/d5ada0ff87)] - **trace\_events**: fix getCategories (theanarkh) [#45092](https://github.com/nodejs/node/pull/45092)
* \[[`7fa62e5c31`](https://github.com/nodejs/node/commit/7fa62e5c31)] - **url**: remove \t \n \r in url.parse() similar to WHATWG (Rich Trott) [#45116](https://github.com/nodejs/node/pull/45116)
* \[[`4ecad09d49`](https://github.com/nodejs/node/commit/4ecad09d49)] - **url**: improve port validation (Rich Trott) [#45012](https://github.com/nodejs/node/pull/45012)
* \[[`e9aa6bbb49`](https://github.com/nodejs/node/commit/e9aa6bbb49)] - **url**: improve url.parse() compliance with WHATWG URL (Rich Trott) [#45011](https://github.com/nodejs/node/pull/45011)
* \[[`aedadba0ef`](https://github.com/nodejs/node/commit/aedadba0ef)] - **(SEMVER-MINOR)** **util**: add MIME utilities (#21128) (Bradley Farias) [#21128](https://github.com/nodejs/node/pull/21128)

<a id="19.0.0"></a>

## 2022-10-18, Version 19.0.0 (Current), @RafaelGSS and @ruyadorno

Node.js 19 is here! Highlights include the update of the V8 JavaScript engine to 10.7, HTTP(s)/1.1 KeepAlive enabled by default, and ESM Resolution adjusts.

Node.js 19 will replace Node.js 18 as our ‘Current’ release line when Node.js 18 enters long-term support (LTS) later this month.
As per the release schedule, Node.js 19 will be ‘Current' release for the next 6 months, until April 2023.

### Notable Changes

#### Deprecations and Removals

* \[[`7dd2f41c73`](https://github.com/nodejs/node/commit/7dd2f41c73)] - **(SEMVER-MAJOR)** **module**: runtime deprecate exports double slash maps (Guy Bedford) [#44495](https://github.com/nodejs/node/pull/44495)
* \[[`ada2d053ae`](https://github.com/nodejs/node/commit/ada2d053ae)] - **(SEMVER-MAJOR)** **process**: runtime deprecate coercion to integer in `process.exit()` (Daeyeon Jeong) [#44711](https://github.com/nodejs/node/pull/44711)

#### HTTP(S)/1.1 KeepAlive by default

Starting with this release, Node.js sets `keepAlive` to true by default. This means that any outgoing HTTP(s) connection will automatically use HTTP 1.1 Keep-Alive. The default waiting window is 5 seconds.
Enable keep-alive will deliver better throughput as connections are reused by default.

Additionally the agent is now able to parse the response `Keep-Alive` which the servers might send. This header instructs the client on how much to stay connected.
On the other side, the Node.js HTTP server will now automatically disconnect idle clients (which are using HTTP Keep-Alive to reuse the connection) when `close()` is invoked).

Node.js HTTP(S)/1.1 requests may experience a better throughput/performance by default.

Contributed by Paolo Insogna in [#43522](https://github.com/nodejs/node/pull/43522)

#### DTrace/SystemTap/ETW Support were removed

The main reason is the lack of resources from Node.js team. The complexity to keep the support up-to-date has been proved not worth it without a clear plan to support those tools. Hence, [an issue was raised](https://github.com/nodejs/node/issues/44550) in the Node.js repository to assess a better support, for `DTrace` in specific.

Contributed by Ben Noordhuis in [#43651](https://github.com/nodejs/node/pull/43651) and [#43652](https://github.com/nodejs/node/pull/43652)

#### V8 10.7

The V8 engine is updated to version 10.7, which is part of Chromium 107.
This version include a new feature to the JavaScript API: `Intl.NumberFormat`.

`Intl.NumberFormat` v3 API is a new [TC39 ECMA402 stage 3 proposal](https://github.com/tc39/proposal-intl-numberformat-v3)
extend the pre-existing `Intl.NumberFormat`.

The V8 update was a contribution by Michaël Zasso in [#44741](https://github.com/nodejs/node/pull/44741).

#### llhttp 8.1.0

llhttp has been updated to version 8.1.0.Collectively, this version brings many update to the llhttp API, introducing new callbacks and allow all callback to be pausable.

Contributed by Paolo Insogna in [#44967](https://github.com/nodejs/node/pull/44967)

#### Other Notable Changes

* \[[`46a3afb579`](https://github.com/nodejs/node/commit/46a3afb579)] - **doc**: graduate webcrypto to stable (Filip Skokan) [#44897](https://github.com/nodejs/node/pull/44897)
* \[[`f594cc85b7`](https://github.com/nodejs/node/commit/f594cc85b7)] - **esm**: remove specifier resolution flag (Geoffrey Booth) [#44859](https://github.com/nodejs/node/pull/44859)

### Semver-Major Commits

* \[[`53f73d1cfe`](https://github.com/nodejs/node/commit/53f73d1cfe)] - **(SEMVER-MAJOR)** **build**: enable V8's trap handler on Windows (Michaël Zasso) [#44741](https://github.com/nodejs/node/pull/44741)
* \[[`06aaf8a1c4`](https://github.com/nodejs/node/commit/06aaf8a1c4)] - **(SEMVER-MAJOR)** **build**: reset embedder string to "-node.0" (Michaël Zasso) [#44741](https://github.com/nodejs/node/pull/44741)
* \[[`aa3a572e6b`](https://github.com/nodejs/node/commit/aa3a572e6b)] - **(SEMVER-MAJOR)** **build**: remove dtrace & etw support (Ben Noordhuis) [#43652](https://github.com/nodejs/node/pull/43652)
* \[[`38f1e2793c`](https://github.com/nodejs/node/commit/38f1e2793c)] - **(SEMVER-MAJOR)** **build**: remove systemtap support (Ben Noordhuis) [#43651](https://github.com/nodejs/node/pull/43651)
* \[[`2849283c4c`](https://github.com/nodejs/node/commit/2849283c4c)] - **(SEMVER-MAJOR)** **crypto**: remove non-standard `webcrypto.Crypto.prototype.CryptoKey` (Antoine du Hamel) [#42083](https://github.com/nodejs/node/pull/42083)
* \[[`a1653ac715`](https://github.com/nodejs/node/commit/a1653ac715)] - **(SEMVER-MAJOR)** **crypto**: do not allow to call setFips from the worker thread (Sergey Petushkov) [#43624](https://github.com/nodejs/node/pull/43624)
* \[[`fd36a8dadb`](https://github.com/nodejs/node/commit/fd36a8dadb)] - **(SEMVER-MAJOR)** **deps**: update llhttp to 8.1.0 (Paolo Insogna) [#44967](https://github.com/nodejs/node/pull/44967)
* \[[`89ecdddaab`](https://github.com/nodejs/node/commit/89ecdddaab)] - **(SEMVER-MAJOR)** **deps**: bump minimum ICU version to 71 (Michaël Zasso) [#44741](https://github.com/nodejs/node/pull/44741)
* \[[`66fe446efd`](https://github.com/nodejs/node/commit/66fe446efd)] - **(SEMVER-MAJOR)** **deps**: V8: cherry-pick 0cccb6f27d78 (Michaël Zasso) [#44741](https://github.com/nodejs/node/pull/44741)
* \[[`88ed027d57`](https://github.com/nodejs/node/commit/88ed027d57)] - **(SEMVER-MAJOR)** **deps**: V8: cherry-pick 7ddb8399f9f1 (Michaël Zasso) [#44741](https://github.com/nodejs/node/pull/44741)
* \[[`26c651c34e`](https://github.com/nodejs/node/commit/26c651c34e)] - **(SEMVER-MAJOR)** **deps**: V8: cherry-pick 1b3a4f0c34a1 (Michaël Zasso) [#44741](https://github.com/nodejs/node/pull/44741)
* \[[`c8ff2dfd11`](https://github.com/nodejs/node/commit/c8ff2dfd11)] - **(SEMVER-MAJOR)** **deps**: V8: cherry-pick b161a0823165 (Michaël Zasso) [#44741](https://github.com/nodejs/node/pull/44741)
* \[[`7a8fa2d517`](https://github.com/nodejs/node/commit/7a8fa2d517)] - **(SEMVER-MAJOR)** **deps**: fix V8 build on Windows with MSVC (Michaël Zasso) [#44741](https://github.com/nodejs/node/pull/44741)
* \[[`83b0aaa800`](https://github.com/nodejs/node/commit/83b0aaa800)] - **(SEMVER-MAJOR)** **deps**: fix V8 build on SmartOS (Michaël Zasso) [#44741](https://github.com/nodejs/node/pull/44741)
* \[[`7a952e8ea5`](https://github.com/nodejs/node/commit/7a952e8ea5)] - **(SEMVER-MAJOR)** **deps**: silence irrelevant V8 warning (Michaël Zasso) [#44741](https://github.com/nodejs/node/pull/44741)
* \[[`6bd756d7c6`](https://github.com/nodejs/node/commit/6bd756d7c6)] - **(SEMVER-MAJOR)** **deps**: update V8 to 10.7.193.13 (Michaël Zasso) [#44741](https://github.com/nodejs/node/pull/44741)
* \[[`03fb789fb9`](https://github.com/nodejs/node/commit/03fb789fb9)] - **(SEMVER-MAJOR)** **events**: add null check for the signal of EventTarget (Masashi Hirano) [#43153](https://github.com/nodejs/node/pull/43153)
* \[[`a4fa526ddc`](https://github.com/nodejs/node/commit/a4fa526ddc)] - **(SEMVER-MAJOR)** **fs**: add directory autodetection to fsPromises.symlink() (Livia Medeiros) [#42894](https://github.com/nodejs/node/pull/42894)
* \[[`bb4891d8d4`](https://github.com/nodejs/node/commit/bb4891d8d4)] - **(SEMVER-MAJOR)** **fs**: add validateBuffer to improve error (Hirotaka Tagawa / wafuwafu13) [#44769](https://github.com/nodejs/node/pull/44769)
* \[[`950a4411fa`](https://github.com/nodejs/node/commit/950a4411fa)] - **(SEMVER-MAJOR)** **fs**: remove coercion to string in writing methods (Livia Medeiros) [#42796](https://github.com/nodejs/node/pull/42796)
* \[[`41a6d82968`](https://github.com/nodejs/node/commit/41a6d82968)] - **(SEMVER-MAJOR)** **fs**: harden fs.readSync(buffer, options) typecheck (LiviaMedeiros) [#42772](https://github.com/nodejs/node/pull/42772)
* \[[`2275faac2b`](https://github.com/nodejs/node/commit/2275faac2b)] - **(SEMVER-MAJOR)** **fs**: harden fs.read(params, callback) typecheck (LiviaMedeiros) [#42772](https://github.com/nodejs/node/pull/42772)
* \[[`29953a0b88`](https://github.com/nodejs/node/commit/29953a0b88)] - **(SEMVER-MAJOR)** **fs**: harden filehandle.read(params) typecheck (LiviaMedeiros) [#42772](https://github.com/nodejs/node/pull/42772)
* \[[`4267b92604`](https://github.com/nodejs/node/commit/4267b92604)] - **(SEMVER-MAJOR)** **http**: use Keep-Alive by default in global agents (Paolo Insogna) [#43522](https://github.com/nodejs/node/pull/43522)
* \[[`0324529e0f`](https://github.com/nodejs/node/commit/0324529e0f)] - **(SEMVER-MAJOR)** **inspector**: introduce inspector/promises API (Erick Wendel) [#44250](https://github.com/nodejs/node/pull/44250)
* \[[`80270994d6`](https://github.com/nodejs/node/commit/80270994d6)] - **(SEMVER-MAJOR)** **lib**: enable global CustomEvent by default (Daeyeon Jeong) [#44860](https://github.com/nodejs/node/pull/44860)
* \[[`f529f73bd7`](https://github.com/nodejs/node/commit/f529f73bd7)] - **(SEMVER-MAJOR)** **lib**: brand check event handler property receivers (Chengzhong Wu) [#44483](https://github.com/nodejs/node/pull/44483)
* \[[`6de2673a9f`](https://github.com/nodejs/node/commit/6de2673a9f)] - **(SEMVER-MAJOR)** **lib**: enable global WebCrypto by default (Antoine du Hamel) [#42083](https://github.com/nodejs/node/pull/42083)
* \[[`73ba8830d5`](https://github.com/nodejs/node/commit/73ba8830d5)] - **(SEMVER-MAJOR)** **lib**: use private field in AbortController (Joyee Cheung) [#43820](https://github.com/nodejs/node/pull/43820)
* \[[`7dd2f41c73`](https://github.com/nodejs/node/commit/7dd2f41c73)] - **(SEMVER-MAJOR)** **module**: runtime deprecate exports double slash maps (Guy Bedford) [#44495](https://github.com/nodejs/node/pull/44495)
* \[[`22c39b1ddd`](https://github.com/nodejs/node/commit/22c39b1ddd)] - **(SEMVER-MAJOR)** **path**: the dot will be added(path.format) if it is not specified in `ext` (theanarkh) [#44349](https://github.com/nodejs/node/pull/44349)
* \[[`587367d107`](https://github.com/nodejs/node/commit/587367d107)] - **(SEMVER-MAJOR)** **perf\_hooks**: expose webperf global scope interfaces (Chengzhong Wu) [#44483](https://github.com/nodejs/node/pull/44483)
* \[[`364c0e196c`](https://github.com/nodejs/node/commit/364c0e196c)] - **(SEMVER-MAJOR)** **perf\_hooks**: fix webperf idlharness (Chengzhong Wu) [#44483](https://github.com/nodejs/node/pull/44483)
* \[[`ada2d053ae`](https://github.com/nodejs/node/commit/ada2d053ae)] - **(SEMVER-MAJOR)** **process**: runtime deprecate coercion to integer in `process.exit()` (Daeyeon Jeong) [#44711](https://github.com/nodejs/node/pull/44711)
* \[[`e0ab8dd637`](https://github.com/nodejs/node/commit/e0ab8dd637)] - **(SEMVER-MAJOR)** **process**: make process.config read only (Sergey Petushkov) [#43627](https://github.com/nodejs/node/pull/43627)
* \[[`481a959adb`](https://github.com/nodejs/node/commit/481a959adb)] - **(SEMVER-MAJOR)** **readline**: remove `question` method from `InterfaceConstructor` (Antoine du Hamel) [#44606](https://github.com/nodejs/node/pull/44606)
* \[[`c9602ce212`](https://github.com/nodejs/node/commit/c9602ce212)] - **(SEMVER-MAJOR)** **src**: use new v8::OOMErrorCallback API (Michaël Zasso) [#44741](https://github.com/nodejs/node/pull/44741)
* \[[`19a70c11e4`](https://github.com/nodejs/node/commit/19a70c11e4)] - **(SEMVER-MAJOR)** **src**: override CreateJob instead of PostJob (Clemens Backes) [#44741](https://github.com/nodejs/node/pull/44741)
* \[[`fd52c62bee`](https://github.com/nodejs/node/commit/fd52c62bee)] - **(SEMVER-MAJOR)** **src**: use V8\_ENABLE\_SANDBOX macro (Michaël Zasso) [#44741](https://github.com/nodejs/node/pull/44741)
* \[[`c10988db44`](https://github.com/nodejs/node/commit/c10988db44)] - **(SEMVER-MAJOR)** **src**: use non-deprecated V8 inspector API (Michaël Zasso) [#44741](https://github.com/nodejs/node/pull/44741)
* \[[`3efe901dd6`](https://github.com/nodejs/node/commit/3efe901dd6)] - **(SEMVER-MAJOR)** **src**: update NODE\_MODULE\_VERSION to 111 (Michaël Zasso) [#44741](https://github.com/nodejs/node/pull/44741)
* \[[`77e585657f`](https://github.com/nodejs/node/commit/77e585657f)] - **(SEMVER-MAJOR)** **src**: turn embedder api overload into default argument (Alena Khineika) [#43629](https://github.com/nodejs/node/pull/43629)
* \[[`dabda03ea9`](https://github.com/nodejs/node/commit/dabda03ea9)] - **(SEMVER-MAJOR)** **src**: per-environment time origin value (Chengzhong Wu) [#43781](https://github.com/nodejs/node/pull/43781)
* \[[`2e49b99cc2`](https://github.com/nodejs/node/commit/2e49b99cc2)] - **(SEMVER-MAJOR)** **src,test**: disable freezing V8 flags on initialization (Clemens Backes) [#44741](https://github.com/nodejs/node/pull/44741)
* \[[`2b32985c62`](https://github.com/nodejs/node/commit/2b32985c62)] - **(SEMVER-MAJOR)** **stream**: use null for the error argument (Luigi Pinca) [#44312](https://github.com/nodejs/node/pull/44312)
* \[[`36805e8524`](https://github.com/nodejs/node/commit/36805e8524)] - **(SEMVER-MAJOR)** **test**: adapt test-repl for V8 update (Michaël Zasso) [#44741](https://github.com/nodejs/node/pull/44741)
* \[[`96ef25793d`](https://github.com/nodejs/node/commit/96ef25793d)] - **(SEMVER-MAJOR)** **test**: adapt test-repl-pretty-\*stack to V8 changes (Michaël Zasso) [#44741](https://github.com/nodejs/node/pull/44741)
* \[[`71c193e581`](https://github.com/nodejs/node/commit/71c193e581)] - **(SEMVER-MAJOR)** **test**: adapt to new JSON SyntaxError messages (Michaël Zasso) [#44741](https://github.com/nodejs/node/pull/44741)
* \[[`b5f1564880`](https://github.com/nodejs/node/commit/b5f1564880)] - **(SEMVER-MAJOR)** **test**: rename always-opt flag to always-turbofan (Michaël Zasso) [#44741](https://github.com/nodejs/node/pull/44741)
* \[[`1acf0339dd`](https://github.com/nodejs/node/commit/1acf0339dd)] - **(SEMVER-MAJOR)** **test**: fix test-hash-seed for new V8 versions (Michaël Zasso) [#44741](https://github.com/nodejs/node/pull/44741)
* \[[`57ff476c33`](https://github.com/nodejs/node/commit/57ff476c33)] - **(SEMVER-MAJOR)** **test**: remove duplicate test (Luigi Pinca) [#44051](https://github.com/nodejs/node/pull/44051)
* \[[`77def91bf9`](https://github.com/nodejs/node/commit/77def91bf9)] - **(SEMVER-MAJOR)** **tls,http2**: send fatal alert on ALPN mismatch (Tobias Nießen) [#44031](https://github.com/nodejs/node/pull/44031)
* \[[`4860ad99b9`](https://github.com/nodejs/node/commit/4860ad99b9)] - **(SEMVER-MAJOR)** **tools**: update V8 gypfiles for 10.7 (Michaël Zasso) [#44741](https://github.com/nodejs/node/pull/44741)

### Semver-Minor Commits

* \[[`af0921d877`](https://github.com/nodejs/node/commit/af0921d877)] - **(SEMVER-MINOR)** **esm**: add `--import` flag (Moshe Atlow) [#43942](https://github.com/nodejs/node/pull/43942)
* \[[`0633e9a0b5`](https://github.com/nodejs/node/commit/0633e9a0b5)] - **(SEMVER-MINOR)** **lib**: add diagnostics channel for process and worker (theanarkh) [#44045](https://github.com/nodejs/node/pull/44045)
* \[[`ca5be26b31`](https://github.com/nodejs/node/commit/ca5be26b31)] - **(SEMVER-MINOR)** **src**: add support for externally shared js builtins (Michael Dawson) [#44376](https://github.com/nodejs/node/pull/44376)
* \[[`e86a638305`](https://github.com/nodejs/node/commit/e86a638305)] - **(SEMVER-MINOR)** **src**: add initial shadow realm support (Chengzhong Wu) [#42869](https://github.com/nodejs/node/pull/42869)
* \[[`71ca6d7d6a`](https://github.com/nodejs/node/commit/71ca6d7d6a)] - **(SEMVER-MINOR)** **util**: add `maxArrayLength` option to Set and Map (Kohei Ueno) [#43576](https://github.com/nodejs/node/pull/43576)

### Semver-Patch Commits

* \[[`78508028e3`](https://github.com/nodejs/node/commit/78508028e3)] - **bootstrap**: generate bootstrapper arguments in BuiltinLoader (Joyee Cheung) [#44488](https://github.com/nodejs/node/pull/44488)
* \[[`5291096ca2`](https://github.com/nodejs/node/commit/5291096ca2)] - **bootstrap**: check more metadata when loading the snapshot (Joyee Cheung) [#44132](https://github.com/nodejs/node/pull/44132)
* \[[`d0f73d383d`](https://github.com/nodejs/node/commit/d0f73d383d)] - **build**: go faster, drop -fno-omit-frame-pointer (Ben Noordhuis) [#44452](https://github.com/nodejs/node/pull/44452)
* \[[`214354fc9f`](https://github.com/nodejs/node/commit/214354fc9f)] - **crypto**: fix webcrypto HMAC "get key length" in deriveKey and generateKey (Filip Skokan) [#44917](https://github.com/nodejs/node/pull/44917)
* \[[`40a0757b21`](https://github.com/nodejs/node/commit/40a0757b21)] - **crypto**: remove webcrypto HKDF and PBKDF2 default-applied lengths (Filip Skokan) [#44945](https://github.com/nodejs/node/pull/44945)
* \[[`eeec3eb16a`](https://github.com/nodejs/node/commit/eeec3eb16a)] - **crypto**: simplify webcrypto ECDH deriveBits (Filip Skokan) [#44946](https://github.com/nodejs/node/pull/44946)
* \[[`0be1c57281`](https://github.com/nodejs/node/commit/0be1c57281)] - **deps**: V8: cherry-pick c2792e58035f (Jiawen Geng) [#44961](https://github.com/nodejs/node/pull/44961)
* \[[`488474618c`](https://github.com/nodejs/node/commit/488474618c)] - **deps**: V8: cherry-pick c3dffe6e2bda (Michaël Zasso) [#44958](https://github.com/nodejs/node/pull/44958)
* \[[`34ba631a0b`](https://github.com/nodejs/node/commit/34ba631a0b)] - **deps**: V8: cherry-pick e7f0f26f5ef3 (Michaël Zasso) [#44958](https://github.com/nodejs/node/pull/44958)
* \[[`690a837f4f`](https://github.com/nodejs/node/commit/690a837f4f)] - **deps**: V8: cherry-pick 3d59a3c2c164 (Michaël Zasso) [#44958](https://github.com/nodejs/node/pull/44958)
* \[[`bab8b3aad6`](https://github.com/nodejs/node/commit/bab8b3aad6)] - **deps**: V8: cherry-pick 8b8703953616 (Michaël Zasso) [#44958](https://github.com/nodejs/node/pull/44958)
* \[[`37e5152245`](https://github.com/nodejs/node/commit/37e5152245)] - **doc**: add notable changes to latest v18.x release changelog (Danielle Adams) [#44996](https://github.com/nodejs/node/pull/44996)
* \[[`19a909902a`](https://github.com/nodejs/node/commit/19a909902a)] - **doc**: deprecate url.parse() (Rich Trott) [#44919](https://github.com/nodejs/node/pull/44919)
* \[[`6686d9000b`](https://github.com/nodejs/node/commit/6686d9000b)] - **doc**: fix backticks in fs API docs (Livia Medeiros) [#44962](https://github.com/nodejs/node/pull/44962)
* \[[`46a3afb579`](https://github.com/nodejs/node/commit/46a3afb579)] - **doc**: graduate webcrypto to stable (Filip Skokan) [#44897](https://github.com/nodejs/node/pull/44897)
* \[[`6e3c55cc35`](https://github.com/nodejs/node/commit/6e3c55cc35)] - **doc**: fix v16.17.1 security release changelog (Ruy Adorno) [#44759](https://github.com/nodejs/node/pull/44759)
* \[[`77cb88b91c`](https://github.com/nodejs/node/commit/77cb88b91c)] - **doc**: mark `--import` as experimental (Moshe Atlow) [#44067](https://github.com/nodejs/node/pull/44067)
* \[[`46dcfb3c7b`](https://github.com/nodejs/node/commit/46dcfb3c7b)] - **doc,crypto**: update webcrypto docs for global access (Filip Skokan) [#44723](https://github.com/nodejs/node/pull/44723)
* \[[`f594cc85b7`](https://github.com/nodejs/node/commit/f594cc85b7)] - **esm**: remove specifier resolution flag (Geoffrey Booth) [#44859](https://github.com/nodejs/node/pull/44859)
* \[[`3c040348fe`](https://github.com/nodejs/node/commit/3c040348fe)] - _**Revert**_ "**esm**: convert `resolve` hook to synchronous" (Jacob Smith) [#43526](https://github.com/nodejs/node/pull/43526)
* \[[`90b634a5a5`](https://github.com/nodejs/node/commit/90b634a5a5)] - **esm**: convert `resolve` hook to synchronous (Jacob Smith) [#43363](https://github.com/nodejs/node/pull/43363)
* \[[`7c06eab1dc`](https://github.com/nodejs/node/commit/7c06eab1dc)] - _**Revert**_ "**http**: do not leak error listeners" (Luigi Pinca) [#44921](https://github.com/nodejs/node/pull/44921)
* \[[`464d1c1558`](https://github.com/nodejs/node/commit/464d1c1558)] - **lib**: reset `RegExp` statics before running user code (Antoine du Hamel) [#43741](https://github.com/nodejs/node/pull/43741)
* \[[`15f10515e3`](https://github.com/nodejs/node/commit/15f10515e3)] - **module**: fix segment deprecation for imports field (Guy Bedford) [#44883](https://github.com/nodejs/node/pull/44883)
* \[[`7cdf745fdd`](https://github.com/nodejs/node/commit/7cdf745fdd)] - **perf\_hooks**: convert maxSize to IDL value in setResourceTimingBufferSize (Chengzhong Wu) [#44902](https://github.com/nodejs/node/pull/44902)
* \[[`be525d7d04`](https://github.com/nodejs/node/commit/be525d7d04)] - **src**: consolidate exit codes in the code base (Joyee Cheung) [#44746](https://github.com/nodejs/node/pull/44746)
* \[[`d5ce285c8b`](https://github.com/nodejs/node/commit/d5ce285c8b)] - **src**: refactor BaseObject methods (Joyee Cheung) [#44796](https://github.com/nodejs/node/pull/44796)
* \[[`717465433c`](https://github.com/nodejs/node/commit/717465433c)] - **src**: create BaseObject with node::Realm (Chengzhong Wu) [#44348](https://github.com/nodejs/node/pull/44348)
* \[[`45f2258f74`](https://github.com/nodejs/node/commit/45f2258f74)] - **src**: restore IS\_RELEASE to 0 (Bryan English) [#44758](https://github.com/nodejs/node/pull/44758)
* \[[`1f54fc25cb`](https://github.com/nodejs/node/commit/1f54fc25cb)] - **src**: use automatic memory mgmt in SecretKeyGen (Tobias Nießen) [#44479](https://github.com/nodejs/node/pull/44479)
* \[[`7371d335ac`](https://github.com/nodejs/node/commit/7371d335ac)] - **src**: use V8 entropy source if RAND\_bytes() != 1 (Tobias Nießen) [#44493](https://github.com/nodejs/node/pull/44493)
* \[[`81d9cdb8cd`](https://github.com/nodejs/node/commit/81d9cdb8cd)] - **src**: introduce node::Realm (Chengzhong Wu) [#44179](https://github.com/nodejs/node/pull/44179)
* \[[`ad41c919df`](https://github.com/nodejs/node/commit/ad41c919df)] - **src**: remove v8abbr.h (Tobias Nießen) [#44402](https://github.com/nodejs/node/pull/44402)
* \[[`fddc701d3c`](https://github.com/nodejs/node/commit/fddc701d3c)] - **src**: support diagnostics channel in the snapshot (Joyee Cheung) [#44193](https://github.com/nodejs/node/pull/44193)
* \[[`d70aab663c`](https://github.com/nodejs/node/commit/d70aab663c)] - **src**: support WeakReference in snapshot (Joyee Cheung) [#44193](https://github.com/nodejs/node/pull/44193)
* \[[`4ca398a617`](https://github.com/nodejs/node/commit/4ca398a617)] - **src**: iterate over base objects to prepare for snapshot (Joyee Cheung) [#44192](https://github.com/nodejs/node/pull/44192)
* \[[`8b0e5b19bd`](https://github.com/nodejs/node/commit/8b0e5b19bd)] - **src**: fix cppgc incompatibility in v8 (Shelley Vohr) [#43521](https://github.com/nodejs/node/pull/43521)
* \[[`3fdf6cfad9`](https://github.com/nodejs/node/commit/3fdf6cfad9)] - **stream**: fix `size` function returned from QueuingStrategies (Daeyeon Jeong) [#44867](https://github.com/nodejs/node/pull/44867)
* \[[`331088f4a4`](https://github.com/nodejs/node/commit/331088f4a4)] - _**Revert**_ "**tools**: refactor `tools/license2rtf` to ESM" (Richard Lau) [#43214](https://github.com/nodejs/node/pull/43214)
* \[[`30cb1bf8b8`](https://github.com/nodejs/node/commit/30cb1bf8b8)] - **tools**: refactor `tools/license2rtf` to ESM (Feng Yu) [#43101](https://github.com/nodejs/node/pull/43101)
* \[[`a3ff4bfc66`](https://github.com/nodejs/node/commit/a3ff4bfc66)] - **url**: revert "validate ipv4 part length" (Antoine du Hamel) [#42940](https://github.com/nodejs/node/pull/42940)
* \[[`87d0d7a069`](https://github.com/nodejs/node/commit/87d0d7a069)] - **url**: validate ipv4 part length (Yagiz Nizipli) [#42915](https://github.com/nodejs/node/pull/42915)
* \[[`5b1bcf82f1`](https://github.com/nodejs/node/commit/5b1bcf82f1)] - **vm**: make ContextifyContext a BaseObject (Joyee Cheung) [#44796](https://github.com/nodejs/node/pull/44796)

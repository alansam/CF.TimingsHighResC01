# CF.TimingsHighResC01

A sample program to compare time differences between [`malloc()`](https://www.manpagez.com/man/3/malloc/),
`malloc()` plus [`memset()`](https://www.manpagez.com/man/3/memset/) , [`calloc()`](https://www.manpagez.com/man/3/calloc/),
[`mmap()`](https://www.manpagez.com/man/2/mmap/) and `mmap()` plus `memset()`.
The time differences are calculated using the [`clock_gettime()`](https://www.manpagez.com/man/3/clock_gettime/) high&ndash;resolution timing functions.

The program sets up the timers and constructs a series of loops containing calls the memory allocation functions. When a loop terminates the time
difference is calculated and the results are displayed to nanosecond precision.

## Sample Output

```
CF.TimingsHighResC01

                  CLOCK_REALTIME :  0 : true
              malloc     0:546195000
data at address: 0x100498000 8080808080808080
data at address: 0x100498200 8080808080808080
0x100498000 0x100498200 80 40

       malloc,memset     3:621712000
data at address: 0x100498000 8080808080808080
data at address: 0x100498200 8080808080808080
0x100498000 0x100498200 80 40

              calloc     4:818925000
data at address: 0x100498000 8080808080808080
data at address: 0x100498200 8080808080808080
0x100498000 0x100498200 80 40

                mmap     1:038662000
data at address: 0x105d80000 0000000000000000
data at address: 0x105d80200 0000000000000000
0x105d80000 0x105d80200 80 40

         mmap,memset    53:538519000
data at address: 0x105d80000 8080808080808080
data at address: 0x105d80200 8080808080808080
0x105d80000 0x105d80200 80 40


                 CLOCK_MONOTONIC :  6 : true
              malloc     0:489173000
data at address: 0x100498000 8080808080808080
data at address: 0x100498200 8080808080808080
0x100498000 0x100498200 80 40

       malloc,memset     2:595601000
data at address: 0x100498000 8080808080808080
data at address: 0x100498200 8080808080808080
0x100498000 0x100498200 80 40

              calloc     4:864319000
data at address: 0x100498000 8080808080808080
data at address: 0x100498200 8080808080808080
0x100498000 0x100498200 80 40

                mmap     1:172371000
data at address: 0x105d80000 0000000000000000
data at address: 0x105d80200 0000000000000000
0x105d80000 0x105d80200 80 40

         mmap,memset    59:687880000
data at address: 0x105d80000 8080808080808080
data at address: 0x105d80200 8080808080808080
0x105d80000 0x105d80200 80 40


             CLOCK_MONOTONIC_RAW :  4 : true
              malloc     1:085889718
data at address: 0x100498000 8080808080808080
data at address: 0x100498200 8080808080808080
0x100498000 0x100498200 80 40

       malloc,memset     3:472035524
data at address: 0x100498000 8080808080808080
data at address: 0x100498200 8080808080808080
0x100498000 0x100498200 80 40

              calloc     5:101045555
data at address: 0x100498000 8080808080808080
data at address: 0x100498200 8080808080808080
0x100498000 0x100498200 80 40

                mmap     1:170369050
data at address: 0x105d80000 0000000000000000
data at address: 0x105d80200 0000000000000000
0x105d80000 0x105d80200 80 40

         mmap,memset    59:920567184
data at address: 0x105d80000 8080808080808080
data at address: 0x105d80200 8080808080808080
0x105d80000 0x105d80200 80 40


      CLOCK_MONOTONIC_RAW_APPROX :  5 : false

                CLOCK_UPTIME_RAW :  8 : true
              malloc     0:517407600
data at address: 0x100498000 8080808080808080
data at address: 0x100498200 8080808080808080
0x100498000 0x100498200 80 40

       malloc,memset     2:828293846
data at address: 0x100498000 8080808080808080
data at address: 0x100498200 8080808080808080
0x100498000 0x100498200 80 40

              calloc     7:276902293
data at address: 0x100498000 8080808080808080
data at address: 0x100498200 8080808080808080
0x100498000 0x100498200 80 40

                mmap     1:488872177
data at address: 0x105d80000 0000000000000000
data at address: 0x105d80200 0000000000000000
0x105d80000 0x105d80200 80 40

         mmap,memset    80:691104641
data at address: 0x105d80000 8080808080808080
data at address: 0x105d80200 8080808080808080
0x105d80000 0x105d80200 80 40


         CLOCK_UPTIME_RAW_APPROX :  9 : false

        CLOCK_PROCESS_CPUTIME_ID : 12 : true
              malloc     0:774105000
data at address: 0x100498000 8080808080808080
data at address: 0x100498200 8080808080808080
0x100498000 0x100498200 80 40

       malloc,memset     4:090384000
data at address: 0x100498000 8080808080808080
data at address: 0x100498200 8080808080808080
0x100498000 0x100498200 80 40

              calloc     7:448674000
data at address: 0x100498000 8080808080808080
data at address: 0x100498200 8080808080808080
0x100498000 0x100498200 80 40

                mmap     1:553422000
data at address: 0x105d80000 0000000000000000
data at address: 0x105d80200 0000000000000000
0x105d80000 0x105d80200 80 40

         mmap,memset    67:644514000
data at address: 0x105d80000 8080808080808080
data at address: 0x105d80200 8080808080808080
0x105d80000 0x105d80200 80 40


         CLOCK_THREAD_CPUTIME_ID : 16 : true
              malloc     0:623364831
data at address: 0x100498000 8080808080808080
data at address: 0x100498200 8080808080808080
0x100498000 0x100498200 80 40

       malloc,memset     3:331643335
data at address: 0x100498000 8080808080808080
data at address: 0x100498200 8080808080808080
0x100498000 0x100498200 80 40

              calloc     5:987890477
data at address: 0x100498000 8080808080808080
data at address: 0x100498200 8080808080808080
0x100498000 0x100498200 80 40

                mmap     1:396255748
data at address: 0x105d80000 0000000000000000
data at address: 0x105d80200 0000000000000000
0x105d80000 0x105d80200 80 40

         mmap,memset    64:943335649
data at address: 0x105d80000 8080808080808080
data at address: 0x105d80200 8080808080808080
0x105d80000 0x105d80200 80 40


Test complete
Program ended with exit code: 0
```

## Appendix
### Timer clock identifier constants used by `clock_gettime()`

<dl>
  <dt><code>CLOCK_REALTIME</code></dt>
  <dd>
    the system's real time (i.e. wall time) clock, expressed as the amount of time since the Epoch. This is the same as the value returned by
    <a href="https://www.manpagez.com/man/2/gettimeofday/" target="_blank"><code>gettimeofday(2)</code></a>.
  </dd>
  <dt><code>CLOCK_MONOTONIC</code></dt>
  <dd>
    clock that increments monotonically, tracking the time since an arbitrary point, and will continue to increment while the system is asleep.
  </dd>
  <dt><code>CLOCK_MONOTONIC_RAW</code></dt>
  <dd>
    clock that increments monotonically, tracking the time since an arbitrary point like <code>CLOCK_MONOTONIC</code>. However, this clock is unaffected by
    frequency or time adjustments. It should not be compared to other system time sources.
  </dd>
  <dt><code>CLOCK_MONOTONIC_RAW_APPROX</code></dt>
  <dd>
    like <code>CLOCK_MONOTONIC_RAW</code>, but reads a value cached by the system at context switch. This can be read faster, but at a loss of accuracy as
    it may return values that are milliseconds old.
  </dd>
  <dt><code>CLOCK_UPTIME_RAW</code></dt>
  <dd>
    clock that increments monotonically, in the same manner as <code>CLOCK_MONOTONIC_RAW</code>, but that does not increment while the system is asleep.
    The returned value is identical to the result of 
    <a href="https://developer.apple.com/documentation/kernel/1462446-mach_absolute_time" target="_blank"><code>mach_absolute_time()</code></a> after the
    appropriate <code>mach_timebase</code> conversion is applied.
  </dd>
  <dt><code>CLOCK_UPTIME_RAW_APPROX</code></dt>
  <dd>
    like <code>CLOCK_UPTIME_RAW</code>, but reads a value cached by the system at context switch.  This can be read faster, but at a loss of accuracy as it
    may return values that are milliseconds old.
  </dd>
  <dt><code>CLOCK_PROCESS_CPUTIME_ID</code></dt>
  <dd>
    clock that tracks the amount of CPU (in user- or kernel-mode) used by the calling process.
  </dd>
  <dt><code>CLOCK_THREAD_CPUTIME_ID</code></dt>
  <dd>
    clock that tracks the amount of CPU (in user- or kernel-mode) used by the calling thread.
  </dd>
</dl>

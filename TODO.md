# TODO

- (In progress) Hashes in db should be stored as `:db.type/bytes` instead of `:db.type/string`.
- (In progress) Remove old codec cruft.

- Import full blockchain and perf-tweak it.
  - Immediate goal here is to provide a simple way for people to host a fully-indexed blockchain locally.
- ^ Expose db with http api so that hyzhenhok can be integrated into other tools.
- Add search to explorer.
- Create db function for looking up byte-array values instead of reimplementing the `java.util.Arrays/equals` match every time.
- Create some sort of wrapper/presenter for exposing entity-maps in `hyzhenhok.explorer` where all byte-array values are converted to hex strings so I don't need to manually `bytes->hex` myself.
- Since the new codec style tries to build entity-map-like structures, take advantage of that in constructors by merging decoded codecs instead of plucking keys a la cart.

## Some other goals

- Replicate satoshi-client bugs, but first implement naively.
- Maintain a test-suite that's a union of the suites of other implementations, particularly satoshi-client and BitcoinJ.
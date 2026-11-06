# A drone's infrared video and its KLV metadata

An extract of the MISB sample "Night Flight IR" (`Night Flight IR.mpg`, https://samples.ffmpeg.org/MPEG2/mpegts-klv/),
for isard's example A drone's video (`addVideo({ video, klv })`):

- `night-flight-ir.mp4`: from 161.2 s to 262 s of the sample, its H.264 video scaled to 960 × 540 (`ffmpeg -ss 161.2
  -to 262 -vf scale=960:-2 -c:v libx264 -crf 30 -an -movflags +faststart`);
- `night-flight-ir.klv`: its KLV packets (MISB ST 0601, the UAS Datalink Local Set) from the one at 161.2 s, one after
  another as they are in the sample.

The sample's origin and licence are not stated where it is published; it is a MISB test sample.

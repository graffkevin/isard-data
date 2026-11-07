# A drone's video and its KLV metadata

Esri's sample video for Full Motion Video (ArcGIS Online item `55ec6f32d5e342fcbfba376ca2cc409a`, "Sample video for
Full Motion Video (FMV)", `Truck.ts`): a drone at about 2900 m following a truck on the Interstate 80 east of Cheyenne
(Wyoming), 148 s, 19 September 2012. For isard's example A drone's video (`addVideo({ video, klv })`):

- `truck.mp4`: its H.264 video scaled to 1280 × 720, without its sound (`ffmpeg -an -vf scale=1280:-2 -c:v libx264
  -preset slow -crf 30 -movflags +faststart`);
- `truck.klv`: its KLV packets (MISB ST 0601, the UAS Datalink Local Set), 711 of them, one after another as they are
  in the sample (`ffmpeg -map 0:d -c copy -f data`).

The sample is published by Esri for trying out ArcGIS's Full Motion Video; no licence is stated where it is published.

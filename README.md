# Senorgif's Restim Event Files

A collection of base funscripts and `.events.yml` files created for use with the [Restim Funscript Processor](https://github.com/edger477/funscript-tools/releases/tag/v2.3.5). The events files define timed E-Stim stimulation events that are layered on top of processed funscripts using the app's Custom Event Builder. These were made with/for Restim Funscript Processor v2.3.5

## Usage

1. Open the [Restim Funscript Processor](https://github.com/edger477/funscript-tools/releases/tag/v2.3.5).
2. Load the `.funscript` file from this repo for the matching title.
3. Click **Process Files** to generate the base Restim scripts.
4. Open the **Custom Event Builder**.
5. Load the corresponding `.events.yml` file from this repo.
6. Click **Apply Effects** to apply the events to the processed funscripts.

## Files Included

| Title | Funscript | Events File |
| --- | --- | --- |
| Cock Hero - Audition 3 | `CH Audition 3/Cock Hero - Audition 3.funscript` | `CH Audition 3/Cock Hero - Audition 3.events.yml` |
| Cock Hero - Blue Angel | `CH Blue Angel/ReStim Generated/CH-Blue Angel.funscript` | `CH Blue Angel/ReStim Generated/CH-Blue Angel.events.yml` |
| Champion of Cocknia | `CH Champion of Cocknia/Champion of Cocknia hell.funscript` | `CH Champion of Cocknia/Champion of Cocknia hell.events.yml` |
| Cock Hero Crescendo (MattMan edit) | `CH Crescendo/MattMan FOC/Cock Hero Crescendo (MattMan).funscript` | `CH Crescendo/MattMan FOC/Cock Hero Crescendo (MattMan).events.yml` |
| CH EroClip | `CH Eroclip/CH EroClip.funscript` | `CH Eroclip/CH EroClip.events.yml` |
| CH EroClip (alternate script) | `CH Eroclip/CH EroClip (LG Script).funscript` | `CH Eroclip/CH EroClip (LG Script).events.yml` |
| EroComp V4 | `CH Erocomp/EroCompV4_compressed.funscript` | `CH Erocomp/EroCompV4_compressed.events.yml` |
| Cock Hero Fail | `CH Fail/Cock Hero Fail.funscript` | `CH Fail/Cock Hero Fail.events.yml` |
| Earn Your Release - Definitive Edition | `Earn_your_Release-1080p/Earn Your Release (...).funscript` | `Earn_your_Release-1080p/Earn Your Release (...).events.yml` |
| Shibby - The Box | `Shibby/The-Box/Shibby - The Box (a_human_bot).funscript` | `Shibby/The-Box/Shibby - The Box (a_human_bot).events.yml` |

## .events.yml Format

Each file is a YAML list of timed events under an `events:` key. Every entry has a `time` (milliseconds from start), a `name` (the event type), and a `params` block that overrides the event's defaults.

```yaml
events:
- time: 120000
  name: fast
  params:
    duration_ms: 15000
    volume_boost: 0.05
    ramp_up_ms: 2500
```

### Built-in Event Types

| Event | Description |
| --- | --- |
| `fast` | Increases pulse frequency and volume — intense, faster feeling |
| `fast-stroke` | Like `fast` but also modulates alpha for a stroking sensation |
| `medium-stroke` | Moderate stroke modulation on alpha |
| `slow` | Reduces pulse frequency and volume for a slower feeling |
| `slow-stroke` | Like `slow` but with alpha stroke modulation |
| `lube` | Low frequency, slight volume reduction — simulates a change in sensation |
| `edge` | Edging effect with sinusoidal volume modulation |
| `cum` | Orgasm effect — pulse frequency drop, wide pulse width, volume buzz |
| `stay` | Hold effect with high-frequency buzz |
| `ruin` | Fades volume to zero — ruined orgasm |
| `stop` | Overrides volume to a low level — pause in stimulation |
| `rest` | Rest period — reduces pulse frequency and volume |
| `rest-stroke` | Rest with slow stroke modulation |
| `tranquil` | Gentle sinusoidal volume oscillation |
| `pulse_freq_shift` | Temporarily shifts pulse frequency up or down |
| `volume_shift` | Temporarily shifts volume up or down |
| `pulse_width_shift` | Temporarily shifts pulse width |

### Common Parameters

Parameters vary by event type but the most common ones are:

| Parameter | Description |
| --- | --- |
| `duration_ms` | How long the event lasts (ms) |
| `ramp_up_ms` / `ramp_ms` | Time to ramp up to full effect (ms) |
| `volume_boost` | Additive volume adjustment (e.g. `0.05` = +5%) |
| `stroke_freq` | Frequency of alpha modulation in Hz |
| `stroke_intensity` | Amplitude of stroke modulation (0.0–1.0) |
| `stroke_offset` | Phase/offset for stroke waveform |
| `buzz_freq` | Frequency of volume buzzing modulation |
| `buzz_intensity` | Amplitude of buzz modulation |
| `pulse_rate` | Override pulse frequency (Hz) |
| `pulse_width` | Override pulse width (%) |

## Notes

- some of these are experimental, not tested or WIP so use at your own risk.
- These all use the built in event types.
- Some folders contain alternate scripts for the same funscript (e.g. EroClip has two versions).
- I have inlcuded the base funscripts I used while creating the events, but theoretically these will work with any funscript that works with the source video. 
-Made for Funscr
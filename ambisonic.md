# Ambisonics Audio

HISPlayer SDK v2.13.0 and above supports Ambisonics audio with ambiX format from first order to 3rd order, and TBE format to capture sound in all directions.
It supports headset rotation listener, so the ambisonics audio is locked to the game world when users move the headset around.

## Requirements
#### Unreal Engine version
- Supported Unreal Engine versions: 5.5, 5.6, 5.7, 5.8

It’s required to set **AmbisonicAudio** property in BP_HISPlayer through the Unreal editor.
<p align="center">
<img width="547" height="470" alt="image" src="https://github.com/user-attachments/assets/06add7cf-19e7-4f31-b227-b0e4afe1f13d" />
</p>

* Only Opus audio codec is supported. Opus is the recommended codec for Ambisonic audio.
* MKV video container is recommended.
* Recommended audio sample rate is 48000Hz.
* Multistream mode with ambisonics is not supported.

For more details, please refer to below APIs section and check out our sample, which includes a scene to test this feature: [HISPlayer Meta XR Sample](https://hisplayer.github.io/UnrealMetaQuest-SDK/#/setup-guide?id=hisplayer-vr-sample).

## Related APIs

**EHISPlayerAmbisonicAudio**: Type of ambisonics audio format:
   * **None**: No ambisonics audio
   * **AmbiX_4**: 4 channels of first order ambiX
   * **AmbiX_4_2**: 4 channels of first order ambiX with 2 channels of head-locked audio
   * **AmbiX_9**: 9 channels of second order ambiX
   * **AmbiX_9_2**: 9 channels of second order ambiX with 2 channels of head-locked audio
   * **AmbiX_16**: 16 channels of third order ambiX
   * **AmbiX_16_2**: 16 channels of third order ambiX with 2 channels of head-locked audio
   * **TBE_4**: 4 channels of hybrid TBE ambisonics
   * **TBE_4_2**: 4 channels of hybrid TBE ambisonics and 2 channels of head-locked stereo audio
   * **TBE_6**: 6 channels of hybrid TBE ambisonics
   * **TBE_6_2**: 6 channels of hybrid TBE ambisonics and 2 channels of head-locked stereo audio
   * **TBE_8**: 8 channels of hybrid TBE ambisonics
   * **TBE_8_2**: 8 channels of hybrid TBE ambisonics and 2 channels of head-locked stereo audio

**EHISPlayerAmbisonicAudio AmbisonicAudio**: Ambisonics audio supporting ambiX format from first order to 3rd order, and TBE format. It's set to None by default. To modify this value, please use the Editor.

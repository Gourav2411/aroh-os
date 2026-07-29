# V1 acceptance criteria

A result counts only when it is repeatable on physical hardware and evidence is
captured without exposing personal data.

## Boot and recovery

- [ ] Each device has a written stock-recovery procedure.
- [ ] The primary prototype completes ten consecutive cold boots.
- [ ] A deliberately broken userspace image can be recovered.
- [ ] Build inputs and image hashes are recorded.

## Essential hardware

- [ ] Display, touch, buttons and storage remain stable for one hour.
- [ ] Wi-Fi connects after reboot.
- [ ] Microphone records intelligible speech.
- [ ] Earpiece and speaker play intelligible audio.
- [ ] Main camera captures a correctly oriented photo.
- [ ] Battery level and charging state are reported.

## Communication

- [ ] The phone places and receives a test call, or the modem blocker is proven
      and documented with an approved fallback demo.
- [ ] The phone sends and receives an SMS where supported.
- [ ] Two Aroh devices exchange an end-to-end encrypted text message.
- [ ] Message keys are not written to ordinary logs.

## Intelligence and authority

- [ ] Local intent recognition works without a network for the core demo.
- [ ] The model cannot call privileged services directly.
- [ ] Protected actions show the target and effect before confirmation.
- [ ] Denied capabilities remain denied after restart.
- [ ] Permission revocation takes effect immediately.
- [ ] Every completed protected action creates a user-readable audit event.
- [ ] Prompt injection test content cannot grant a new capability.

## Demonstration

- [ ] “Call a contact” completes with disambiguation and confirmation.
- [ ] “Take a photo” completes with a visible camera indicator.
- [ ] “Send this message” shows recipient and content before sending.
- [ ] Airplane mode and model-runtime failure leave manual recovery controls
      available.
- [ ] Both devices pass the final scenario twice from clean installations.

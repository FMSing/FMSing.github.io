# Table of contents
{:.no_toc}
* toc
{:toc}

# Abstract
![Image](figure1.png){: width="75%"}{: .center}
![Image](figure2.png){: width="85%"}{: .center}
In this paper, we propose Universal MelGAN: a robust waveform generation model for high-fidelity speech synthesis. The proposed model was improved as follows. 1) We increased the hidden channel sizes of the generator by 4 times and applied gated activation unit to the last layer of each residual stack. 2) To alleviate the over-smoothing problem in high frequency domain caused by the larger model size, we designed multi-resolution spectrogram discriminators and attached to the model. As a result, our model trained by hundreds of speakers recorded the best MOS score among the competing baselines in most seen and unseen domain scenarios such as speaker, language, recording condition or emotion in both Korean and English. In text-to-speech, high-fidelity audio was produced regardless of whether seen or unseen speakers(a real-time synthesis speed of 0.028 RTF on NVIDIA V100 GPU). This result obtained without any explicit domain information suggests the possibility of the proposed model as a universal vocoder.

# Korean samples

## Seen speakers scenarios

### Single speaker
<table>
    <thead>
        <th>Index</th>
        <th>Recording</th>
        <th>Universal MelGAN</th>
        <th>FB-MelGAN</th>
        <th>WaveRNN</th>
        <th>WaveGlow</th>
        <th>WaveNet</th>
    </thead>
    <tbody>
        <tr>
            <th>#1</th>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/gt/kor_seen_single/FTTS_dg21445.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/melgan_ours/kor_seen_single/FTTS_dg21445.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/melgan_orig/kor_seen_single/FTTS_dg21445.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/wavernn/kor_seen_single/FTTS_dg21445.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/waveglow/kor_seen_single/FTTS_dg21445.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/wavenet/kor_seen_single/FTTS_dg21445.wav" type="audio/wav"></audio></td>
        </tr>
    </tbody>
    <tbody>
        <tr>
            <th>#1</th>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/gt/kor_seen_single/FTTS_dw09691.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/melgan_ours/kor_seen_single/FTTS_dw09691.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/melgan_orig/kor_seen_single/FTTS_dw09691.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/wavernn/kor_seen_single/FTTS_dw09691.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/waveglow/kor_seen_single/FTTS_dw09691.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/wavenet/kor_seen_single/FTTS_dw09691.wav" type="audio/wav"></audio></td>
        </tr>
    </tbody>
    <tbody>
        <tr>
            <th>#3</th>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/gt/kor_seen_single/FTTS_dw10439.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/melgan_ours/kor_seen_single/FTTS_dw10439.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/melgan_orig/kor_seen_single/FTTS_dw10439.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/wavernn/kor_seen_single/FTTS_dw10439.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/waveglow/kor_seen_single/FTTS_dw10439.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/wavenet/kor_seen_single/FTTS_dw10439.wav" type="audio/wav"></audio></td>
        </tr>
    </tbody>
</table>

### Multiple speakers
<table>
    <thead>
        <th>Index</th>
        <th>Recording</th>
        <th>Universal MelGAN</th>
        <th>FB-MelGAN</th>
        <th>WaveRNN</th>
        <th>WaveGlow</th>
        <th>WaveNet</th>
    </thead>
    <tbody>
        <tr>
            <th>#1</th>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/gt/kor_seen_universal/03.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/melgan_ours/kor_seen_universal/03.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/melgan_orig/kor_seen_universal/03.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/wavernn/kor_seen_universal/03.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/waveglow/kor_seen_universal/03.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/wavenet/kor_seen_universal/03.wav" type="audio/wav"></audio></td>
        </tr>
    </tbody>
    <tbody>
        <tr>
            <th>#2</th>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/gt/kor_seen_universal/04.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/melgan_ours/kor_seen_universal/04.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/melgan_orig/kor_seen_universal/04.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/wavernn/kor_seen_universal/04.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/waveglow/kor_seen_universal/04.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/wavenet/kor_seen_universal/04.wav" type="audio/wav"></audio></td>
        </tr>
    </tbody>
    <tbody>
        <tr>
            <th>#3</th>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/gt/kor_seen_universal/05.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/melgan_ours/kor_seen_universal/05.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/melgan_orig/kor_seen_universal/05.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/wavernn/kor_seen_universal/05.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/waveglow/kor_seen_universal/05.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/wavenet/kor_seen_universal/05.wav" type="audio/wav"></audio></td>
        </tr>
    </tbody>
</table>

## Unseen speakers and out-of-domain scenarios

### Clean, noisy and reverberant
<table>
    <thead>
        <th>Index</th>
        <th>Recording</th>
        <th>Universal MelGAN</th>
        <th>FB-MelGAN</th>
        <th>WaveRNN</th>
        <th>WaveGlow</th>
        <th>WaveNet</th>
    </thead>
    <tbody>
        <tr>
            <th>Clean #1</th>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/gt/kor_ood_unseen_clean/06.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/melgan_ours/kor_ood_unseen_clean/06.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/melgan_orig/kor_ood_unseen_clean/06.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/wavernn/kor_ood_unseen_clean/06.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/waveglow/kor_ood_unseen_clean/06.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/wavenet/kor_ood_unseen_clean/06.wav" type="audio/wav"></audio></td>
        </tr>
    </tbody>
    <tbody>
        <tr>
            <th>Clean #2</th>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/gt/kor_ood_unseen_clean/07.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/melgan_ours/kor_ood_unseen_clean/07.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/melgan_orig/kor_ood_unseen_clean/07.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/wavernn/kor_ood_unseen_clean/07.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/waveglow/kor_ood_unseen_clean/07.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/wavenet/kor_ood_unseen_clean/07.wav" type="audio/wav"></audio></td>
        </tr>
    </tbody>
        <tbody>
        <tr>
            <th>Noisy #1</th>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/gt/kor_ood_noisy/08.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/melgan_ours/kor_ood_noisy/08.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/melgan_orig/kor_ood_noisy/08.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/wavernn/kor_ood_noisy/08.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/waveglow/kor_ood_noisy/08.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/wavenet/kor_ood_noisy/08.wav" type="audio/wav"></audio></td>
        </tr>
    </tbody>
    <tbody>
        <tr>
            <th>Noisy #2</th>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/gt/kor_ood_noisy/09.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/melgan_ours/kor_ood_noisy/09.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/melgan_orig/kor_ood_noisy/09.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/wavernn/kor_ood_noisy/09.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/waveglow/kor_ood_noisy/09.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/wavenet/kor_ood_noisy/09.wav" type="audio/wav"></audio></td>
        </tr>
    </tbody>
        <tbody>
        <tr>
            <th>Reverb #1</th>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/gt/kor_ood_reverberated/10.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/melgan_ours/kor_ood_reverberated/10.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/melgan_orig/kor_ood_reverberated/10.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/wavernn/kor_ood_reverberated/10.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/waveglow/kor_ood_reverberated/10.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/wavenet/kor_ood_reverberated/10.wav" type="audio/wav"></audio></td>
        </tr>
    </tbody>
    <tbody>
        <tr>
            <th>Reverb #2</th>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/gt/kor_ood_reverberated/11.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/melgan_ours/kor_ood_reverberated/11.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/melgan_orig/kor_ood_reverberated/11.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/wavernn/kor_ood_reverberated/11.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/waveglow/kor_ood_reverberated/11.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/wavenet/kor_ood_reverberated/11.wav" type="audio/wav"></audio></td>
        </tr>
    </tbody>
</table>

### Expressive
<table>
    <thead>
        <th>Index</th>
        <th>Recording</th>
        <th>Universal MelGAN</th>
        <th>FB-MelGAN</th>
        <th>WaveRNN</th>
        <th>WaveGlow</th>
        <th>WaveNet</th>
    </thead>
    <tbody>
        <tr>
            <th>Sportscasting</th>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/gt/kor_ood_expressive/12.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/melgan_ours/kor_ood_expressive/12.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/melgan_orig/kor_ood_expressive/12.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/wavernn/kor_ood_expressive/12.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/waveglow/kor_ood_expressive/12.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/wavenet/kor_ood_expressive/12.wav" type="audio/wav"></audio></td>
        </tr>
    </tbody>
    <tbody>
        <tr>
            <th>Anger</th>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/gt/kor_ood_expressive/13.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/melgan_ours/kor_ood_expressive/13.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/melgan_orig/kor_ood_expressive/13.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/wavernn/kor_ood_expressive/13.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/waveglow/kor_ood_expressive/13.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/wavenet/kor_ood_expressive/13.wav" type="audio/wav"></audio></td>
        </tr>
    </tbody>
    <tbody>
        <tr>
            <th>Disgust</th>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/gt/kor_ood_expressive/14.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/melgan_ours/kor_ood_expressive/14.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/melgan_orig/kor_ood_expressive/14.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/wavernn/kor_ood_expressive/14.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/waveglow/kor_ood_expressive/14.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/wavenet/kor_ood_expressive/14.wav" type="audio/wav"></audio></td>
        </tr>
    </tbody>
    <tbody>
        <tr>
            <th>Fear</th>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/gt/kor_ood_expressive/15.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/melgan_ours/kor_ood_expressive/15.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/melgan_orig/kor_ood_expressive/15.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/wavernn/kor_ood_expressive/15.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/waveglow/kor_ood_expressive/15.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/wavenet/kor_ood_expressive/15.wav" type="audio/wav"></audio></td>
        </tr>
    </tbody>
    <tbody>
        <tr>
            <th>Happiness</th>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/gt/kor_ood_expressive/16.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/melgan_ours/kor_ood_expressive/16.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/melgan_orig/kor_ood_expressive/16.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/wavernn/kor_ood_expressive/16.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/waveglow/kor_ood_expressive/16.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/wavenet/kor_ood_expressive/16.wav" type="audio/wav"></audio></td>
        </tr>
    </tbody>
    <tbody>
        <tr>
            <th>Sadness</th>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/gt/kor_ood_expressive/17.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/melgan_ours/kor_ood_expressive/17.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/melgan_orig/kor_ood_expressive/17.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/wavernn/kor_ood_expressive/17.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/waveglow/kor_ood_expressive/17.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/wavenet/kor_ood_expressive/17.wav" type="audio/wav"></audio></td>
        </tr>
    </tbody>
</table>

### Unseen languages
<table>
    <thead>
        <th>Index</th>
        <th>Recording</th>
        <th>Universal MelGAN</th>
        <th>FB-MelGAN</th>
        <th>WaveRNN</th>
        <th>WaveGlow</th>
        <th>WaveNet</th>
    </thead>
    <tbody>
        <tr>
            <th>Spanish</th>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/gt/kor_ood_unseen_languages/18.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/melgan_ours/kor_ood_unseen_languages/18.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/melgan_orig/kor_ood_unseen_languages/18.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/wavernn/kor_ood_unseen_languages/18.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/waveglow/kor_ood_unseen_languages/18.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/wavenet/kor_ood_unseen_languages/18.wav" type="audio/wav"></audio></td>
        </tr>
    </tbody>
    <tbody>
        <tr>
            <th>German</th>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/gt/kor_ood_unseen_languages/19.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/melgan_ours/kor_ood_unseen_languages/19.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/melgan_orig/kor_ood_unseen_languages/19.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/wavernn/kor_ood_unseen_languages/19.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/waveglow/kor_ood_unseen_languages/19.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/wavenet/kor_ood_unseen_languages/19.wav" type="audio/wav"></audio></td>
        </tr>
    </tbody>
    <tbody>
        <tr>
            <th>French</th>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/gt/kor_ood_unseen_languages/20.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/melgan_ours/kor_ood_unseen_languages/20.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/melgan_orig/kor_ood_unseen_languages/20.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/wavernn/kor_ood_unseen_languages/20.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/waveglow/kor_ood_unseen_languages/20.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/wavenet/kor_ood_unseen_languages/20.wav" type="audio/wav"></audio></td>
        </tr>
    </tbody>
    <tbody>
        <tr>
            <th>Japanese</th>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/gt/kor_ood_unseen_languages/21.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/melgan_ours/kor_ood_unseen_languages/21.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/melgan_orig/kor_ood_unseen_languages/21.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/wavernn/kor_ood_unseen_languages/21.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/waveglow/kor_ood_unseen_languages/21.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/wavenet/kor_ood_unseen_languages/21.wav" type="audio/wav"></audio></td>
        </tr>
    </tbody>
    <tbody>
        <tr>
            <th>Chinese</th>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/gt/kor_ood_unseen_languages/22.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/melgan_ours/kor_ood_unseen_languages/22.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/melgan_orig/kor_ood_unseen_languages/22.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/wavernn/kor_ood_unseen_languages/22.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/waveglow/kor_ood_unseen_languages/22.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/wavenet/kor_ood_unseen_languages/22.wav" type="audio/wav"></audio></td>
        </tr>
    </tbody>
</table>

## Multi-speaker text-to-speech

### Trained with large datasets
<table>
    <thead>
        <th>Index</th>
        <th>Universal MelGAN</th>
        <th>FB-MelGAN</th>
        <th>WaveRNN</th>
        <th>WaveGlow</th>
        <th>WaveNet</th>
    </thead>
    <tbody>
        <tr>
            <th>#1</th>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/melgan_ours/kor_tts_large/23.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/melgan_orig/kor_tts_large/23.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/wavernn/kor_tts_large/23.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/waveglow/kor_tts_large/23.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/wavenet/kor_tts_large/23.wav" type="audio/wav"></audio></td>
        </tr>
    </tbody>
    <tbody>
        <tr>
            <th>#1</th>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/melgan_ours/kor_tts_large/24.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/melgan_orig/kor_tts_large/24.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/wavernn/kor_tts_large/24.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/waveglow/kor_tts_large/24.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/wavenet/kor_tts_large/24.wav" type="audio/wav"></audio></td>
        </tr>
    </tbody>
    <tbody>
        <tr>
            <th>#3</th>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/melgan_ours/kor_tts_large/25.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/melgan_orig/kor_tts_large/25.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/wavernn/kor_tts_large/25.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/waveglow/kor_tts_large/25.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/wavenet/kor_tts_large/25.wav" type="audio/wav"></audio></td>
        </tr>
    </tbody>
</table>

### Trained with small datasets or unseen datasets
<table>
    <thead>
        <th>Index</th>
        <th>Universal MelGAN</th>
        <th>FB-MelGAN</th>
        <th>WaveRNN</th>
        <th>WaveGlow</th>
        <th>WaveNet</th>
    </thead>
    <tbody>
        <tr>
            <th>#1</th>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/melgan_ours/kor_tts_small/26.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/melgan_orig/kor_tts_small/26.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/wavernn/kor_tts_small/26.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/waveglow/kor_tts_small/26.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/wavenet/kor_tts_small/26.wav" type="audio/wav"></audio></td>
        </tr>
    </tbody>
    <tbody>
        <tr>
            <th>#1</th>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/melgan_ours/kor_tts_small/27.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/melgan_orig/kor_tts_small/27.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/wavernn/kor_tts_small/27.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/waveglow/kor_tts_small/27.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/wavenet/kor_tts_small/27.wav" type="audio/wav"></audio></td>
        </tr>
    </tbody>
    <tbody>
        <tr>
            <th>#3</th>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/melgan_ours/kor_tts_small/28.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/melgan_orig/kor_tts_small/28.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/wavernn/kor_tts_small/28.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/waveglow/kor_tts_small/28.wav" type="audio/wav"></audio></td>
            <td><audio controls style="width: 150px;"><source src="wav_for_demo/kor/wavenet/kor_tts_small/28.wav" type="audio/wav"></audio></td>
        </tr>
    </tbody>
</table>

# English samples

## Seen speakers scenarios

### Single speaker

### Multiple speakers

## Unseen speakers and out-of-domain scenarios

### Clean, noisy and reverberant

### Expressive

### Unseen languages

## Text-to-speech

### LJSpeech

# Additional study

## Korean TTS samples: Multi-band + AMP
(achieved 0.003 RTF on NVIDIA V100 GPU)

## Welcome to GitHub Page

You can use the [editor on GitHub](https://github.com/kallavinka8045/icassp2021/edit/gh-pages/index.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/kallavinka8045/icassp2021/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.

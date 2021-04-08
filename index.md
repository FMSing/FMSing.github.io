

{:.no_toc}
* toc
{:toc}



# Abstract
High-fidelity multi-speaker singing voice synthesis is challenging for vocoder due to the singing voice data shortage, limited speaker generalization, and long-term waveforms modeling. Existing open corpora could not meet requirements for high-fidelity singing voice synthesis since their scale and quality weakness. Furthermore, previous vocoders have difficulty in multi-speaker modeling and a distinct degradation emerges when we adapt them to unseen speaker singing voice generation. To accelerate singing voice researches in the community, we release a large-scale, multi-speaker Chinese singing voice dataset OpenSing. For tackling the difficulty during unseen speaker modeling, we propose FMSing, a fast and multi-speaker vocoder with a generative adversarial network. Specifically, 1) FMSing uses a multi-band generator to speed up both training and inference procedure. 2) to capture and rebuild speaker identity from acoustic feature (i.e., mel-spectrogram), FMSing adopts a speaker conditional discriminator and conditional adversarial training objective. 3) to supervise the reconstruction of speaker representations in spectrum envelopes in the frequency domain, we firstly propose an auxiliary speaker perceptual loss. The joint training approach effectively works in GANs for multi-speaker waveforms modeling. Experimental results verify the effectiveness of OpenSing for singing voice synthesis and show that FMSing synthesizes singing voices of unseen speakers faster with higher quality and similarity over previous methods. The further experiment proves that combined with FastSpeech 2 as an acoustic model, FMSing achieves strong robustness in the multi-speaker singing voice synthesis pipeline. Audio samples are available at <a href="https://FMSing.github.io/"><i>https://FMSing.github.io/</i></a>.


# Multi-speaker modeling (Unseen Speakers)

## Woman
<table>
    <thead>
    <th style="text-align: center">Speaker</th>
    <th style="text-align: center">Recording</th>
    <th style="text-align: center">WaveRNN</th>
    <th style="text-align: center">SC-WaveRNN</th>
    <th style="text-align: center">Parallel WaveGAN</th>
    <th style="text-align: center">MelGAN</th>
    <th style="text-align: center">FMSing</th>
    </thead>
    <tbody>
        <tr>
            <th>#1</th>
            <td style="text-align: center"><audio controls style="width: 150px;"><source src="wav_for_demo/unseen-singsing/gt/women/F1_1_03.wav" type="audio/wav"></audio></td>
            <td style="text-align: center"><audio controls style="width: 150px;"><source src="wav_for_demo/unseen-singsing/waveRNN/women/F1_1_03.wav" type="audio/wav"></audio></td>
            <td style="text-align: center"><audio controls style="width: 150px;"><source src="wav_for_demo/unseen-singsing/gt/women/F1_1_03.wav" type="audio/wav"></audio></td>
            <td style="text-align: center"><audio controls style="width: 150px;"><source src="wav_for_demo/unseen-singsing/pwg_all/women/F1_1_03_gen.wav" type="audio/wav"></audio></td>
            <td style="text-align: center"><audio controls style="width: 150px;"><source src="wav_for_demo/unseen-singsing/FBMelGAN/women/F1_1_03.wav" type="audio/wav"></audio></td>
            <td style="text-align: center"><audio controls style="width: 150px;"><source src="wav_for_demo/unseen-singsing/gt/women/F1_1_03.wav" type="audio/wav"></audio></td>
        </tr>
    </tbody>
    <tbody>
        <tr>
            <th>#2</th>
            <td style="text-align: center"><audio controls style="width: 150px;"><source src="wav_for_demo/unseen-singsing/gt/women/F3_1_02.wav" type="audio/wav"></audio></td>
            <td style="text-align: center"><audio controls style="width: 150px;"><source src="wav_for_demo/unseen-singsing/waveRNN/women/F3_1_02.wav" type="audio/wav"></audio></td>
            <td style="text-align: center"><audio controls style="width: 150px;"><source src="wav_for_demo/unseen-singsing/gt/women/F1_1_03.wav" type="audio/wav"></audio></td>
            <td style="text-align: center"><audio controls style="width: 150px;"><source src="wav_for_demo/unseen-singsing/pwg_all/women/F3_1_02_gen.wav" type="audio/wav"></audio></td>
            <td style="text-align: center"><audio controls style="width: 150px;"><source src="wav_for_demo/unseen-singsing/FBMelGAN/women/F3_1_02.wav" type="audio/wav"></audio></td>
            <td style="text-align: center"><audio controls style="width: 150px;"><source src="wav_for_demo/unseen-singsing/gt/women/F1_1_03.wav" type="audio/wav"></audio></td>
       </tr>
    </tbody>
    <tbody>
        <tr>
            <th>#3</th>
            <td style="text-align: center"><audio controls style="width: 150px;"><source src="wav_for_demo/unseen-singsing/gt/women/F4_2_01.wav" type="audio/wav"></audio></td>
            <td style="text-align: center"><audio controls style="width: 150px;"><source src="wav_for_demo/unseen-singsing/waveRNN/women/F4_2_01.wav" type="audio/wav"></audio></td>
            <td style="text-align: center"><audio controls style="width: 150px;"><source src="wav_for_demo/unseen-singsing/gt/women/F1_1_03.wav" type="audio/wav"></audio></td>
            <td style="text-align: center"><audio controls style="width: 150px;"><source src="wav_for_demo/unseen-singsing/pwg_all/women/F4_2_01_gen.wav" type="audio/wav"></audio></td>
            <td style="text-align: center"><audio controls style="width: 150px;"><source src="wav_for_demo/unseen-singsing/FBMelGAN/women/F4_2_01.wav" type="audio/wav"></audio></td>
            <td style="text-align: center"><audio controls style="width: 150px;"><source src="wav_for_demo/unseen-singsing/gt/women/F1_1_03.wav" type="audio/wav"></audio></td>
        </tr>
    </tbody>
        <tbody>
        <tr>
            <th>#4</th>
            <td style="text-align: center"><audio controls style="width: 150px;"><source src="wav_for_demo/unseen-singsing/gt/women/F5_2_02.wav" type="audio/wav"></audio></td>
            <td style="text-align: center"><audio controls style="width: 150px;"><source src="wav_for_demo/unseen-singsing/waveRNN/women/F5_2_02.wav" type="audio/wav"></audio></td>
            <td style="text-align: center"><audio controls style="width: 150px;"><source src="wav_for_demo/unseen-singsing/gt/women/F1_1_03.wav" type="audio/wav"></audio></td>
            <td style="text-align: center"><audio controls style="width: 150px;"><source src="wav_for_demo/unseen-singsing/pwg_all/women/F5_2_02_gen.wav" type="audio/wav"></audio></td>
            <td style="text-align: center"><audio controls style="width: 150px;"><source src="wav_for_demo/unseen-singsing/FBMelGAN/women/F5_2_02.wav" type="audio/wav"></audio></td>
            <td style="text-align: center"><audio controls style="width: 150px;"><source src="wav_for_demo/unseen-singsing/gt/women/F1_1_03.wav" type="audio/wav"></audio></td>
        </tr>
    </tbody>
    <tbody>
        <tr>
            <th>#5</th>
            <td style="text-align: center"><audio controls style="width: 150px;"><source src="wav_for_demo/unseen-singsing/gt/women/vocal-盛夏的果实_06.wav" type="audio/wav"></audio></td>
            <td style="text-align: center"><audio controls style="width: 150px;"><source src="wav_for_demo/unseen-singsing/waveRNN/women/vocal-盛夏的果实_06.wav" type="audio/wav"></audio></td>
            <td style="text-align: center"><audio controls style="width: 150px;"><source src="wav_for_demo/unseen-singsing/gt/women/F1_1_03.wav" type="audio/wav"></audio></td>
            <td style="text-align: center"><audio controls style="width: 150px;"><source src="wav_for_demo/unseen-singsing/pwg_all/women/vocal-盛夏的果实_06_gen.wav" type="audio/wav"></audio></td>
            <td style="text-align: center"><audio controls style="width: 150px;"><source src="wav_for_demo/unseen-singsing/FBMelGAN/women/vocal-盛夏的果实_06.wav" type="audio/wav"></audio></td>
            <td style="text-align: center"><audio controls style="width: 150px;"><source src="wav_for_demo/unseen-singsing/gt/women/F1_1_03.wav" type="audio/wav"></audio></td>
        </tr>
    </tbody>
    <tbody>
        <tr>
            <th>#6</th>
            <td style="text-align: center"><audio controls style="width: 150px;"><source src="wav_for_demo/unseen-singsing/gt/women/中文女声DM-001-22.wav" type="audio/wav"></audio></td>
            <td style="text-align: center"><audio controls style="width: 150px;"><source src="wav_for_demo/unseen-singsing/waveRNN/women/中文女声DM-001-22.wav" type="audio/wav"></audio></td>
            <td style="text-align: center"><audio controls style="width: 150px;"><source src="wav_for_demo/unseen-singsing/gt/women/F1_1_03.wav" type="audio/wav"></audio></td>
            <td style="text-align: center"><audio controls style="width: 150px;"><source src="wav_for_demo/unseen-singsing/pwg_all/women/中文女声DM-001-22_gen.wav" type="audio/wav"></audio></td>
            <td style="text-align: center"><audio controls style="width: 150px;"><source src="wav_for_demo/unseen-singsing/FBMelGAN/women/中文女声DM-001-22.wav" type="audio/wav"></audio></td>
            <td style="text-align: center"><audio controls style="width: 150px;"><source src="wav_for_demo/unseen-singsing/gt/women/F1_1_03.wav" type="audio/wav"></audio></td>
        </tr>
    </tbody>
</table>

## Man
<table>
    <thead>
    <th style="text-align: center">Speaker</th>
    <th style="text-align: center">Recording</th>
    <th style="text-align: center">WaveRNN</th>
    <th style="text-align: center">SC-WaveRNN</th>
    <th style="text-align: center">Parallel WaveGAN</th>
    <th style="text-align: center">MelGAN</th>
    <th style="text-align: center">FMSing</th>
    </thead>
    <tbody>
        <tr>
            <th>#1</th>
            <td style="text-align: center"><audio controls style="width: 150px;"><source src="wav_for_demo/unseen-singsing/gt/man/m4_1_stc2.wav" type="audio/wav"></audio></td>
            <td style="text-align: center"><audio controls style="width: 150px;"><source src="wav_for_demo/unseen-singsing/waveRNN/man/m4_1_stc2.wav" type="audio/wav"></audio></td>
            <td style="text-align: center"><audio controls style="width: 150px;"><source src="wav_for_demo/unseen-singsing/gt/man/m4_1_stc2.wav" type="audio/wav"></audio></td>
            <td style="text-align: center"><audio controls style="width: 150px;"><source src="wav_for_demo/unseen-singsing/pwg_all/man/m4_1_stc2_gen.wav" type="audio/wav"></audio></td>
            <td style="text-align: center"><audio controls style="width: 150px;"><source src="wav_for_demo/unseen-singsing/FBMelGAN/man/m4_1_stc2.wav" type="audio/wav"></audio></td>
            <td style="text-align: center"><audio controls style="width: 150px;"><source src="wav_for_demo/unseen-singsing/gt/man/m4_1_stc2.wav" type="audio/wav"></audio></td>
        </tr>
    </tbody>
    <tbody>
        <tr>
            <th>#2</th>
            <td style="text-align: center"><audio controls style="width: 150px;"><source src="wav_for_demo/unseen-singsing/gt/man/m9_2_stc6.wav" type="audio/wav"></audio></td>
            <td style="text-align: center"><audio controls style="width: 150px;"><source src="wav_for_demo/unseen-singsing/waveRNN/man/m9_2_stc6.wav" type="audio/wav"></audio></td>
            <td style="text-align: center"><audio controls style="width: 150px;"><source src="wav_for_demo/unseen-singsing/gt/man/m4_1_stc2.wav" type="audio/wav"></audio></td>
            <td style="text-align: center"><audio controls style="width: 150px;"><source src="wav_for_demo/unseen-singsing/pwg_all/man/m9_2_stc6_gen.wav" type="audio/wav"></audio></td>
            <td style="text-align: center"><audio controls style="width: 150px;"><source src="wav_for_demo/unseen-singsing/FBMelGAN/man/m9_2_stc6.wav" type="audio/wav"></audio></td>
            <td style="text-align: center"><audio controls style="width: 150px;"><source src="wav_for_demo/unseen-singsing/gt/man/m4_1_stc2.wav" type="audio/wav"></audio></td>
        </tr>
    </tbody>
    <tbody>
        <tr>
            <th>#3</th>
            <td style="text-align: center"><audio controls style="width: 150px;"><source src="wav_for_demo/unseen-singsing/gt/man/100627002.wav" type="audio/wav"></audio></td>
            <td style="text-align: center"><audio controls style="width: 150px;"><source src="wav_for_demo/unseen-singsing/waveRNN/man/100627002.wav" type="audio/wav"></audio></td>
            <td style="text-align: center"><audio controls style="width: 150px;"><source src="wav_for_demo/unseen-singsing/gt/man/m4_1_stc2.wav" type="audio/wav"></audio></td>
            <td style="text-align: center"><audio controls style="width: 150px;"><source src="wav_for_demo/unseen-singsing/pwg_all/man/100627002_gen.wav" type="audio/wav"></audio></td>
            <td style="text-align: center"><audio controls style="width: 150px;"><source src="wav_for_demo/unseen-singsing/FBMelGAN/man/100627002.wav" type="audio/wav"></audio></td>
            <td style="text-align: center"><audio controls style="width: 150px;"><source src="wav_for_demo/unseen-singsing/gt/man/m4_1_stc2.wav" type="audio/wav"></audio></td>
        </tr>
    </tbody>
        <tbody>
        <tr>
            <th>#4</th>
            <td style="text-align: center"><audio controls style="width: 150px;"><source src="wav_for_demo/unseen-singsing/gt/man/m2_1_stc1.wav" type="audio/wav"></audio></td>
            <td style="text-align: center"><audio controls style="width: 150px;"><source src="wav_for_demo/unseen-singsing/waveRNN/man/m2_1_stc1.wav" type="audio/wav"></audio></td>
            <td style="text-align: center"><audio controls style="width: 150px;"><source src="wav_for_demo/unseen-singsing/gt/man/m4_1_stc2.wav" type="audio/wav"></audio></td>
            <td style="text-align: center"><audio controls style="width: 150px;"><source src="wav_for_demo/unseen-singsing/pwg_all/man/m2_1_stc1_gen.wav" type="audio/wav"></audio></td>
            <td style="text-align: center"><audio controls style="width: 150px;"><source src="wav_for_demo/unseen-singsing/FBMelGAN/man/m2_1_stc1.wav" type="audio/wav"></audio></td>
            <td style="text-align: center"><audio controls style="width: 150px;"><source src="wav_for_demo/unseen-singsing/gt/man/m4_1_stc2.wav" type="audio/wav"></audio></td>
        </tr>
    </tbody>
    <tbody>
        <tr>
            <th>#5</th>
            <td style="text-align: center"><audio controls style="width: 150px;"><source src="wav_for_demo/unseen-singsing/gt/man/m2_2_stc4.wav" type="audio/wav"></audio></td>
            <td style="text-align: center"><audio controls style="width: 150px;"><source src="wav_for_demo/unseen-singsing/waveRNN/man/m2_2_stc4.wav" type="audio/wav"></audio></td>
            <td style="text-align: center"><audio controls style="width: 150px;"><source src="wav_for_demo/unseen-singsing/gt/man/m4_1_stc2.wav" type="audio/wav"></audio></td>
            <td style="text-align: center"><audio controls style="width: 150px;"><source src="wav_for_demo/unseen-singsing/pwg_all/man/m2_2_stc4_gen.wav" type="audio/wav"></audio></td>
            <td style="text-align: center"><audio controls style="width: 150px;"><source src="wav_for_demo/unseen-singsing/FBMelGAN/man/m2_2_stc4.wav" type="audio/wav"></audio></td>
            <td style="text-align: center"><audio controls style="width: 150px;"><source src="wav_for_demo/unseen-singsing/gt/man/m4_1_stc2.wav" type="audio/wav"></audio></td>
        </tr>
    </tbody>
    <tbody>
        <tr>
            <th>#6</th>
            <td style="text-align: center"><audio controls style="width: 150px;"><source src="wav_for_demo/unseen-singsing/gt/man/m3_2_stc4.wav" type="audio/wav"></audio></td>
            <td style="text-align: center"><audio controls style="width: 150px;"><source src="wav_for_demo/unseen-singsing/waveRNN/man/m3_2_stc4.wav" type="audio/wav"></audio></td>
            <td style="text-align: center"><audio controls style="width: 150px;"><source src="wav_for_demo/unseen-singsing/gt/man/m4_1_stc2.wav" type="audio/wav"></audio></td>
            <td style="text-align: center"><audio controls style="width: 150px;"><source src="wav_for_demo/unseen-singsing/pwg_all/man/m3_2_stc4_gen.wav" type="audio/wav"></audio></td>
            <td style="text-align: center"><audio controls style="width: 150px;"><source src="wav_for_demo/unseen-singsing/FBMelGAN/man/m3_2_stc4.wav" type="audio/wav"></audio></td>
            <td style="text-align: center"><audio controls style="width: 150px;"><source src="wav_for_demo/unseen-singsing/gt/man/m4_1_stc2.wav" type="audio/wav"></audio></td>
        </tr>
    </tbody>
</table>

# Cross-gender evaluation


# Singing Voice Synthesis



 ضبط صدا و رسم موج صوتی با پایتون

این پروژه‌ی ساده و کاربردی با استفاده از زبان پایتون، صدای کاربر را از طریق میکروفون ضبط کرده، آن را در یک فایل WAV ذخیره می‌کند و سپس نمودار موج صوتی آن را رسم می‌کند. برای افرادی که علاقه‌مند به **پردازش سیگنال صوتی**، **تشخیص صدا** یا **تحلیل بصری صدا** هستند، این پروژه نقطه‌ی شروع عالی‌ای به حساب می‌آید.

---

 امکانات

*  ضبط صدای زنده از میکروفون (به‌صورت پیش‌فرض: ۳ ثانیه)
*  ذخیره‌ی صدا با فرمت `output.wav`
*  رسم موج صوتی با استفاده از `matplotlib`
*  کد تمیز و قابل فهم برای مبتدی‌ها

---

 پیش‌نیازها

برای اجرای این پروژه، کتابخانه‌های زیر را نصب کنید:

```bash
pip install pyaudio numpy matplotlib
```

**نکته:** در بعضی سیستم‌ها (به‌خصوص ویندوز)، نصب `pyaudio` به‌صورت عادی ممکن نیست. پیشنهاد می‌شود از نسخه‌ی چرخ‌دنده‌ای (wheel) استفاده کنید:
> [https://www.lfd.uci.edu/\~gohlke/pythonlibs/#pyaudio](https://www.lfd.uci.edu/~gohlke/pythonlibs/#pyaudio)

---

 ساختار پروژه

```
├── audio_recorder.py
├── output.wav
└── README.md
```

---

نحوه‌ی اجرا

فایل پایتون را به سادگی اجرا کنید:

```bash
python audio_recorder.py
```

خروجی برنامه به شکل زیر خواهد بود:

```
 Recording...
 Done recording.
 Saved as output.wav
```

سپس نمودار موج صدای ضبط‌شده نمایش داده می‌شود.

---

پیش‌نمایش

<p align="center">
  <img src="https://i.imgur.com/XsI9apv.png" alt="Waveform Example" width="600">
</p>

---

 این برنامه چگونه کار می‌کند؟

1. با استفاده از `PyAudio` صدای ورودی از میکروفون دریافت می‌شود.
2. به مدت مشخص (۳ ثانیه) صدا ضبط شده و فریم‌ها در لیستی ذخیره می‌شوند.
3. فریم‌های صوتی به آرایه‌ی NumPy تبدیل می‌شوند.
4. صدا در قالب فایل `.wav` ذخیره می‌شود.
5. نمودار موج صدا با `matplotlib` رسم می‌شود.

---

✨ ایده‌هایی برای توسعه

*  رسم نمودار زنده‌ی صدا (Live Plot)
*  افزودن تشخیص سکوت یا صدا (Voice Activity Detection)
*  تحلیل طیف فرکانسی (با FFT)
*  ترکیب با کتابخانه‌های تشخیص گفتار

---



Real-Time Audio Recorder & Waveform Plotter

This Python project **records real-time audio**, saves it to a **WAV file**, and **plots the waveform** using `matplotlib`. It uses the `pyaudio` and `wave` libraries to handle audio input and storage, and is great for beginners interested in **audio signal processing**, **voice-based applications**, or **sound visualization**.

---

 Features

*  Records audio from your microphone (default: 3 seconds)
*  Saves audio as `output.wav`
*  Plots the waveform using `matplotlib`
*  Clean and beginner-friendly Python code

---

 Requirements

Install the required libraries using `pip`:

```bash
pip install pyaudio numpy matplotlib
```

>  **Note:** On some systems (especially Windows), you might need to install `pyaudio` from wheel:
> [https://www.lfd.uci.edu/\~gohlke/pythonlibs/#pyaudio](https://www.lfd.uci.edu/~gohlke/pythonlibs/#pyaudio)

---

 Project Structure

```
├── audio_recorder.py
├── output.wav
└── README.md
```

---

 How to Run

Just execute the script:

```bash
python audio_recorder.py
```

You'll see:

```
 Recording...
 Done recording.
 Saved as output.wav
```

Then a waveform plot of your voice will appear.

---

 Preview

<p align="center">
  <img src="https://i.imgur.com/XsI9apv.png" alt="Waveform Example" width="600">
</p>

---

 How It Works

1. **Initialize PyAudio** and open an audio stream from the default input device (microphone).
2. **Record audio** for a set duration (`RECORD_SECONDS`).
3. **Convert the audio frames** to NumPy arrays for further processing.
4. **Save the audio** to a `.wav` file using the `wave` module.
5. **Plot the waveform** with `matplotlib`.

---

✨ You Can Try Extending It With:

*  Real-time visualization (live plot while recording)
*  Voice activity detection (VAD)
*  Frequency spectrum analysis with FFT
*  Integrate with speech recognition libraries

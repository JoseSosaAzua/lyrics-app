<script>
// @ts-nocheck

let recognizing = false;
let outputText = '';

const startRecognition = () => {
    recognizing = true;
    const recognition = new webkitSpeechRecognition() || new SpeechRecognition();
    recognition.lang = 'es-ES';
    recognition.interimResults = true;
    recognition.continuous = true;

    recognition.onresult = event => {
        const result = event.results[event.results.length - 1][0].transcript;
        outputText = result;
    };

    recognition.onend = () => {
        recognizing = false;
    };

    recognition.onerror = event => {
        console.error('Speech recognition error:', event.error);
    };

    recognition.onnomatch = () => {
        console.log('No speech was recognized.');
    };

    recognition.start();
};
</script>

<div class="flex flex-row bg-orange-400 p-10">

    <div class="bg-pink-600 flex items-center justify-center w-full">
        <button
            on:click={startRecognition}
            disabled={recognizing}
            class=""
            >
            {recognizing ? 'Recording...' : 'Start Recording'}
        </button>
    </div>

    <div class="bg-slate-900 flex flex-col w-full">
        <h1 class="text-5xl">Speech to Text</h1>
        <span>
            {outputText}
        </span>
    </div>

</div>

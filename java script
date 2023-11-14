document.getElementById('translateButton').addEventListener('click', function () {
    const inputText = document.getElementById('inputText').value;
    const targetLanguage = document.getElementById('targetLanguage').value;

    // Replace 'YOUR_API_KEY' with your actual Google Translate API key
    const apiKey = 'YOUR_API_KEY';

    const url = `https://translation.googleapis.com/language/translate/v2?key=${apiKey}`;
    const data = {
        q: inputText,
        target: targetLanguage,
    };

    fetch(url, {
        method: 'POST',
        body: JSON.stringify(data),
        headers: {
            'Content-Type': 'application/json',
        },
    })
    .then(response => response.json())
    .then(data => {
        const translation = data.data.translations[0].translatedText;
        document.getElementById('outputText').innerText = translation;
    })
    .catch(error => {
        console.error('Translation error:', error);
    });
});

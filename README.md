# GitGabCompound
GitGabMyAgent
const crypto = require('crypto');

function generateKey() {
    const key = crypto.randomBytes(32).toString('hex');
    console.log('Generated Key:', key);
}

generateKey();

node generate_key.


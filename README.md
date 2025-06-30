## Offers implementation using SDK


## References
https://github.com/adobe/adobe-client-data-layer/wiki


## Launch Setup

import { useEffect } from 'react';

function SetLibrary() {
    useEffect(() => {
        const script = document.createElement('script');
        script.src = 'https://assets.adobedtm.com/4a0c5698386a/52f6ba7a68d1/launch-8a3e12bbb0c1-staging.min.js';
        script.async = true;
        script.onload = () => {
            // This sets a callback to run once the script is successfully loaded. Useful for initializing or calling functions from that script.
            console.log('Script loaded!');
        };
        //To place the script in the <head> tag
        document.head.appendChild(script);

        // Optional: cleanup
        return () => {
            document.head.removeChild(script);
        };
    }, []);

    // React function must have a return statement. So returned null
    return null;
}


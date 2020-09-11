# Release 7.68.0 Library and Headers

This release includes cURL+OpenSSL+Nghttp2 libraries and header files for MacOS, iOS and tvOS projects.

## Versions

	LIBCURL="7.68.0"        # https://curl.haxx.se/download.html
	OPENSSL="1.1.1d"        # https://www.openssl.org/source/
	NGHTTP2="1.40.0"        # https://nghttp2.org/

## Archive

This directory contains the curl and openssl headers (in the `include` folder), the various *.a libraries built along with a MacOS binary for `curl` and `openssl`.

	   |___libcurl-7.68.0-openssl-1.1.1d-nghttp2-1.40.0
             |
             |____cacert.pem
             |
             |____bin/
             |  |____openssl*
             |  |____curl*
             |
             |____lib/
             |  |____iOS/
             |  |____MacOS/
             |  |____tvOS/
             |
             |____include/
                |____openssl/
                |____curl/
 
## Usage

 1. Copy libs and headers to your project.
 2. Import appropriate libraries: "libssl.a", "libcrypto.a", "libcurl.a", "libnghttp2.a".
 3. Reference Headers.
 4. Specifying the flag  "-lz" in "Other Linker Flags" (OTHER_LDFLAGS) setting in the "Linking" section in the Build settings of the target.
 5. Initialize curl in your code:

        #include <curl/curl.h>

        - (void)foo {    
            CURL* cURL = curl_easy_init();  
            ...  
        }



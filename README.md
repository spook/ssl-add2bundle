# ssl-add2bundle
Add certs to a bundle file, but only if not already there.

This simple script will add SSL PEM-format certificates to a bundle file, 
such as /etc/ssl/certs/ca-certificates.crt, but only if the new certs
are not already there.  It checks the fingerprint of each existing
certificate against the fingerprints of the new certs.

To install, put this script into your /usr/bin directory (or any
execyutable place in your PATH), then make it executable:
  chmod +x /usr/bin/ssl-add2bundle

To use:

  ssl-add2bundle /etc/ssl/certs/ca-certificates.crt new-cert-1.pem new-cert-2.pem...

Licensed under the MIT License.

Enjoy!
- Uncle Spook

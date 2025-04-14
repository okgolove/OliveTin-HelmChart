= Key rotation

gpg --full-generate-key

use RSA4096, as ED... isn't supported by HELM

gpg --export <keyid> > pubkey-YYYY-MM-DD.asc. Add this to the gh-pages branch, commit, push.

Edit charts/.../Chart.yaml and change the fingerprint / key URL

Go to GitHub repo secrets, 

add secret value of `gpg --armor --export-secret-key AF5833720407770CEF18C82A96A0784C72FD05AE > foo.asc`

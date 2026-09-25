Here are the steps to get PDF bookmarks and keep hyperlinks:
1.  Run the command that will output your MD into a simple `.html` file:
    ```bash
    pandoc .\resume.md --from=gfm --standalone --css=".\resume.css" -o .\resume.html
    ```
2.  After having your Chromium-based browser installed, use the following (on a Windows machine):
    ```powershell
    & "C:\Program Files (x86)\Microsoft\Edge\Application\msedge.exe" --headless --disable-gpu --no-pdf-header-footer --generate-pdf-document-outline --run-all-compositor-stages-before-draw --print-to-pdf="$PWD\resume.pdf" "file:///$PWD\resume.html"
    ```
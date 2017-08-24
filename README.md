# Rikai champ!

Port of rikaikun (which is a port of rikaichan (which is a port of rikaiXUL)) to
Web Extensions.

## Testing

TODO:

- [x] Get an assertion library and check that __tests__/rikaicontent.html passes
      when loaded directly in a browser.
- [ ] Get the output to be reflected back when running from the command line
      including correctly reporting errors.
- [ ] Drop `__tests__/rikaicontent.js` at this point
- [ ] Setup `package.json` to run these tests
   - [ ] Get Jest to ignore them (might need a jest config JSON file)
   - [ ] Stick an extra `MOZ_HEADLESS=1 slimerjs __tests__/rikaicontent.js`
         command in there.
- [ ] Get all this to work on Travis
    - [ ] Make travis install latest Firefox

### Debugging

For debugging something like the following should work:

`
./node_modules/.bin/slimerjs utils/slimerjs-test-runner.js __tests__/rikaicontent.html  --debug=true -jsconsole
`

Regular running:

`
MOZ_HEADLESS=1 ./node_modules/.bin/slimerjs utils/slimerjs-test-runner.js __tests__/rikaicontent.html
`
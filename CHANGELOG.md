# Changelog

## v1.8.0

- `ActionMailer` interceptors are registered after Rails initialization and no
  longer when loading this gem. If you were using this gem outside Rails, you'll
  need to call `Premailer::Rails.register_interceptors` manually.

## v1.7.0

- Register preview hook for the new previewing functionality introduced in
  rails 4.1.0

- Add example rails application

## v1.6.1

- Remove Nokogiri unicode fix since it's working properly without it by now

- Make sure html part comes before text part

## v1.6.0

- Only use asset pipeline if Rails is defined and if compile is true

- Depend on actionmailer instead of rails

- Check whether `::Rails` is defined before using it

- Add ability to skip premailer

- Test against multiple action mailer versions on travis

- Ensure CSS strings are always UTF-8 encoded

- Require premailer version >= 1.7.9

## v1.5.1

- Prefer precompiled assets over asset pipeline

- Improve construction of file URL when requesting from CDN

- No longer use open-uri

- Remove gzip unzipping after requesting file

## v1.5.0

- No longer support ruby 1.8

- Find linked stylesheets by `rel='stylesheet'` attribute instead of
  `type='text/css'`

- Don't test hpricot on JRuby due to incompatibility

## v1.4.0

- Fix attachments

## v1.3.2

- Rename gem to premailer-rails (drop the 3)

- Add support for rails 4

- Refactor code

- Add support for precompiled assets

- No longer include default `email.css`

## v1.1.0

- Fixed several bugs

- Strip asset digest from CSS path

- Improve nokogiri support

- Request CSS file if asset is not found locally

  This allows you to host all your assets on a CDN and deploy the
  app without the `app/assets` folder.

Thanks to everyone who contributed!

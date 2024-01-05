# WSSCI-Conference-Template

A template for WSSCI meeting websites built using Jekyll.

## Usage

Before the meeting, modify:

- The data file `_data/conference.yml` that configures conference information, including dates, location information, banner images (placed in `assets/images/slideshow`), deadlines, sponsors, and committee members
- Conference intro and description in `index.md`
- Call for papers text and link in `cfp.md`
- Submission information in `submission.md`
- Venue information in `venue.md`
- Registration information in `registration.md`

When the program has been determined, edit or create a schedule YAML file (`_data/schedule.yml`).
You can use the `_data/old-schedule.yml` as a formatting reference. If you have program in PDF format,
add this to the `program_link` field in the configuration file.

You should only need to edit the Markdown files (extension `.md`).
The HTML files (`organization.html`, `program.html`) read from the configuration files.

To build and view the website locally, run `bundle exec make serve`, then use the resulting server address (e.g., http://127.0.0.1:4000/). (You may need to run `bundle install` first to install dependencies.)

## Reference

Based on [@yishanhe](https://github.com/yishanhe)'s [jekyll-conference-template](https://github.com/yishanhe/jekyll-conference-template).

## Todo

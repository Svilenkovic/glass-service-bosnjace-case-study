<a href="https://glassbosnjace.rs/"><img src="media/cover.jpg" alt="Glass Service Bošnjace, home page on a laptop and a phone" width="100%"></a>

# Glass Service Bošnjace

Site for an auto glass shop near Leskovac: a five-step online quote instead of a price list, pages for the towns it covers and insurance explained plainly.

**[glassbosnjace.rs](https://glassbosnjace.rs/)** · [Case study (in Serbian)](https://svilenkovic.com/radovi/glass-service-bosnjace) · [Srpski](README.sr.md)

> [!NOTE]
> Client project. The source code belongs to the client and stays in a private repository. This page describes what I built and how.

<table>
  <tr><td><b>Client</b></td><td>Glass Service Bošnjace</td></tr>
  <tr><td><b>Industry</b></td><td>Auto glass replacement and repair, ADAS calibration</td></tr>
  <tr><td><b>Location</b></td><td>Bošnjace, Leskovac, Serbia</td></tr>
  <tr><td><b>Type</b></td><td>Multi-page website</td></tr>
  <tr><td><b>My role</b></td><td>Design, development, SEO, hosting and maintenance</td></tr>
  <tr><td><b>Stack</b></td><td>PHP 8.3, nginx, PHPMailer</td></tr>
</table>

## About the project

Glass Service Bošnjace replaces and repairs windscreens, side and rear glass, calibrates ADAS cameras after a replacement and drives out to customers across southern Serbia. People call on the day the glass cracks, often from the roadside, so the phone number sits on every screen. Much of the work goes through insurance, and the paperwork for it has its own page.

A price list would have been wrong, because the price depends on the exact glass, sensors, heating and camera. Instead there is a five-step quote form: client, service, location, vehicle, review. The VIN is checked for 17 characters, repairs need photos of the damage, and if a crack was already repaired once the form explains why it can't be done again and offers to switch the request to a replacement. Requests leave from the shop's own domain, signed with its DKIM key.

## What I built

- The services page rebuilt from scratch after I found it was an empty shell: a PHP include failed silently and nineteen URLs returned 200 with nothing between header and footer
- A single place where scripts are loaded, after the same form script ran three times and sent three emails per submission
- Serbian letters restored on the town pages after an earlier pass had stripped everything outside ASCII: about 430 fixes in two rounds, titles and structured data included
- Pages for the towns the shop covers, each about the distance and call-outs to that place, plus a separate page for ADAS calibration
- IPv6 listening added, since mobile networks that prefer IPv6 were not reaching the site at all
- An internal business app for appointments, quotes, stock and invoices, kept separate from the public site

## Results

| | Performance | Accessibility | Best practices | SEO |
| :-- | :-: | :-: | :-: | :-: |
| Mobile | 86 | 100 | 100 | 100 |
| Desktop | 97 | 100 | 100 | 100 |

PageSpeed Insights, lab test of the live site, September 2026. Security headers: 6 of 6. HTML validator: no errors. axe accessibility check: no violations. Structured data: `AutoRepair`.

## Screenshots

<table>
  <tr>
    <td width="68%" valign="top"><img src="media/desktop.webp" alt="Glass Service Bošnjace, home page on a 1440 px screen"></td>
    <td width="32%" valign="top"><img src="media/mobile.webp" alt="Glass Service Bošnjace, home page on a phone"></td>
  </tr>
</table>

<img src="media/inner-1.webp" alt="Complete services: windshield replacement, repair and work billed through insurance">
<sub>Complete services: windshield replacement, repair and work billed through insurance</sub>

<img src="media/inner-2.webp" alt="The &quot;Naši rezultati&quot; (Our results) section: the figures the shop highlights about its work">
<sub>The "Naši rezultati" (Our results) section: the figures the shop highlights about its work</sub>

---

<sub>Built by [D. Svilenković](https://svilenkovic.com).</sub>

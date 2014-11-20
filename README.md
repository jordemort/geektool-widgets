This is a series of Perl scripts I slapped together one night to use with
[GeekTool](http://projects.tynsoe.org/en/geektool/) to
display current IP and weather information on the desktop of my HTPC. This
repository does not contain particularly great or commented or really even
usuable (without at least some surgery) code. It exists only as a reference
point for myself as I rebuild this code as widgets for
[Übersicht](http://tracesof.net/uebersicht/).

The weather stuff is broken out into several fragments, which I did for layout
purposes, since GeekTool can't render HTML. The Übersicht incarnation will
thankfully be able to be a single widget. The geektool-forecast script handles
fetching/caching the current conditions from the forecast.io API (which you
will need a key for), and thenthe geektool-weather-* scripts call it and emit
formatted output based on the JSON blob.

The IP script uses 'dig' and OpenDNS's service to determine your currently
visible external IP. You will need a set of [flag icons](http://www.famfamfam.com/lab/icons/flags/)
named according to the [ISO 3166-1 alpha-2](http://en.wikipedia.org/wiki/ISO_3166-1_alpha-2)
code of each country to use it.

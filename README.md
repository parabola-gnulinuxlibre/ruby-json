# Ruby stdlib 'json' gem, patched to be Free Software

From 1998 to 2007, the Unicode Consortium maintained a library called
CVTUTF.  In 2009, CVTUTF was removed from unicode.org, and the Unicode
Consortium said that every version of CVTUTF had bugs, and that folks
should use the ICU library instead.

CVTUTF was under a custom license that was not Free under the FSF's
definition, not Open Source under the OSI's definition, and not
GPL-compatible.  The Ruby stdlib [JSON
gem](https://github.com/flori/json) uses code taken-from/based-on
CVTUTF.  This has caused much consternation among folks who care about
any of those 3 things.

We have submitted [a PR](https://github.com/flori/json/pull/567) to
the upstream JSON gem to replace this non-Free code with Free code,
however it is not yet merged.  In the mean-time GNU/Linux distros need
Free versions of the JSON gem so that they can ship Ruby.  This
repository maintains several such versions of the gem, for different
Ruby versions.

| Bundled in             | JSON version                   | Parabola support until        |
|------------------------|--------------------------------|-------------------------------|
| Ruby 1.9.0             | JSON 1.1.2 - 1.1.3             |                               |
| Ruby 1.9.1             | JSON 1.1.3 - 1.1.4             |                               |
| Ruby 1.9.2             | JSON 1.4.2                     |                               |
| Ruby 1.9.3             | JSON 1.5.3-29-gf7f7889 - 1.5.5 |                               |
| Ruby 2.0               | JSON 1.7.5 - 1.7.7             |                               |
| Ruby 2.1               | JSON 1.8.1                     |                               |
| Ruby 2.2               | JSON 1.8.1 - 1.8.1.1           |                               |
| Ruby 2.3               | JSON 1.8.3 - 1.8.3.1           |                               |
| Ruby 2.4               | JSON 2.0.2 - 2.0.4             |                               |
| Ruby 2.5               | JSON 2.1.0                     |                               |
| Ruby 2.6               | JSON 2.1.0                     |                               |
|------------------------|--------------------------------|-------------------------------|
| Ruby 2.7               | JSON 2.3.0                     | TBD                           |
| Ruby 3.0               | JSON 2.5.1                     | 2024-08                       |
| Ruby 3.1               | JSON 2.6.1                     | -                             |
| Ruby 3.2               | JSON 2.6.3                     | Whenever Ruby 3.4.0 comes out |
| Ruby 3.3               | JSON 2.7.1                     | -                             |
| Ruby 3.4 (.0.preview1) | JSON 2.7.2                     | -                             |

| JSON base version | vanilla LTS branch           | liberated branch               |
|-------------------|------------------------------|--------------------------------|
| JSON 2.3.0        | [`lts/v2.3.0/vanilla` ![CI status](https://github.com/parabola-gnulinuxlibre/ruby-json/actions/workflows/ci.yml/badge.svg?branch=lts%2Fv2.3.0%2Fvanilla)](https://github.com/parabola-gnulinuxlibre/ruby-json/tree/lts/v2.3.0/vanilla) | [`lts/v2.3.0/no-cvtutf` ![CI status](https://github.com/parabola-gnulinuxlibre/ruby-json/actions/workflows/ci.yml/badge.svg?branch=lts%2Fv2.3.0%2Fno-cvtutf)](https://github.com/parabola-gnulinuxlibre/ruby-json/tree/lts/v2.3.0/no-cvtutf) |
| JSON 2.6.3        | [`lts/v2.6.3/vanilla` ![CI status](https://github.com/parabola-gnulinuxlibre/ruby-json/actions/workflows/ci.yml/badge.svg?branch=lts%2Fv2.6.3%2Fvanilla)](https://github.com/parabola-gnulinuxlibre/ruby-json/tree/lts/v2.6.3/vanilla) | [`lts/v2.6.3/no-cvtutf` ![CI status](https://github.com/parabola-gnulinuxlibre/ruby-json/actions/workflows/ci.yml/badge.svg?branch=lts%2Fv2.6.3%2Fno-cvtutf)](https://github.com/parabola-gnulinuxlibre/ruby-json/tree/lts/v2.6.3/no-cvtutf) |
| JSON `master`   | -                            | [`lukeshu/no-cvtutf` ![CI status](https://github.com/parabola-gnulinuxlibre/ruby-json/actions/workflows/ci.yml/badge.svg?branch=lukeshu%2Fno-cvtutf)](https://github.com/parabola-gnulinuxlibre/ruby-json/tree/lukeshu/no-cvtutf)    |

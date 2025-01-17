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

# Version chart

| Bundled in             | JSON version                   | Parabola support until        |
|------------------------|--------------------------------|-------------------------------|
| Ruby 1.9.0             | JSON 1.1.2 - 1.1.3             | -                             |
| Ruby 1.9.1             | JSON 1.1.3 - 1.1.4             | -                             |
| Ruby 1.9.2             | JSON 1.4.2                     | -                             |
| Ruby 1.9.3             | JSON 1.5.3-29-gf7f7889 - 1.5.5 | -                             |
| Ruby 2.0               | JSON 1.7.5 - 1.7.7             | -                             |
| Ruby 2.1               | JSON 1.8.1                     | -                             |
| Ruby 2.2               | JSON 1.8.1 - 1.8.1.1           | -                             |
| Ruby 2.3               | JSON 1.8.3 - 1.8.3.1           | -                             |
| Ruby 2.4               | JSON 2.0.2 - 2.0.4             | -                             |
| Ruby 2.5               | JSON 2.1.0                     | -                             |
| Ruby 2.6               | JSON 2.1.0                     | -                             |
| Ruby 2.7               | JSON 2.3.0                     | TBD                           |
| Ruby 3.0               | JSON 2.5.1                     | 2024-08                       |
| Ruby 3.1               | JSON 2.6.1                     | -                             |
| Ruby 3.2               | JSON 2.6.3                     | Whenever Ruby 3.4.0 comes out |
| Ruby 3.3               | JSON 2.7.1                     | -                             |
| Ruby 3.4 (.0.preview1) | JSON 2.7.2                     | TBD                           |

# Branches

| JSON base version | status                | vanilla LTS branch           | liberated branch               |
|-------------------|-----------------------|------------------------------|--------------------------------|
| JSON 2.3.0        | active (for Ruby 2.7) | [`lts/v2.3.0/vanilla` ![CI status](https://github.com/parabola-gnulinuxlibre/ruby-json/actions/workflows/ci.yml/badge.svg?branch=lts%2Fv2.3.0%2Fvanilla)](https://github.com/parabola-gnulinuxlibre/ruby-json/tree/lts/v2.3.0/vanilla) | [`lts/v2.3.0/no-cvtutf` ![CI status](https://github.com/parabola-gnulinuxlibre/ruby-json/actions/workflows/ci.yml/badge.svg?branch=lts%2Fv2.3.0%2Fno-cvtutf)](https://github.com/parabola-gnulinuxlibre/ruby-json/tree/lts/v2.3.0/no-cvtutf) |
| JSON 2.6.3        | active (for Ruby 3.2) | [`lts/v2.6.3/vanilla` ![CI status](https://github.com/parabola-gnulinuxlibre/ruby-json/actions/workflows/ci.yml/badge.svg?branch=lts%2Fv2.6.3%2Fvanilla)](https://github.com/parabola-gnulinuxlibre/ruby-json/tree/lts/v2.6.3/vanilla) | [`lts/v2.6.3/no-cvtutf` ![CI status](https://github.com/parabola-gnulinuxlibre/ruby-json/actions/workflows/ci.yml/badge.svg?branch=lts%2Fv2.6.3%2Fno-cvtutf)](https://github.com/parabola-gnulinuxlibre/ruby-json/tree/lts/v2.6.3/no-cvtutf) |
| JSON 2.7.1        | inactive              | [`lts/v2.7.1/vanilla` ![CI status](https://github.com/parabola-gnulinuxlibre/ruby-json/actions/workflows/ci.yml/badge.svg?branch=lts%2Fv2.7.1%2Fvanilla)](https://github.com/parabola-gnulinuxlibre/ruby-json/tree/lts/v2.7.1/vanilla) | [`lts/v2.7.1/no-cvtutf` ![CI status](https://github.com/parabola-gnulinuxlibre/ruby-json/actions/workflows/ci.yml/badge.svg?branch=lts%2Fv2.7.1%2Fno-cvtutf)](https://github.com/parabola-gnulinuxlibre/ruby-json/tree/lts/v2.7.1/no-cvtutf) |
| JSON `master`   | active (for PR)       | -                            | [`lukeshu/no-cvtutf` ![CI status](https://github.com/parabola-gnulinuxlibre/ruby-json/actions/workflows/ci.yml/badge.svg?branch=lukeshu%2Fno-cvtutf)](https://github.com/parabola-gnulinuxlibre/ruby-json/tree/lukeshu/no-cvtutf)    |

# Releases

| Date | Version | Ruby (vendored) | JSON (standalone) |
|------|---------|-----------------|-------------------|
| 2024-02-22 | [`v2.7.1-1.parabola1`](https://github.com/parabola-gnulinuxlibre/ruby-json/commits/6e75be64c896e093075ec99bf94a3f5fc576c283) | Git tag: [`ruby-3.0.6-libre1`](https://github.com/parabola-gnulinuxlibre/ruby-json/releases/tag/ruby-3.0.6-libre1)<br/> tarball: [`ruby-3.0.6-libre1.tar.gz`](https://repo.parabola.nu/other/ruby-libre/ruby-3.0.6-libre1.tar.gz) | Git tag: [`v2.7.1-1.parabola1`](https://github.com/parabola-gnulinuxlibre/ruby-json/releases/tag/v2.7.1-1.parabola1)<br/> tarball: [`6e75be6….tar.gz`](https://github.com/parabola-gnulinuxlibre/ruby-json/archive/6e75be64c896e093075ec99bf94a3f5fc576c283.tar.gz) |
| 2024-05-15 | [`v2.3.0-20-gb67679c`](https://github.com/parabola-gnulinuxlibre/ruby-json/commits/b67679c13bca877e20b7fcd47fb1365f5cc01eb5) | Git tag: [`ruby-2.7.8-libre1`](https://github.com/parabola-gnulinuxlibre/ruby-json/releases/tag/ruby-2.7.8-libre1)<br/> tarball: [`ruby-2.7.8-libre1.tar.gz`](https://repo.parabola.nu/other/ruby-libre/ruby-2.7.8-libre1.tar.gz) | tarball: [`b67679c….tar.gz`](https://github.com/parabola-gnulinuxlibre/ruby-json/archive/b67679c13bca877e20b7fcd47fb1365f5cc01eb5.tar.gz) |
| 2024-08-31 | [`v2.6.3-8-g4bcec6c`](https://github.com/parabola-gnulinuxlibre/ruby-json/commits/4bcec6c2950bdf7e1bbd086e91bdd431577f10a4) | Git tag: [`ruby-3.2.5-libre1`](https://github.com/parabola-gnulinuxlibre/ruby-json/releases/tag/ruby-3.2.5-libre1)<br/> tarball: [`ruby-3.2.5-libre1.tar.gz`](https://repo.parabola.nu/other/ruby-libre/ruby-3.2.5-libre1.tar.gz) | tarball: [`4bcec6c….tar.gz`](https://github.com/parabola-gnulinuxlibre/ruby-json/archive/4bcec6c2950bdf7e1bbd086e91bdd431577f10a4.tar.gz) |


<!-- README.md is generated from README.Rmd. Please edit that file -->
About `meps.prpl`
=================

[![Travis-CI Build Status](https://travis-ci.org/jjchern/meps.prpl.svg?branch=master)](https://travis-ci.org/jjchern/meps.prpl) [![AppVeyor Build Status](https://ci.appveyor.com/api/projects/status/github/jjchern/meps.prpl?branch=master&svg=true)](https://ci.appveyor.com/project/jjchern/meps.prpl) [![CRAN\_Status\_Badge](http://www.r-pkg.org/badges/version/meps.prpl)](https://cran.r-project.org/package=meps.prpl)

The goal of `meps.prpl` is to wrap the Person Round Plan (`prpl`) Public Use Files from the Medical Expenditure Panel Survey (`meps`) Household Component (HC) in an R data package. All variable labels and value labels are included.

Currently the package includes data from 2011-2014.

For more information about the MEPS-PRPL files, see [the AHRQ webpages](https://meps.ahrq.gov/mepsweb/data_stats/download_data_files_results.jsp?cboDataYear=All&cboDataTypeY=1%2CHousehold+Full+Year+File&buttonYearandDataType=Search&cboPufNumber=All&SearchTitle=Person+Round+Plan).

Installation
============

``` r
# install.packages("devtools")
devtools::install_github("jjchern/meps.prpl")

# To uninstall the package, use:
# remove.packages("meps.prpl")
```

Usage
=====

``` r
# Load tibble for better printout
library(tibble)

meps.prpl::f2014
#> # A tibble: 57,710 x 68
#>                         epcpidx dupersid phldridx     estbidx
#>                           <chr>    <chr>    <chr>       <chr>
#>  1 400018A002140001102340001101 40001101 40001102 400018A0021
#>  2 400018A002140001102340001102 40001102 40001102 400018A0021
#>  3 400018A002140001102340001103 40001103 40001102 400018A0021
#>  4 400018A002140001102340001104 40001104 40001102 400018A0021
#>  5 400018A002140001102440001101 40001101 40001102 400018A0021
#>  6 400018A002140001102440001102 40001102 40001102 400018A0021
#>  7 400018A002140001102440001103 40001103 40001102 400018A0021
#>  8 400018A002140001102440001104 40001104 40001102 400018A0021
#>  9 400018A002140001102540001101 40001101 40001102 400018A0021
#> 10 400018A002140001102540001102 40001102 40001102 400018A0021
#> # ... with 57,700 more rows, and 64 more variables: eprsidx <chr>,
#> #   panel <fctr>, rn <fctr>, jobsidx <chr>, jobsinfr <fctr>,
#> #   jobsfile <fctr>, pitflg <fctr>, fyflg <fctr>, cmjins <fctr>,
#> #   emplstat <fctr>, pholder <fctr>, depndnt <fctr>, evalcovr <fctr>,
#> #   status1 <fctr>, status2 <fctr>, status3 <fctr>, status4 <fctr>,
#> #   status5 <fctr>, status6 <fctr>, status7 <fctr>, status8 <fctr>,
#> #   status9 <fctr>, status10 <fctr>, status11 <fctr>, status12 <fctr>,
#> #   status13 <fctr>, status14 <fctr>, status15 <fctr>, status16 <fctr>,
#> #   status17 <fctr>, status18 <fctr>, status19 <fctr>, status20 <fctr>,
#> #   status21 <fctr>, status22 <fctr>, status23 <fctr>, status24 <fctr>,
#> #   decphldr <fctr>, outphldr <fctr>, nopuflg <fctr>, covrout <fctr>,
#> #   typeflag <fctr>, stexch03 <fctr>, stexch23 <fctr>, stshop <fctr>,
#> #   privcat <fctr>, hospinsx <fctr>, msupinsx <fctr>, dentlins <fctr>,
#> #   visionin <fctr>, pmedins <fctr>, cobra <fctr>, covtypin <fctr>,
#> #   oopelig <fctr>, oopprem <fctr>, ooppremx <fctr>, oopx12x <fctr>,
#> #   oopflag <fctr>, premlevx <fctr>, premsubz <fctr>, anndedct <fctr>,
#> #   hsaacct <fctr>, uprhmo <fctr>, namechng <fctr>

meps.prpl::f2013
#> # A tibble: 58,947 x 71
#>                         epcpidx dupersid phldridx     estbidx
#>                           <chr>    <chr>    <chr>       <chr>
#>  1 200042A002120004101320004101 20004101 20004101 200042A0021
#>  2 200042A002120004101320004102 20004102 20004101 200042A0021
#>  3 200042A002120004101320004103 20004103 20004101 200042A0021
#>  4 200042A002120004101420004101 20004101 20004101 200042A0021
#>  5 200042A002120004101420004102 20004102 20004101 200042A0021
#>  6 200042A002120004101420004103 20004103 20004101 200042A0021
#>  7 200042A002120004101520004101 20004101 20004101 200042A0021
#>  8 200042A002120004101520004102 20004102 20004101 200042A0021
#>  9 200042A002120004101520004103 20004103 20004101 200042A0021
#> 10 200063A003120006104420006104 20006104 20006104 200063A0031
#> # ... with 58,937 more rows, and 67 more variables: eprsidx <chr>,
#> #   panel <fctr>, rn <fctr>, jobsidx <chr>, jobsinfr <fctr>,
#> #   jobsfile <fctr>, pitflg <fctr>, fyflg <fctr>, cmjins <fctr>,
#> #   emplstat <fctr>, pholder <fctr>, depndnt <fctr>, evalcovr <fctr>,
#> #   status1 <fctr>, status2 <fctr>, status3 <fctr>, status4 <fctr>,
#> #   status5 <fctr>, status6 <fctr>, status7 <fctr>, status8 <fctr>,
#> #   status9 <fctr>, status10 <fctr>, status11 <fctr>, status12 <fctr>,
#> #   status13 <fctr>, status14 <fctr>, status15 <fctr>, status16 <fctr>,
#> #   status17 <fctr>, status18 <fctr>, status19 <fctr>, status20 <fctr>,
#> #   status21 <fctr>, status22 <fctr>, status23 <fctr>, status24 <fctr>,
#> #   decphldr <fctr>, outphldr <fctr>, nopuflg <fctr>, covrout <fctr>,
#> #   typeflag <fctr>, privcat <fctr>, hospinsx <fctr>, msupinsx <fctr>,
#> #   dentlins <fctr>, visionin <fctr>, pmedins <fctr>, cobra <fctr>,
#> #   covtypin <fctr>, oopelig <fctr>, oopprem <fctr>, ooppremx <fctr>,
#> #   oopx12x <fctr>, oopflag <fctr>, premlevx <fctr>, byfed <fctr>,
#> #   bystate <fctr>, bylocal <fctr>, bysomgov <fctr>, byempl <fctr>,
#> #   byunion <fctr>, byother <fctr>, anndedct <fctr>, hsaacct <fctr>,
#> #   uprhmo <fctr>, namechng <fctr>

meps.prpl::f2012
#> # A tibble: 63,361 x 85
#>                         epcpidx dupersid phldridx     estbidx
#>                           <chr>    <chr>    <chr>       <chr>
#>  1 200042A002120004101120004101 20004101 20004101 200042A0021
#>  2 200042A002120004101120004102 20004102 20004101 200042A0021
#>  3 200042A002120004101120004103 20004103 20004101 200042A0021
#>  4 200042A002120004101220004101 20004101 20004101 200042A0021
#>  5 200042A002120004101220004102 20004102 20004101 200042A0021
#>  6 200042A002120004101220004103 20004103 20004101 200042A0021
#>  7 200042A002120004101320004101 20004101 20004101 200042A0021
#>  8 200042A002120004101320004102 20004102 20004101 200042A0021
#>  9 200042A002120004101320004103 20004103 20004101 200042A0021
#> 10 200109A003120010101120010101 20010101 20010101 200109A0031
#> # ... with 63,351 more rows, and 81 more variables: eprsidx <chr>,
#> #   panel <fctr>, rn <fctr>, jobsidx <chr>, jobsinfr <fctr>,
#> #   jobsfile <fctr>, pitflg <fctr>, fyflg <fctr>, cmjins <fctr>,
#> #   emplstat <fctr>, pholder <fctr>, depndnt <fctr>, evalcovr <fctr>,
#> #   status1 <fctr>, status2 <fctr>, status3 <fctr>, status4 <fctr>,
#> #   status5 <fctr>, status6 <fctr>, status7 <fctr>, status8 <fctr>,
#> #   status9 <fctr>, status10 <fctr>, status11 <fctr>, status12 <fctr>,
#> #   status13 <fctr>, status14 <fctr>, status15 <fctr>, status16 <fctr>,
#> #   status17 <fctr>, status18 <fctr>, status19 <fctr>, status20 <fctr>,
#> #   status21 <fctr>, status22 <fctr>, status23 <fctr>, status24 <fctr>,
#> #   decphldr <fctr>, outphldr <fctr>, nopuflg <fctr>, covrout <fctr>,
#> #   typeflag <fctr>, privcat <fctr>, hospinsx <fctr>, msupinsx <fctr>,
#> #   dentlins <fctr>, visionin <fctr>, pmedins <fctr>, cobra <fctr>,
#> #   covtypin <fctr>, oopelig <fctr>, oopprem <fctr>, ooppremx <fctr>,
#> #   oopx12x <fctr>, oopflag <fctr>, premlevx <fctr>, byfed <fctr>,
#> #   bystate <fctr>, bylocal <fctr>, bysomgov <fctr>, byempl <fctr>,
#> #   byunion <fctr>, byother <fctr>, anndedct <fctr>, hsaacct <fctr>,
#> #   uprhmo <fctr>, uprmnc <fctr>, drlist <fctr>, visitpay <fctr>,
#> #   namechng <fctr>, satelig <fctr>, gtdocprb <fctr>, aprvtret <fctr>,
#> #   aprvdlay <fctr>, lookinf <fctr>, prbfdinf <fctr>, custserv <fctr>,
#> #   prbcstsv <fctr>, paprwrk <fctr>, prbpprwk <fctr>, rateplan <fctr>

meps.prpl::f2011
#> # A tibble: 58,478 x 85
#>                         epcpidx dupersid phldridx     estbidx
#>                           <chr>    <chr>    <chr>       <chr>
#>  1 100070A001110007101310007101 10007101 10007101 100070A0011
#>  2 100070A001110007101310007102 10007102 10007101 100070A0011
#>  3 100070A001110007101310007103 10007103 10007101 100070A0011
#>  4 100070A001110007101310007104 10007104 10007101 100070A0011
#>  5 100070A001110007101410007101 10007101 10007101 100070A0011
#>  6 100070A001110007101410007102 10007102 10007101 100070A0011
#>  7 100070A001110007101410007103 10007103 10007101 100070A0011
#>  8 100070A001110007101410007104 10007104 10007101 100070A0011
#>  9 100070A001110007101510007101 10007101 10007101 100070A0011
#> 10 100070A001110007101510007102 10007102 10007101 100070A0011
#> # ... with 58,468 more rows, and 81 more variables: eprsidx <chr>,
#> #   panel <fctr>, rn <fctr>, jobsidx <chr>, jobsinfr <fctr>,
#> #   jobsfile <fctr>, pitflg <fctr>, fyflg <fctr>, cmjins <fctr>,
#> #   emplstat <fctr>, pholder <fctr>, depndnt <fctr>, evalcovr <fctr>,
#> #   status1 <fctr>, status2 <fctr>, status3 <fctr>, status4 <fctr>,
#> #   status5 <fctr>, status6 <fctr>, status7 <fctr>, status8 <fctr>,
#> #   status9 <fctr>, status10 <fctr>, status11 <fctr>, status12 <fctr>,
#> #   status13 <fctr>, status14 <fctr>, status15 <fctr>, status16 <fctr>,
#> #   status17 <fctr>, status18 <fctr>, status19 <fctr>, status20 <fctr>,
#> #   status21 <fctr>, status22 <fctr>, status23 <fctr>, status24 <fctr>,
#> #   decphldr <fctr>, outphldr <fctr>, nopuflg <fctr>, covrout <fctr>,
#> #   typeflag <fctr>, privcat <fctr>, hospinsx <fctr>, msupinsx <fctr>,
#> #   dentlins <fctr>, visionin <fctr>, pmedins <fctr>, cobra <fctr>,
#> #   covtypin <fctr>, oopelig <fctr>, oopprem <fctr>, ooppremx <fctr>,
#> #   oopx12x <fctr>, oopflag <fctr>, premlevx <fctr>, byfed <fctr>,
#> #   bystate <fctr>, bylocal <fctr>, bysomgov <fctr>, byempl <fctr>,
#> #   byunion <fctr>, byother <fctr>, anndedct <fctr>, hsaacct <fctr>,
#> #   uprhmo <fctr>, uprmnc <fctr>, drlist <fctr>, visitpay <fctr>,
#> #   namechng <fctr>, satelig <fctr>, gtdocprb <fctr>, aprvtret <fctr>,
#> #   aprvdlay <fctr>, lookinf <fctr>, prbfdinf <fctr>, custserv <fctr>,
#> #   prbcstsv <fctr>, paprwrk <fctr>, prbpprwk <fctr>, rateplan <fctr>
```

PAQUETES ESTADÍSTICOS: Durante el curso se manejarán varios paquetes
estadísticos que nos servirán para entender mejor los conceptos y para
realizar análisis Bayesianos.
1) R (http://www.r-project.org/)
Paquetes: R2WinBUGS, R2OpenBUGS, rjags
2) R Studio (http://www.rstudio.com/)
3) WinBUGS (http://www.mrc-bsu.cam.ac.uk/bugs/)
4) OpenBUGS (http://www.openbugs.net/)
5) JAGS (http://sourceforge.net/projects/mcmc-jags/files/JAGS/) 


You install rjags (and R2jags) from within R. Open R, and then type

```
> install.packages("rjags", dependencies=TRUE) 
Installing package into ‘C:/Users/gabriela.flores/Documents/R/win-library/3.3’
(as ‘lib’ is unspecified)
also installing the dependency ‘coda’

trying URL 'https://cran.rstudio.com/bin/windows/contrib/3.3/coda_0.18-1.zip'
Content type 'application/zip' length 199098 bytes (194 KB)
downloaded 194 KB

trying URL 'https://cran.rstudio.com/bin/windows/contrib/3.3/rjags_4-6.zip'
Content type 'application/zip' length 579796 bytes (566 KB)
downloaded 566 KB

package ‘coda’ successfully unpacked and MD5 sums checked
package ‘rjags’ successfully unpacked and MD5 sums checked

The downloaded binary packages are in
	C:\Users\gabriela.flores\AppData\Local\Temp\Rtmpa22eUp\downloaded_packages
> install.packages("R2jags", dependencies=TRUE)
Installing package into ‘C:/Users/gabriela.flores/Documents/R/win-library/3.3’
(as ‘lib’ is unspecified)
also installing the dependencies ‘abind’, ‘R2WinBUGS’

trying URL 'https://cran.rstudio.com/bin/windows/contrib/3.3/abind_1.4-5.zip'
Content type 'application/zip' length 40177 bytes (39 KB)
downloaded 39 KB

trying URL 'https://cran.rstudio.com/bin/windows/contrib/3.3/R2WinBUGS_2.1-21.zip'
Content type 'application/zip' length 779782 bytes (761 KB)
downloaded 761 KB

trying URL 'https://cran.rstudio.com/bin/windows/contrib/3.3/R2jags_0.5-7.zip'
Content type 'application/zip' length 58800 bytes (57 KB)
downloaded 57 KB

package ‘abind’ successfully unpacked and MD5 sums checked
package ‘R2WinBUGS’ successfully unpacked and MD5 sums checked
package ‘R2jags’ successfully unpacked and MD5 sums checked

The downloaded binary packages are in
	C:\Users\gabriela.flores\AppData\Local\Temp\Rtmpa22eUp\downloaded_packages

```
and hit enter after each. If it asks you to select a CRAN mirror, pick “USA (OR)”. This will run installation scripts.
Check that it worked. In R, type

library(rjags)
You should see something like this:

Loading required package: coda Loading required package: lattice Linked to JAGS 3.3.0 Loaded modules: basemod,bugs

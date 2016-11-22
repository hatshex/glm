## PAQUETES ESTADÍSTICOS:
Durante el curso se manejarán varios paquetes estadísticos que nos servirán para entender mejor los conceptos y para realizar análisis Bayesianos.
* R (http://www.r-project.org/)
Paquetes: R2WinBUGS, R2OpenBUGS, R2jags
* R Studio (http://www.rstudio.com/)
* WinBUGS (http://www.mrc-bsu.cam.ac.uk/bugs/)
* OpenBUGS (http://www.openbugs.net/)
* JAGS (http://sourceforge.net/projects/mcmc-jags/files/JAGS/) 

## Para Ubuntu 16.04
El paquete de OpenBugs usa librerías para 32 bits y el Sistema Operativo es de 64 bits, por lo que necesitamos instalar la las librerías comunes en su versión de 32 bits

``` shell
sudo apt-get install gcc-multilib g++-multilib
```

## Instalando R
http://ftp.osuosl.org/pub/cran/

## Instalando R Studio para escritorio

https://www.rstudio.com/products/rstudio/download2/

## Instalando librerías en R rjags y R2jags

Abre R Studio y teclea lo siguiente
```
install.packages('dplyr', 
	    dependencies = TRUE, 
	    repos = "http://cran.us.r-project.org")
install.packages("rjags", dependencies=TRUE) 
install.packages("R2jags", dependencies=TRUE)
install.packages("R2OpenBUGS", dependencies=TRUE)
install.packages("R2WinBUGS", dependencies=TRUE)
install.packages("rmarkdown", dependencies=TRUE)
```

La salida se verá:

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


install.packages("R2OpenBUGS")
Installing package into ‘C:/Users/gabriela.flores/Documents/R/win-library/3.3’
(as ‘lib’ is unspecified)
trying URL 'https://cran.rstudio.com/bin/windows/contrib/3.3/R2OpenBUGS_3.2-3.1.zip'
Content type 'application/zip' length 974250 bytes (951 KB)
downloaded 951 KB

package ‘R2OpenBUGS’ successfully unpacked and MD5 sums checked

The downloaded binary packages are in
	C:\Users\gabriela.flores\AppData\Local\Temp\RtmpOyhKKb\downloaded_packages
	
> install.packages("R2WinBUGS")
Installing package into ‘C:/Users/gabriela.flores/Documents/R/win-library/3.3’
(as ‘lib’ is unspecified)
trying URL 'https://cran.rstudio.com/bin/windows/contrib/3.3/R2WinBUGS_2.1-21.zip'
Content type 'application/zip' length 779782 bytes (761 KB)
downloaded 761 KB

package ‘R2WinBUGS’ successfully unpacked and MD5 sums checked

The downloaded binary packages are in
	C:\Users\gabriela.flores\AppData\Local\Temp\RtmpgZEUVA\downloaded_packages
```
## Para Probar, teclea:
```
> library(rjags)
Linked to JAGS 4.2.0
Loaded modules: basemod,bugs
```

## Algo mal?
```
Loading required package: coda
Error : .onLoad failed in loadNamespace() for 'rjags', details:
  call: fun(libname, pkgname)
  error: Failed to locate any version of JAGS version 4

The rjags package is just an interface to the JAGS library
Make sure you have installed JAGS-4.x.y.exe (for any x >=0, y>=0) from
http://www.sourceforge.net/projects/mcmc-jags/files

Error: package or namespace load failed for ‘rjags’
```

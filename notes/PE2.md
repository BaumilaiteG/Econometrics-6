# Practical Econometrics 2
Vygantas Butkus  


Introductory Notes
====================================

This is not a textbook and it is not intend to be. 
Rather, it is short summary that emphases messages of lectures, 
gives corresponding references and reminds tasks (if any). 
During the course this note will be updated regularly.


### Students assesments

The final score are going to be estimated according a formula given below. 
Give your self a time to understand it: 


```r
round(sum(min(6, sum(tasks, midExam, extraPoints)), goldenPoints, finalExam))
```

The variables are explained in more details:

* `tasks`: during the course you are going to have quite a number of tasks. 
I believe this is the main part of the course. The maximum sum of points is 4, but
please note, that huge (unlimited) number of extra points can be received, 
if you demonstrate extra efforts in the tasks. In addition, please note that the `tasks` 
variable can be positive only if you supplied all the tasks that was required. 
If at least on of obligatory tasks are missing, the sum of total points are going to be 0.
Thus, do all the tasks, event if the deadline is far over.
* `midExam`: in the middle of semester you are going to have mid exam. The possible outcome is 2 points.
* `extraPoints`: extra points are going to serve as system of encouraging. You can get extra points in many situations: 
taking challenges, answering unexpected question in lecture, giving good question and so on. 
Please note, that `extraPoints` can be negative as well. This could happen in the case of cheating (or something).
* `goldenPoints`: golden points are very similar to extra points, but to get those, 
you will have to put extra efforts in it. How to get them will be steaded in course.
* `finalExam` after the semester you are going to have final exam. The total points of the exam is 4.

**Cultural aspects of the course:**

1. During the course students are encourage to collaborate with each other. 
You can freely share thought, ideas and event source codes. 
In addition students can use all the material that can be found in the Internet or textbooks.
Using the materials made by others are absolutely legal and have no negative side effect on your assesment.
But there are two conditions that are strictly mandatory:
  * You have to give all the credits to original source. 
  Please write an explicit note with links and give some comments. 
  * You have to make sure you understand all the details of the code (or ideas) that you are using. 
  You can be asked to comment it in great details. So, please use the material that you fully understand.


2. I am promise to do my best in answering all your question. You can ask freely during the lectures.
Nevertheless, in practical assignments, your tasks is to try to find the answer by your self. 
So, in practical tasks, before asking any question please be prepare to report that 
efforts you have made to get the answer?
For example: what has the Google query that you have used? That function you have already tried to apply?  


3. Reading and assessing other students rapports is an important part of your learning. 
Please be honest to your colleagues and give the best insights. On the other hand, 
you should appreciate all the criticism that you get and accept it as important part of your learning.

4. Any initiative and communication is highly encouraged. 
Thus, If you have any ideas how to make course more productive or interesting, please let me know. 

5. The tasks are always open for deeper analysis. If you
have idea how to reveal topic in more detail please do it - it probably will get you some extra points.
On the other hand, if you are not satisfied with the assignment that you get, 
you are free to give your reasons and negotiate. 
 

### Outline of the course

1. A short intro of the stuff that you already should know (at least most of it):
  * Technical tools: R (RStudio), Rmd files, Git
  * The basic properties and concepts  in statistics
  * Linear regression (with some extensions)

2. Linear regression in the content of time series
  * Basics (concepts, the difference with classical regression)
  * Trends (stochastic vs deterministic)
  * Spurious regression
  * Autoregressive model
  * Transformations  

3. Intro in time series
  * Basics: stationarity, autocorrelation, AIF, PAIF
  * The decomposition of time series 
  * Some common methods: exponential smoothing, moving average, filtering
  * Overview of more advanced methods: HP, Kalman, State Space

4. ARIMA model
  * AR(p)
  * MA(q)
  * RW
  * ARIMA: specification, diagnostic, estimation.
  
5. Overview of other important models:
  * Garch
  * logit

### Learning material

Selected textbooks that can be useful in this course could be found in `literature` folder.
In addition, all references are given at the end o this document.


Moreover, some wonderful online material is available:

* Using R for Introductory Econometrics: http://www.urfie.net/ 
* Forecasting: principles and practice: https://www.otexts.org/fpp 
* Introduction to Probability, Statistics, and Random Processes: https://www.probabilitycourse.com/ 


Chapter 1. Technical tools
=====================================

## Technical requirements

In the course you are going to use tree main software:

* R - environment for statistical computing and graphics
* RStudio - a set of integrated tools designed to help you be more productive with R.
* Git - distributed version control system 


I assume you already know R and how to install it. If not check the links below:

* [Installing R on Windows](https://www.youtube.com/watch?v=mfGFv-iB724&feature=youtu.be)
* [Installing R on Mac](https://www.youtube.com/watch?v=Icawuhf0Yqo&feature=youtu.be)
* [Installing R on Ubuntu (linux) ](https://www.youtube.com/watch?v=P8wx4HY9me0)

In addition to R, it’s highly recommended that you install RStudio, 
which will make your experience with R much more enjoyable.
If you need to install RStudio, you can do so [here](https://www.rstudio.com/products/rstudio/download/).
Select the appropriate installer for your operating system.

Moreover, Git is also quite an important software. 
Git is a free and open source distributed version control system.
It helps you not to get lost in versions of your project. 
In addition it is much easier to merge contributions among 
all team members and always have the newest version of the project.
This is a system that professionals uses quite a lot (please admire it).
Please visit [Git home](https://git-scm.com/) and install it in your system.
Originally Git is command line program, on the other hand, Git might be used with
graphical interface (GUI). Visit [Gits guis page](https://git-scm.com/downloads/guis) 
to select the one that looks best for you.


## Task 1. Rmd in Github

The goal of your first task is to get familiar with R, Rmd files and Git. 

1. Firstly, you have to sign up for [Github account](https://github.com/) and then create a repository
under the name `Econometrics`. 

2. Go to the Google and find some awesome R features, packages, programs, graphs or something.
Pick anything that you think is worth noting. 

2. In `Econometrics` create a subdirectory `task1` and in this subdirectory
create Rmd file with title `task1.Rmd`. Then write a very short summary about the topic you have choose.
Please be polite and give the link to original material.
Try to put some R code snippets and visualization that describes the main essence of your note.
Try to customize something (if possible). And finally make sure that the file can be knited.

3. Commit it to Git and push to Github.
Please note, that RStudio has small GUI for Git. 
It is avalible if you create a project (insted of plain Rmd file).

4. Write an email to me (Vygantas.Butkus@mii.vu.lt) with subject "[PE2][task1] Link to Github".
And give the link to your Github account in the body.

Hint: A [short learning course on git](https://try.github.io/levels/1/challenges/1 could be useful.
Please try it if you are not familial with Git.

Please note that those who demonstrate the greatest quality in their task will have actual opportunity 
to get their first extra points. 

## Task 2. Swirl course

Please visit [swirl](http://swirlstats.com/) website. 
Swirl is a frameworks for interactive R learning.
Your task is to complete R programming course that can be find
in my [GitHub accaunt](https://github.com/1vbutkus/R_Programming).

For a first time, you have to install `swirl` package and the course material. 
Run R commands (be patient, this can take a while):

```r
install.packages('swirl')
library("swirl")
install_course_github("1vbutkus", "swirl", multi=TRUE)
```


To run a course you should type:

```r
library("swirl")
swirl()
```

Follow the instructions and select the "R Programming" course.
Course contains 12 lessons. You have to do all of them. After 
Finishing each lesson, system will generate an email that you have to send to 
vygantas.butkus@mii.vu.lt (with exact subject and body content that will be generated by swirl).

Please note, that there are other courses. They are optional and can be really
useful to increase knowledge and competition in R and data analysis. 
Please help your self.


**Alternative.**
This task have an alternative. If you consider your self being advanced enough in R, then
you can request a personal task. I believe this would be more interesting and more useful.
Contact me personally if you consider doing a personal task. 


Chapter 2. Probability and modeling
=====================================

Literature: the main source is [@Lavine2013a, ch. 1,2]. 
Alternative source is [@Kerns2011a, ch. 4-6, 10].


Key qualifications:

* understand main concepts of random variables (probability mass function, distribution function, quantile function, moments, covariance).
* know how to use R functions of random variables, ex: dnorm, pnorm, qnorm, rnorm
* how to use model custom variables of the forms $f(x)$, where $f$ is some known function, and
$x$ is some classical random variable.
* what is the principal of statistical tests?
* how to summarize modeling results and draw the conclusions.

Note: This chapter is about something that you already should know. 
So, please make sure you understand everything. If not, spend some time to catch up.

<!--
Paskaitos planas:

* Ankstenes paskaitos neišpildyti akcentai:
    * GIT iliustracija: status, add, commit, push, pull, clone, gitignore
* Atsitiktinių dydžių p,d,q,r funkcijos - teoriškai ir praktiškai.
* Mokomes generuoti dydžius pagal savo norus. Funkcija nuo atsitiktinių dydžių - taip pat atsitiktinis dydis! 
* Interaktyvus iššūkis
* R galimybės
* Statistiniai testai (esminis visuotinis principas). 
* Pasiūlymai užsidirbti:
    * Rulete - kai jau pamatai tendencija statyti priešingai. Hmm?
    * Ruletė - duble down strategija
-->

### Priminimas apie GIT

Svarbiausios proceduros: status, add, commit, push, pull, clone, gitignore.
Sukursime RProject ir pademonstruosime kaip dirbama.


### Random variables in R

R aplinkoje yra realiasuota labai daug atsitiktinių dydžių, žr. `?distributions`.
Pastebėkite, kad visi jie naudoja ta pačia pavadinimu schemą. Pirmosios raidės yra
`p`, `d`, `q`, ir `r`, o likusi dalis žymi skirstinio pavadinmą, pvz: `dnorm`, `pnorm`, `qnorm`, `rnorm`.



```r
# pazisiurekime p ir d sarysi: p = \int d
print("Skaiciai turi sutapti:")
integrate(dnorm, -Inf, 1)
pnorm(1)

# p ir q sarysis - tai vienas kitam prie6ingos funkcijos
print("Ar nustebsite, kad atsakymas bus 0.66?")
qnorm(pnorm(0.66))

# generavimas
print("O cia galiausiai generavimo pvz:")
x = rnorm(10000)
summary(x)
```

```
## [1] "Skaiciai turi sutapti:"
## 0.8413448 with absolute error < 1.5e-05
## [1] 0.8413447
## [1] "Ar nustebsite, kad atsakymas bus 0.66?"
## [1] 0.66
## [1] "O cia galiausiai generavimo pvz:"
##      Min.   1st Qu.    Median      Mean   3rd Qu.      Max. 
## -3.684000 -0.677300  0.006035  0.003606  0.668500  4.440000
```

Pasižiurėkime grafini skirstinio vertinimą:


```r
# sugeneruojame dydzius ir padrome grazu grafika palygonti teorija su praktika
x = rnorm(500)

# 1. histograma su branduoliniu tankiu ir palyginimu su teoriniu
hist(x, probability = TRUE)
lines(density(x), col=4, lwd=2)
curve(dnorm, lwd=2, col=2, add=TRUE)
```

![](PE2_files/figure-html/xprob_iliustration-1.png) 

```r
# 2. empyrine pasiskirskirstymo funkcija 
Fn <- ecdf(x)
plot(Fn)
curve(pnorm, -4, 4, add=TRUE, col=2, lwd=2)
```

![](PE2_files/figure-html/xprob_iliustration-2.png) 


### Custom random variables

Labai svarbus akcentas: funkcija nuo atsitiktinių dydžių - taip pat atsitiktinis dydis 
(su savo pasiskirstymo funkcija). p.s. šiame fakte slypi statistikos esmė.

#### Pvz. 1

Tegul $x \sim N(0,1)$ ir $y:= \sqrt{|x|}$. Kaip atrodo $y$ skirstinys? Koks vidurkis? Kam lygi tikimybė, kad $y < 1$? 

```r
# reneruojam x
x = rnorm(10000)

# tada y
y = sqrt(abs(x))

# galiausiai gauname grafika:
hist(y, probability = TRUE)
lines(density(y), col=4, lwd=2)
curve(dnorm(x, mean=mean(y), sd=sd(y)), lwd=2, col=2, add=TRUE)
```

![](PE2_files/figure-html/yFromX1-1.png) 



```r
# kitos galimo isvados: mean, median, table (summary), density ir t.t.
summary(y)

# kokia tikimybe, kad y >1
mean(y>1)

# kokia tikimybe, kad kad y yra intervale [1, 1.5]
mean((1 <= y) & (y <=1.5))

# raskime 70% kvantili, t.y. toki x, kuriam galia lygybe: P(y<x)=0.7
quantile(y, 0.7)
```

```
##    Min. 1st Qu.  Median    Mean 3rd Qu.    Max. 
## 0.01213 0.56780 0.82100 0.82530 1.07400 1.98300 
## [1] 0.3198
## [1] 0.2926
##      70% 
## 1.019593
```



#### Pvz. 2

Du žaidėja ridena kauliukus. Pirmasis žaidėjas meta du klausiukus, o antrasis tris. 
Vertinama išmestų kauliukų suma. Laimi tas žaidėjas, kurio išmestu taškų suma yra didesnė. 
Jeigu iškrenta lygiosios, tai laimi pirmasis žaidėjas. Kokia tikimybė, kad laimės antrasis žaidėjas?


```r
# lets define the function that demonstrate dice roll
rollDice <- function(NDice){
  sum(sample(6, size=NDice, replace = TRUE))
}

# apply this function
rollDice(2) # pirmo zaidejo ekspermentas
rollDice(3) # antro zaidejo
rollDice(2) >= rollDice(3) # zaidimo ekspermentas

# apibrezkime ekspermento funkcija
experment <- function(){
  rollDice(2) >= rollDice(3) 
}

# lets find out the distribution of sum of two dices - abi uzklausos yra ekvivalencios
sim = replicate(10000, rollDice(2) >= rollDice(3))
sim = replicate(10000, experment())

# lets estimate the probability P(dice(3)=<dice(2))
mean(sim)
```

```
## [1] 5
## [1] 12
## [1] FALSE
## [1] 0.2258
```

#### Pvz. 3

Tegul $x_i \sim U(0,1), i={1,...,N}$. Stebėjimų vektorių pažymėkime $X$. 
Kaip atorodo aritmetinio vidurkio skirstinys? Griežtai kalbant mums reikia rasti funkcijos
$$f(X) = \frac{\sum x_i}{N} $$
skirstinį.

Išpradžių išsigrėžkimte, kaip atrodo $U(0,1)$ skirstinys

```r
# tai galima padaryti su specialia vfunkcija: curve(dunif, -1, 2)
# arba patiems realizuotifunkcija
x = seq(-1, 2, by=0.01)
y = dunif(x)
plot(x, y, type='l')
```

![](PE2_files/figure-html/runif1-1.png) 

Paziurekime, kaip atrodo $F(X)$ skirstinys, kai $N=2$. Labai primenta trikampį (ištiesų taip ir turi būti).

```r
sim = replicate(100000, mean(runif(2)))
hist(sim, probability = TRUE)
lines(density(sim), col=4, lwd=2)
curve(dnorm(x, mean=mean(sim), sd=sd(sim)), lwd=2, col=2, add=TRUE)
```

![](PE2_files/figure-html/runif2-1.png) 

Dabar pažiūrėkime, kaip atrodo $F(X)$ skirstinys, kai $N=100$ - turi daug labiau panašėti į normalujį.
Tai užtikrina CRT.

```r
sim = replicate(100000, mean(runif(100)))
hist(sim, probability = TRUE)
lines(density(sim), col=4, lwd=2)
curve(dnorm(x, mean=mean(sim), sd=sd(sim)), lwd=2, col=2, add=TRUE)
```

![](PE2_files/figure-html/runif3-1.png) 

Kaip atrodo funkcijos 
$$ g(X) = \sqrt{N} (\bar{X} - 0.5 )$$
skirstinys? Čia $\bar{X}=f(X)$, t.y. $\bar{X}$ yra aritmetinis vidurkis.
Ar jo priklausomybė nuo $N$ tapo didesnė ar mažesnė?


```r
N = 50
sim = replicate(100000, sqrt(N)*(mean(runif(N))-0.5))
hist(sim, probability = TRUE)
lines(density(sim), col=4, lwd=2)
curve(dnorm(x, mean=mean(sim), sd=sd(sim)), lwd=2, col=2, add=TRUE)
```

![](PE2_files/figure-html/runif4-1.png) 



#### Interaktyvus iššūkis

Reikia sukonstruoti MC modeliavimą, kurio pagalba galėtume įvertinti $\pi$ reikšmę, 
naudojant tik elemntarius veiksmus.

Mastymo vingiai:

1. Visų prima reikia susieti $\pi$ su kažkokių dydžiu, kurį galėtume vertinti.
Tam reikia turėti gerą intuiciją arba žinių arba patirtis. Kaip ten bebūtų viena 
iš geriausiai žinomų tiesioginių sąsajų yra apskritimo plotas, t.y. 
$$S = \pi r^2$$

Kadangi $r$ galime pasirinkti kokį modeliuoti, tai pasirenkame $r=1$ ir gauname, kad $S=\pi$.
Kitaip sakant $\pi$ radimas susiveda į ploto radimo uždavinį.

2. Kaip galime rasti plotą? Žinomo ploto kvadrate tolygiai skleisti atsitiktinius taškus.
Tuomet žiūrėti kiek jų yra apskritimo viduje. Šių taškų proporcija ir padeda iškaičiuoti atsakymą.

![](PE2_files/figure-html/pi1-1.png) 

3. Kaip reikia generuoti dvimačius taškus ir gauti atsakymą? 
Kadangi taškai pagal abi kordinates yra nepriklausomos,
tai generavimas yra labai paprastas - atskirai generuojma $x$ ir atskirai $y$.
O galutinis atsakymas yra apskritimo vidinių taškų proporcija padauginti iš keturkampio ploto. Taigi

```r
N = 100000
x = runif(N, -1, 1)
y = runif(N, -1, 1)
mean(x^2 + y^2 <= 1) * 4
```

```
## [1] 3.14384
```

5. Kaip patikrinti konvergavimą? Galima žiūrėti, kaip keičiasi įvertis vis daugėjant stebėjimų.  



```r
N = 1000
x = runif(N, -1, 1)
y = runif(N, -1, 1)
sim = (x^2 + y^2 <= 1) * 4
cummean = cumsum(sim) / seq_along(sim)
plot(cummean, type="l")
abline(a=pi, b=0, col=3)
```

![](PE2_files/figure-html/pi3, -1.png) 

### R galimybių demonstracija

* Animacija
* Rcmdr ir grafika
* Shiny paketas


### Statistiniai testai

Visi statistiniai testai remiasi tuo pačiu principu.
Reikia turėti tokią funkciją,  kurios skirstinys būtų žinomas, kai galioja nulinė hipotezė.
Jei gauta funkcijos realizacija yra labai mažai tikėtina, tuomet hipotezės galiojimas kelia įtarimų.


```r
?t.test
?prop.test
?cor.test
?var.test

x = rnorm(100, mean=0)
t.test(x)
```

Panagrinėkime `t.test`. Įsitikinkite, kad mokate jį palesiti, suprantete atsakymą ir mokate padaryti išvadas.


```r
N = 100
x = rnorm(N, 0)
y = rnorm(N, 0.0)
t.test(x,y)
```

```
## 
## 	Welch Two Sample t-test
## 
## data:  x and y
## t = 1.5507, df = 196.34, p-value = 0.1226
## alternative hypothesis: true difference in means is not equal to 0
## 95 percent confidence interval:
##  -0.05609641  0.46893428
## sample estimates:
##   mean of x   mean of y 
## -0.02081068 -0.22722961
```

Kaip suprasti p-reiksmę. 
Patikrinikime p-reikšmės prasmė meliaviavimo principu.
Kas yra testo galia? Kaip ją galime paskaičiuoti?
Kokį skirstinį turi p-reikšmę?


## Task 3

Žemiau rasti užduotis. Kiekvienas studentas turi padaryti bent po dvi užduotis.
Jeigu studentas pasirenka daryti iššūkį, tai antros užduoties atlikti nereikia. 
Atliekant užduotis, reikia išnagrinėti pateiktus klausimus. Vien tik teisingas atsakymas netinka - 
reikia pateikti savo argumentus, rezultatus, iliustracijas ir kodo esminius fragmentus. 
Ką ir kokiu detalumu pateikti reikia nuspręsti jums patiems.
Siekiamybė yra pateikti tokią ataskaitą, kad statistikos pagrindus turintis žmogus galėtų
suprasti argumentus ir pasitikėti rezultatais.

Studentai gali laisvai rinktis kokias užduotis atlikti, 
bet labai skatinu studentus tarpusavyje pasiderinti, kad 
būtų atliktos visos užduotys. Išreikšdamas šį skatinimą pasižadu šiuos skatinimus:

* Labai apsimoka daryti užduotį, kurios niekas nenori. Kuo mažiau žmonių daro tą pačią užduotį, 
tuo didesnė tikimybė gauti papildomus taškus. Jeigu būsi vienintelis atlikęs užduotį, 
tai papildomi taškai tampa praktiškai užtikrinti. 

* Apsimoka daryti daugiau negu privalomas minimumas. Jeigu kokybiškai atliksite daugiau nei privaloma, tai
gausite papildomų taškų.

* Jeigu bendrai per visus studentus bus realizuotos visos užduotys, tai visi visuotinai gausite papildomų taškų.

* Jeigu šalia visų užduočių taip pat bus **kokybiškai** realizuoti ir visi iššūkiai, 
tai visuotinai gaunami taškai bus padvigubinti.


Šiai užduočiai sukurite subdirektorija `task3`. Jos viduje kiekvienai pasirinktai užduočiai 
taip pat po direktorija - pagal užduoties pavadinima. 


**Kauliukai.** Pirmasis žaidėjas meta vieną kauliuką ir fiksuojamas atsivertusių taškų skaičius.
Antrasis žaidėjas meta du klausiukus ir fiksuojamas dydis:
$\max(x_1, x_2)-1$,  kur $x_1$ ir $x_2$ žymi pirmojo ir antrojo kauliukų iškritusių akių skaičių.
Jeigu žaidėjų gautų taškų skaičiai yra lygus, tai ekspermentas kartojamas iš naujo 
(ir taip kartojama tol, kol galiausiai nustatomas laimėtojas). Kokia tikimybė laimėti pirmajam žaidėjui?


**Moneta.** Tarkime metama moneta. Jeigu iškrenta herbas, tai laimite $12$ EUR. 
Jeigu skaičius, tai pralošiate $10$ EUR.
Bus žaidžiama $n$ kartų ir gauti rezultatai sumuojami. Kokia tikimybė jums turėti teigiamą
balansą po $n$ kartų? Kokis išlošių pasikliautiniai $95%$ intervalai.
Ištirkite tikimybes su skirtingais $n$, pvz. $n={1,2,5,10,20,100}$.
Kaip atrodo balanso tankis? Kai $n=100$.


**Rulete.** Nagrin4kime standartinę kazino ruletę. 
Kokia tikimybė po $1000$ vienodų statymų ant vienos pasirinktos spalvos, bus teigiamas balansas?
Raskite apytikslę $x$ reikšmę, kuriai galioja nelygybe $P(balansas<x) = 0.25$.


**CRT.** Generuojame $m$ atsitiktinių dydžių turinčių Beta skirstinį su parametrais 
$\alpha=\beta=0.5$ Iš šių atsitiktinių dydžių suskaičiuojamas aritmetinis vidurkis.
Kaip atrodo vidurkio tankis, kai $n=100$? 


**TeorijaVsPraktika.** Ridename $4$ klauliukus. 
Suskaičiuokite jų teorinį skirstini ir patikrinkite jį su empiriniu skirstiniu gautu Monte Carlo metodu.


**Laimikis.** (Įššūkis) Žvejys žvejoja kiekviena darbo dieną. Ir taip jau stabiliai tęsiasi $5$ metus.
Vidutiniškai žmogus pagauna 20 žuvų per dieną. Tarkime, kad žuvų kiekio skirstinį gerai aprašo Poisono 
atsitiktinis dydis. Žuvų dydį gerai nusako normalusis atsitiktinis dydis.
Pagaunamų žuvų dydžio pasikliautinis 90% intervalas yra [180, 750] (gramų). 
Pabandykite įvertinti kokį didžiausią laimikį yra pagavęs žvejys. Koks Jūsų įverčio pasikliautinis intervalas?

**Futbolas.** (Įššūkis) Modeliuokime fotbolo varžymų metu įmašumų įvarčių kiekį. 
Laiko intervalai tarp įvarčių modeliuojami su eksponentiniu skirstiniu 
(eksponentinio skirstinio parametrą pasiūlykite patys). 
Kaip tuomet atrodo įvarčių pasiskirstymas varžybų tėkmėje?
Taip pat pažiūrėkite kokį skirstinį turi varžymų bagties skirstinys. 
Ar tai primena Poisono skirstinį? Ar galite tlikti formalų testą?


**LengvasUzdarbis** (Įššūkis) Kazino ruletės išsami analizė. 
Internete yra daug puslapių siūlančių greitai ir užtikrintai užsidirbti.
Pvz: http://gerasuzdarbis.biz/l1/
Šiame puslapyje pateikta lošimo strategija, kuri anot autoriaus garantuoja išlošimą. 
Jums reikia kaip profesionalui išsiaiškinti strategiją ir patikrinti jos veikimą. Taip pat 
patikrinti ką teigia puslaio autorius ir rasti ką jis nutyli. 


**Trikampis** (Įššūkis) Fraktalo generavimas. 
Kartais atsitiktinumas sugeneruoja labai neatsitiktines struktūras.
Pvz: https://en.wikipedia.org/wiki/Sierpinski_triangle 
Padarykite R gražia aplikaciją, kurioje būtų vizualiai realizuotas
Sierpinskio trikampio generavimas **Chaos game** principu.



Chapter 3. Tiesinė regresija
=====================================================

Literature: the main source is [@Kerns2011a, ch. 11, 12]. 
Alternative source is [@Lavine2013a, ch. 3].

Key qualifications:

* Know and understand the linear model in both representations (in equation and matrix forms)
* Run linear regresion and make proper conclusions form regresion output
* Make sure regresion is correctlly applied
* Know how to apply transformations and dummy variables
* Run custom hipotesis tests
* Understand ANOVA (and t-test) as special case of linear regresion.




<!--
Beveik tvarkinga tiesinė regresija:

Išskirtys, 
Multikolinerumas,
Heteroskedastiskumas.
Interpretacijos atskirimas nuo optimalios prognozes.
overfit problema

Kūribinga dalis:
ištiesinimas
plano matricos specifikavimas

Prezentacija:
Mokėti tiksliai suformuluoti modeli paprasta lygtimi ir matriciniu pavidalu.
Gauta lygti prašyti išreikštiniu pavidalu.
Mokėti teisinga interpretuoti
-->






References
============================================================
---
references:
- id: Kerns2011a
  title: Introduction to Probability and Statistics Using R
  author:
  - family: Kerns
    given: G. Jay
  issued:
    year: 2011

- id: Lavine2013a
  title: Introduction to Statistical Thought
  author:
  - family: Lavine
    given: Michael
  issued:
    year: 2013




- id: fenner2012a
  title: One-click science marketing
  author:
  - family: Fenner
    given: Martin
  container-title: Nature Materials
  volume: 11
  URL: 'http://dx.doi.org/10.1038/nmat3283'
  DOI: 10.1038/nmat3283
  issue: 4
  publisher: Nature Publishing Group
  page: 261-263
  type: article-journal
  issued:
    year: 2012
    month: 3
---


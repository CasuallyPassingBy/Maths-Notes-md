Links: [[Common Taylor Series]], [[Bernoulli numbers]], [[Hyperbolic Trigonometric Identities]], [[Useful Identities]]

### Pythagorean Identities

$$ \cos^2x+\sin^2x=1 $$

$$ 1+\tan^2x=\sec^2x $$

$$ \cot^2x+1=\csc^2x $$

### Sum of Angles

$$ \sin(\alpha \pm \beta) = \sin \alpha \cos \beta \pm \cos \alpha \sin \beta $$

$$ \cos(\alpha \pm \beta) = \cos \alpha \cos \beta \mp \sin \alpha \sin \beta $$

$$ \tan(\alpha \pm \beta) = \frac{\tan \alpha \pm \tan \beta}{1 \mp \tan \alpha \tan \beta} $$

$$ \csc(\alpha \pm \beta) = \frac{\sec \alpha \sec \beta \csc \alpha \csc \beta}{\sec \alpha \csc \beta \pm \csc \alpha \sec \beta} $$

$$ \sec(\alpha \pm \beta) = \frac{\sec \alpha \sec \beta \csc \alpha \csc \beta}{\csc \alpha \csc \beta \mp \sec \alpha \sec \beta} $$

$$ \cot(\alpha \pm \beta) = \frac{\cot \alpha \cot \beta \mp 1}{\cot \beta \pm \cot \alpha} $$

### Double Angle

$$ \sin (2\theta) = 2 \sin \theta \cos \theta = \frac{2\tan(\theta)}{1+\tan^2(\theta)} $$

$$ \cos (2\theta) = \cos^2 \theta - \sin^2 \theta = 2 \cos^2 \theta - 1 = 1 - 2 \sin^2 \theta= \frac{1-\tan^2(\theta)}{1+ \tan^2(\theta)} $$

$$ \tan (2\theta) = \frac{2 \tan \theta} {1 - \tan^2 \theta} $$

$$ \csc (2\theta) = \frac{\sec \theta \csc \theta}{2} $$

$$ \sec (2\theta) = \frac{\sec^2 \theta}{2 - \sec^2 \theta} $$

$$ \cot (2\theta) = \frac{\cot^2 \theta - 1}{2 \cot \theta} $$

### Triple Angle

$$ \sin (3\theta) =3\sin\theta - 4\sin^3\theta = 4\sin\theta\sin\left(\frac{\pi}{3} -\theta\right)\sin\left(\frac{\pi}{3} + \theta\right) $$

$$ \cos (3\theta) = 4 \cos^3\theta - 3 \cos\theta =4\cos\theta\cos\left(\frac{\pi}{3} -\theta\right)\cos\left(\frac{\pi}{3} + \theta\right) $$

$$ \tan (3\theta) = \frac{3 \tan\theta - \tan^3\theta}{1 - 3 \tan^2\theta} = \tan \theta\tan\left(\frac{\pi}{3} - \theta\right)\tan\left(\frac{\pi}{3} + \theta\right) $$

$$ \csc (3\theta) = \frac{\csc^3\theta}{3\csc^2\theta-4} $$

$$ \sec (3\theta) = \frac{\sec^3\theta}{4-3\sec^2\theta} $$

$$ \cot (3\theta) = \frac{3 \cot\theta - \cot^3\theta}{1 - 3 \cot^2\theta} $$

### $n$ Angle

$$ \begin{align*}\sin(n\theta) &= \sum_{k \text{ odd}} (-1)^{\frac{k-1}{2}}{n\choose k}\cos^{n-k}(\theta) \sin^k(\theta) \\ &=2^{n-1}\prod_{k = 0}^{n-1}\sin\left(\frac{k\pi}{n}+\theta\right) \end{align*} $$

$$ \cos(n\theta) = \sum_{k \text{ even}} (-1)^{\frac{k}{2}}{n \choose k}\cos^{n-k}(\theta) \sin^k(\theta) $$

this can be derived from

$$ \cos(n\theta) +i\sin(n\theta) = (\cos(\theta)+i\sin(\theta))^n $$

### Half-angle

$$ \sin \frac{\theta}{2} = \pm \sqrt{\frac{1 - \cos \theta}{2}} $$

$$ \cos \frac{\theta}{2} = \pm \sqrt{\frac{1 + \cos\theta}{2}} $$

$$ \tan \frac{\theta}{2} = \csc \theta - \cot \theta = \pm\, \sqrt\frac{1 - \cos \theta}{1 + \cos \theta} = \frac{\sin \theta}{1 + \cos \theta} $$

$$ = \frac{1 - \cos \theta}{\sin \theta} = \frac{-1 \pm \sqrt{1+\tan^2\theta}}{\tan\theta} = \frac{\tan\theta}{1 + \sec{\theta}} $$

$$ \cot \frac{\theta}{2} = \csc \theta + \cot \theta = \pm\, \sqrt\frac{1 + \cos \theta}{1 - \cos \theta} = \frac{\sin \theta}{1 - \cos \theta} = \frac{1 + \cos \theta}{\sin \theta} $$

### Product/Sum Identities

- Product to Sum
    $$ 2\cos \theta \cos \varphi = {{\cos(\theta - \varphi) + \cos(\theta + \varphi)}} $$
    $$ 2\sin \theta \sin \varphi = {{\cos(\theta - \varphi) - \cos(\theta + \varphi)} } $$
    
    $$ 2\sin \theta \cos \varphi = {{\sin(\theta + \varphi) + \sin(\theta - \varphi)} } $$
    
    $$ 2\cos \theta \sin \varphi = {{\sin(\theta + \varphi) - \sin(\theta - \varphi)} } $$
    
    $$ \tan \theta \tan \varphi =\frac{\cos(\theta-\varphi)-\cos(\theta+\varphi)}{\cos(\theta-\varphi)+\cos(\theta+\varphi)} $$
    
- Sum to Product
    
    $$ \sin \theta \pm \sin \varphi = 2 \sin\left( \frac{\theta \pm \varphi}{2} \right) \cos\left( \frac{\theta \mp \varphi}{2} \right) $$
    
    $$ \cos \theta + \cos \varphi = 2 \cos\left( \frac{\theta + \varphi} {2} \right) \cos\left( \frac{\theta - \varphi}{2} \right) $$
    
    $$ \cos \theta - \cos \varphi = -2\sin\left( \frac{\theta + \varphi}{2}\right) \sin\left(\frac{\theta - \varphi}{2}\right) $$
    
    $$ \tan\theta\pm\tan\varphi=\frac{\sin(\theta\pm \varphi)}{\cos\theta\cos\varphi} $$
    

### Power-reduction
If $n$ is odd

$$ \cos^n(\theta) = \frac{2}{2^n}\sum_{k = 0}^{\frac{n-1}{2}}{n \choose k}\cos((n-2k)\theta) $$

$$ \sin^n(\theta) =\frac{2}{2^n}\sum_{k = 0}^{\frac{n-1}{2}}(-1)^{\left(\frac{n-1}{2}-k\right)}\sin((n-2k)\theta) $$

If $n$ is even

$$ \cos^n(\theta) = \frac{1}{2^n}{n \choose\frac{n}{2}}+\frac{2}{2^n}\sum_{k = 0}^{\frac{n}{2}-1}{n \choose k}\cos((n-2k)\theta) $$

$$ \sin^n(\theta) =\frac{1}{2^n}{n \choose\frac{n}{2}}+\frac{2}{2^n}\sum_{k = 0}^{\frac{n}{2}-1}(-1)^{\left(\frac{n}{2}-k\right)}{n \choose k}\cos((n-2k)\theta) $$

### Lagrange Identities

$$ \sum_{k =0}^n \sin k\theta = \frac{\cos\frac{\theta}{2}-\cos\left((n+\frac{1}{2}\right)\theta)}{2\sin\frac{1}{2}\theta} $$

$$ \sum_{k =0}^n \cos k\theta = \frac{\sin\frac{\theta}{2}+\sin\left((n+\frac{1}{2}\right)\theta)}{2\sin\frac{1}{2}\theta} $$

and the [[Main definitions for Fourier Analysis|Dirichlet kernel]]:

$$ D_n(\theta) =1+2\sum_{k =1}^n \cos k\theta = \frac{\sin((n+\frac{1}{2}) \theta) }{\sin\frac{1}{2}\theta} $$

### Complex Exponential

$$ \sin\theta = \frac{e^{i\theta}-e^{-i\theta}}{2i} $$

$$ \cos\theta= \frac{e^{i\theta}+e^{-i\theta}}{2} $$

$$ \tan \theta = -i\frac{e^{i\theta}-e^{-i\theta}}{e^{i\theta}+e^{-i\theta}} $$

$$ \csc \theta = \frac{2i}{e^{i\theta}-e^{-i\theta}} $$

$$ \sec\theta= \frac{2}{e^{i\theta}+e^{-i\theta}} $$

$$ \cot\theta= i \frac{e^{i\theta}+e^{-i\theta}}{e^{i\theta}-e^{-i\theta}} $$

$$ \operatorname{cis}\theta= e^{i\theta} $$

$$ \arcsin x= -i\ln\left(ix+\sqrt{1-x^2}\right) $$

$$ \arccos x= -i \ln\left(x+\sqrt{x^2-1}\right) $$

$$ \arctan x= \frac{i}{2}\ln\left(\frac{i+x}{i-x}\right) $$

$$ \operatorname{arccsc}x = -i \ln\left(\frac{i}{x}+\sqrt{1-\frac{1}{x^2}}\right) $$

$$ \operatorname{arcsec}x = -i \ln\left(\frac{1}{x}+i\sqrt{1-\frac{1}{x^2}}\right) $$

$$ \operatorname{arccot} x = \frac{i}{2}\ln\left(\frac{x-i}{x+i}\right) $$

$$ \operatorname{arccis} x= -i\ln(x) $$

### Inverse Trig Functions

$$ \newcommand{\arccsc}{\operatorname{arccsc}} \newcommand{\arcsec}{\operatorname{arcsec}} \newcommand{\arccot}{\operatorname{arccot}} \begin{align*} \sin(\arcsin x) &=x & \cos(\arcsin x) &=\sqrt{1-x^2} & \tan(\arcsin x) &=\frac{x}{\sqrt{1 - x^2}} \\ \sin(\arccos x) &=\sqrt{1-x^2} & \cos(\arccos x) &=x & \tan(\arccos x) &=\frac{\sqrt{1 - x^2}}{x} \\ \sin(\arctan x) &=\frac{x}{\sqrt{1+x^2}} & \cos(\arctan x) &=\frac{1}{\sqrt{1+x^2}} & \tan(\arctan x) &=x \\ \sin(\arccsc x) &=\frac{1}{x} & \cos(\arccsc x) &=\frac{\sqrt{x^2 - 1}}{x} & \tan(\arccsc x) &=\frac{1}{\sqrt{x^2 - 1}} \\ \sin(\arcsec x) &=\frac{\sqrt{x^2 - 1}}{x} & \cos(\arcsec x) &=\frac{1}{x} & \tan(\arcsec x) &=\sqrt{x^2 - 1} \\ \sin(\arccot x) &=\frac{1}{\sqrt{1+x^2}} & \cos(\arccot x) &=\frac{x}{\sqrt{1+x^2}} & \tan(\arccot x) &=\frac{1}{x} \\ \end{align*} $$

### Derivatives
$$ \frac{d}{dx} \sin x = \cos x$$
$$ \frac{d}{dx} \cos x = -\sin x$$
$$ \frac{d}{dx} \tan x = \sec^2 x$$
$$ \frac{d}{dx} \csc x = -\csc x\cot x$$
$$ \frac{d}{dx} \sec x = \sec x\tan x$$
$$ \frac{d}{dx} \cot x = -\csc^2  x$$
### Derivatives of Inverse functions
$$ \frac{d}{dx} \sin^{-1} x = \frac{1}{\sqrt{1-x^2}}$$
$$ \frac{d}{dx} \cos^{-1} x = -\frac{1}{\sqrt{1-x^2}}$$
$$ \frac{d}{dx} \tan^{-1} x = \frac{1}{{1+x^2}}$$
$$ \frac{d}{dx} \csc^{-1} x = \frac{1}{x\sqrt{x^2-1}}$$
$$ \frac{d}{dx} \sec^{-1} x = \frac{1}{x\sqrt{x^2-1}}$$
$$ \frac{d}{dx} \csc^{-1} x = -\frac{1}{{x^2+1}}$$
### Integrals
$$\int \sin x\, dx = -\cos x +C$$
$$\int \cos x\, dx = \sin x +C$$
$$\int \tan x\, dx = \ln |\sec x| +C$$
$$\int \csc x\, dx = \ln |\csc x-\cot x| +C$$
$$\int \sec x\, dx = \ln |\sec x-\tan x| +C$$
$$\int \cot x\, dx = \ln |\sin x| +C$$
### Integrals of the Inverse functions

$$\int \sin^{-1}x \, dx = x\sin^{-1}x + \sqrt{1-x^2} + C$$
$$\int \cos^{-1}x \, dx = x\cos^{-1}x - \sqrt{1-x^2} + C$$
$$\int \tan^{-1}x \, dx = x\sin^{-1}x -\frac{1}{2}\ln(1+x^2) + C$$
$$\int \csc^{-1}x \, dx = x\sin^{-1}x + \ln (x+\sqrt{x^2-1}) + C$$
$$\int \sec^{-1}x \, dx = x\sin^{-1}x - \ln (x+\sqrt{x^2-1}) + C$$
$$\int \cot^{-1}x \, dx = x\sin^{-1}x +\frac{1}{2}\ln(1+x^2) + C$$

### Power Reduction Integrals
$$ \int \sin^n x\, dx = \frac{-\cos x \sin^{n-1}x}{n} + \frac{n-1}{n}\int \sin^{n-2}x\, dx $$
$$ \int \cos^n x\, dx = \frac{\sin x \cos^{n-1}x}{n} + \frac{n-1}{n}\int \cos^{n-2}x\, dx $$
$$ \int \tan^n x\, dx = \frac{\tan^{n-1}x}{n-1} - \int \tan^{n-2}x\, dx $$
$$ \int \csc^n x\, dx = \frac{-\cot x \csc^{n-2}x}{n-1} + \frac{n-2}{n-1}\int \csc^{n-2}x\, dx $$
$$ \int \sec^n x\, dx = \frac{\tan x \sec^{n-2}x}{n-1} + \frac{n-2}{n-1}\int \sec^{n-2}x\, dx $$
$$ \int \cot^n x\, dx = \frac{\cot^{n-1}x}{n-1} - \int \cot^{n-2}x\, dx $$


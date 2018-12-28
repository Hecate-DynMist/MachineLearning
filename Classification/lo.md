# Logistic Regression

## Notation

Data Sets $$(x,y),\quad x \in \mathbb R^{n_x},y\in\{0,1\}$$, then $$m$$ training sets: 

$$\{(x^{(1)},y^{(1)}),(x^{(2)},y^{(2)}),...(x^{(m)},y^{(m)})\}$$ , then $$x \in \mathbb R^{n_x\times m},y \in \mathbb R^{1\times m}$$



## Logistic Regression

Given $$x$$, need $$\hat y=P(y=1|x),x \in \mathbb R^{n_x}\quad 0\le \hat y\le 1$$, parameters: $$w \in \mathbb R^{n_x},b \in \mathbb R$$

$$\hat y =\sigma(w^Tx+b), \quad \sigma(z)=1/(1+e^{-z})$$ 

If $$z\approx +\infty,\sigma(z)\approx 1;\quad z\approx -\infty,\sigma(z)\approx 0$$

Let $$\theta_0=b\to\theta^Tx=w^Tx$$



## Cost Function

Given  $$m$$ training sets, need $$\hat y \approx y^{(i)}$$

$$\hat y^{(i)} =\sigma(w^Tx^{(i)}+b), \quad \sigma(z^{(i)})=1/(1+e^{-z^{(i)}})$$

**Loss function:** $$\mathcal L(\hat y,y)=\frac{1}{2}(\hat y-y)^2$$

or $$\mathcal L(\hat y,y)=-(ylog(\hat y + (1-y)log(1-\hat y))$$

If $$y=1: \mathcal L(\hat y,y)=-log\hat y\to \hat y$$ large to ensure $$log \hat y$$ large

If $$y=0: \mathcal L(\hat y,y)=-log(1-\hat y)\to \hat y$$ small to ensure $$log (1-\hat y)$$ large

**Cost Function:**  $$J(w,b)=\frac{1}{m}\sum_{i=1}^{m}\mathcal L(\hat y^{(i)},y^{(i)})=-\frac{1}{m}\sum_{i=1}^{m}(y^{(i)}log(\hat y^{(i)} + (1-y^{(i)})log(1-\hat y^{(i)}))$$























 
<p>ⓒ JMC 2017  </p>

<p>출처 : 확률론, 덕성여대 이상준 교수, A First Course in Probability, Sheldon Ross</p>



<pre class="prettyprint"><code class=" hljs haml"># 마크다운 작성법 (2017.04.25)
-<span class="ruby"> 수식은 <span class="hljs-constant">KaTeX</span>로 작성한다.
</span>-<span class="ruby"> h1 <span class="hljs-symbol">:</span> 강의 제목
</span>-<span class="ruby"> h2 <span class="hljs-symbol">:</span> 영어 원제
</span>-<span class="ruby"> h3 <span class="hljs-symbol">:</span> 한글 질문
</span>-<span class="ruby">  + <span class="hljs-symbol">:</span> 질문에 대한 답변</span></code></pre>

<hr>



<h1 id="3강-combinational-analysis-3-이항정리-다항정리">3강 Combinational Analysis ::: (3) 이항정리, 다항정리</h1>



<h2 id="binomial-theorem">Binomial Theorem</h2>



<h3 id="q-이항정리란-무엇인가">Q. 이항정리란 무엇인가?</h3>

<ul>
<li><p>두 개의 항 <code>(x+y)</code>를 <code>n제곱</code>했을 때, 각 항의 계수는 <code>n choose k</code>의 공식을 따른다.</p></li>
<li><p><img src="https://wikimedia.org/api/rest_v1/media/math/render/svg/729b7b8a083fff37cab47d7ec3fea0428bc875ea" alt="Binomail Theorem" title=""></p></li>
</ul>



<h3 id="q-이항정리는-어떻게-증명하는가">Q. 이항정리는 어떻게 증명하는가?</h3>

<ul>
<li>경우의 수를 셀 때 사용했던 조합을 이용하면 된다.</li>
<li><script type="math/tex" id="MathJax-Element-1">x^k</script> <br>
<ul><li>x를 k번 선택하는 경우의 수</li>
<li>전체 n개 중에 k를 뽑는 경우의 수 : <code>n choose k</code> = <script type="math/tex" id="MathJax-Element-2">\binom nk</script></li></ul></li>
<li><script type="math/tex" id="MathJax-Element-3">x^ky^{n-k}</script> <br>
<ul><li>x를 k번, y를 n-k번 선택하는 경우의 수 = x를 k번 선택하는 경우의 수</li>
<li><code>n choose k</code> = <script type="math/tex" id="MathJax-Element-4">\binom nk</script></li></ul></li>
</ul>



<h3 id="q-2x3y4의-계수를-이항정리를-통해-구하시오">Q. <script type="math/tex" id="MathJax-Element-5">(2x+3y)^4</script>의 계수를 이항정리를 통해 구하시오.</h3>

<ul>
<li><script type="math/tex" id="MathJax-Element-6">(2x+3y)^4 = \binom 44 (2x)^4(3y)^0 + \binom 43 (2x)^3(3y)^1 + \binom 42 (2x)^2(3y)^2 + \binom 41 (2x)^1(3y)^3 + \binom 40 (2x)^0(3y)^4</script></li>
</ul>



<h3 id="q-다음-이항정리-공식이-이해되는가">Q. 다음 이항정리 공식이 이해되는가?</h3>

<ul>
<li><img src="https://wikimedia.org/api/rest_v1/media/math/render/svg/689f5d27fa52a8ff3f89bed50e7d6625d5c35aaa" alt="Binomial Theorem (generalized)" title=""></li>
</ul>



<h3 id="q-n개의-원소를-가진-집합의-부분집합의-개수는-몇-개인가">Q. n개의 원소를 가진 집합의 부분집합의 개수는 몇 개인가?</h3>



<h4 id="solution-1">solution 1</h4>

<ul>
<li>원소 : 1, 2, 3, …., n</li>
<li>각각의 원소가 들어가냐 안 들어가냐를 계산한다.</li>
<li>모든 원소는 2가지 경우 (들어가는 경우 or 들어가지 않는 경우)를 가지고 있다.</li>
<li>2가지 경우가 n개의 원소에 각각 적용되므로 곱의 법칙을 사용한다.</li>
<li><script type="math/tex" id="MathJax-Element-7"> 2 * 2 * 2 ... * 2</script></li>
<li><script type="math/tex" id="MathJax-Element-8"> \therefore 2^n</script></li>
</ul>



<h4 id="solution-2">solution 2</h4>

<ul>
<li>원소가 0개인 경우, 1개인 경우, 2개인 경우, …., n개인 경우를 모두 구해서 더한다.</li>
<li>원소가 0개인 경우 : <script type="math/tex" id="MathJax-Element-9">\binom n0</script></li>
<li>원소가 1개인 경우 : <script type="math/tex" id="MathJax-Element-10">\binom n1</script></li>
<li>원소가 2개인 경우 : <script type="math/tex" id="MathJax-Element-11">\binom n2</script></li>
<li>원소가 n개인 경우 : <script type="math/tex" id="MathJax-Element-12">\binom nn</script></li>
<li>이항정리에 <code>x=1</code>, <code>y=1</code>을 넣으면 다음과 같은 식이 완성된다.</li>
<li><script type="math/tex" id="MathJax-Element-13"> (1+1)^n = \binom n0 + \binom n1 + ... + \binom nn</script></li>
<li><script type="math/tex" id="MathJax-Element-14"> \therefore 2^n</script></li>
</ul>



<h2 id="mutinomial-theorem">Mutinomial Theorem</h2>



<h3 id="q-x-y-2z2의-계수를-구하시오">Q. <script type="math/tex" id="MathJax-Element-15">(x + y + 2z)^2</script>의 계수를 구하시오.</h3>

<p>@@@ resume : 33:25</p>



<pre class="prettyprint"><code class=" hljs avrasm"><span class="hljs-label">https:</span>//youtu<span class="hljs-preprocessor">.be</span>/VksOK9Ja-iA?t=<span class="hljs-number">33</span>m28s</code></pre>

<hr>



<h1 id="2강-combinational-analysis-2-순열-조합">2강 Combinational Analysis ::: (2) 순열, 조합</h1>



<h2 id="permutations">Permutations</h2>



<h3 id="q-순열이란-무엇인가">Q. 순열이란 무엇인가?</h3>

<ul>
<li>순서가 있는 배열을 순열이라 한다.</li>
<li>n개를 순서대로 배열하는 방법의 수 : <code>n!</code></li>
</ul>



<h2 id="repeated-perumations">Repeated Perumations</h2>



<h3 id="q-중복-순열이란-무엇인가">Q. 중복 순열이란 무엇인가?</h3>

<ul>
<li>반복을 가진 순열을 뜻한다.</li>
<li>전체 n개 중에 p개 반복되고 r개 반복되는 순열</li>
</ul>



<h3 id="q-pepper을-배열하는-전체-경우의-수는">Q. PEPPER을 배열하는 전체 경우의 수는?</h3>



<pre class="prettyprint"><code class=" hljs erlang-repl">[답] <span class="hljs-number">6</span><span class="hljs-exclamation_mark">!</span>/(<span class="hljs-number">3</span><span class="hljs-exclamation_mark">!</span>*<span class="hljs-number">2</span><span class="hljs-exclamation_mark">!</span>)

<span class="hljs-variable">PEPPER</span>을 모두 다른 글자로 보면 전체 경우의 수 = <span class="hljs-number">6</span><span class="hljs-exclamation_mark">!</span>

그런데 전체 경우의 수를 셀 때 곱해주었던 <span class="hljs-number">3</span>개의 <span class="hljs-variable">P</span>는 모두 같은 숫자였다.
<span class="hljs-variable">PPP</span>를 배열하는 방법은 몇 가지일까? <span class="hljs-number">1</span>가지 밖에 없다.
그런데 <span class="hljs-variable">PPP</span>를 마치 <span class="hljs-variable">ABC</span>처럼 서로 다른 알파벳으로 간주해서 경우의 수 <span class="hljs-number">3</span><span class="hljs-exclamation_mark">!</span>을 곱해준 것이다.
따라서 곱해준 값을 상쇄해야 하므로 곱해준 값만큼 나눠주면 된다.
전체 경우의 수 <span class="hljs-number">6</span><span class="hljs-exclamation_mark">!</span>에서 <span class="hljs-number">3</span><span class="hljs-exclamation_mark">!</span>을 나눠줘야 한다.

마찬가지로 <span class="hljs-number">2</span>개의 <span class="hljs-variable">E</span> 또한 모두 같은 숫자였다.
곱해준 값을 상쇄해야 하므로 그만큼 나눠줘야 한다.
알파벳 <span class="hljs-number">2</span>개를 순서대로 나열하는 방법은 <span class="hljs-number">2</span><span class="hljs-exclamation_mark">!</span>이다.
따라서 <span class="hljs-number">6</span><span class="hljs-exclamation_mark">!</span>에서 <span class="hljs-number">3</span><span class="hljs-exclamation_mark">!</span>을 나눈 값에 <span class="hljs-number">2</span><span class="hljs-exclamation_mark">!</span>을 더 나눠줘야 한다.

따라서 <span class="hljs-function_or_atom">n</span>개의 순열이 있을 때, 반복되는 횟수가 <span class="hljs-function_or_atom">p</span>, <span class="hljs-function_or_atom">r</span>개 있다면
<span class="hljs-function_or_atom">n</span><span class="hljs-exclamation_mark">!</span>/(<span class="hljs-function_or_atom">p</span><span class="hljs-exclamation_mark">!</span>*<span class="hljs-function_or_atom">r</span><span class="hljs-exclamation_mark">!</span>)로 계산해줘야 한다.</code></pre>



<h3 id="중복-순열은-경우의-수를-어떻게-계산하는가">중복 순열은 경우의 수를 어떻게 계산하는가?</h3>

<ul>
<li><code>n!/(p!*r!)</code></li>
</ul>



<h2 id="combinations">Combinations</h2>



<h3 id="q-조합이란-무엇인가">Q. 조합이란 무엇인가?</h3>

<ul>
<li>순서가 없는 배열을 조합이라고 한다.</li>
</ul>



<h3 id="q-수학식으로-표현된-조합을-영어로-어떻게-읽는가">Q. 수학식으로 표현된 조합을 영어로 어떻게 읽는가?</h3>

<ul>
<li>한국에서는 고등학교 때 조합의 기호를 nCr로 표현했다. 이러한 표현을 안 쓰는 것은 아니지만 교수님 말씀에 따르면 학계에서나 전 세계적으로나 아래와 같이 표현한다고 한다.</li>
</ul>

<p><img src="https://wikimedia.org/api/rest_v1/media/math/render/svg/08bdf0fff474c26293414f9eb01ab4bc73ef941f" alt="n combination c" title=""></p>

<ul>
<li>nCk는 <code>n choose k</code>라고 읽으면 된다.</li>
</ul>

<p><strong>끝.</strong></p>

<hr>



<h1 id="1강-combinational-analysis-1-경우의-수">1강 Combinational Analysis ::: (1) 경우의 수</h1>



<h2 id="counting">Counting</h2>



<h3 id="q-확률을-배우는데-경우의-수부터-시작하는-이유는-무엇인가">Q. 확률을 배우는데 경우의 수부터 시작하는 이유는 무엇인가?</h3>

<ul>
<li>확률을 계산하는 방법은 매우 다양하다.</li>
<li>그 중 가장 쉬운 방법이 경우의 수이다.</li>
<li><p>쉬운 것부터 차근차근 해결하기 위해 경우의 수부터 시작한다.</p></li>
<li><p><strong>전제</strong> : 모든 샘플이 동일한 확률로 발생하면, 경우의 수만 잘 세면 확률을 쉽게 계산할 수 있다.</p></li>
</ul>



<h3 id="q-주사위를-던졌을-때-짝수가-나올-확률은">Q. 주사위를 던졌을 때, 짝수가 나올 확률은?</h3>

<ul>
<li>주사위의 숫자는 <strong>각각 동일한 확률</strong> 로 발생한다.</li>
<li>따라서 경우의 수만 잘 세면 된다.</li>
</ul>



<pre class="prettyprint"><code class=" hljs fix"><span class="hljs-attribute">[답] 1/2

주사위가 나올 수 있는 값은 1, 2, 3, 4, 5, 6이다.
그 중에 짝수는 2, 4, 6이다.
따라서 3/6 </span>=<span class="hljs-string"> 1/2 이다.</span></code></pre>



<h3 id="q-3개의-동전을-던졌을-때-앞면이-1개-뒷면이-2개-나올-확률은">Q. 3개의 동전을 던졌을 때, 앞면이 1개, 뒷면이 2개 나올 확률은?</h3>

<ul>
<li>동전의 앞면, 뒷면은 <strong>각각 동일한 확률</strong> 로 발생한다.</li>
<li>따라서 경우의 수만 잘 세면 된다.</li>
</ul>



<pre class="prettyprint"><code class=" hljs fix"><span class="hljs-attribute">[답] 3/8

전체 경우의 수 </span>=<span class="hljs-string">  2 * 2 * 2 = 8가지
앞면 1개, 뒷면 2개 경우의 수 = 3가지
따라서, 사건의 경우의 수 / 전체 경우의 수 = 3/8</span></code></pre>



<h3 id="q-윷놀이할-때-개가-나올-확률은-도개걸윳모-다섯-사건-중에-하나이므로-15이다-o-x">Q. 윷놀이할 때 개가 나올 확률은, 도개걸윳모 다섯 사건 중에 하나이므로 1/5이다. (o, x)</h3>

<ul>
<li>윷놀이의 패는 <strong>각각 동일하지 않은 확률</strong> 로 발생한다.</li>
<li>따라서 경우의 수로 확률을 계산할 수 없다.</li>
</ul>



<pre class="prettyprint"><code class=" hljs css"><span class="hljs-attr_selector">[답]</span> <span class="hljs-tag">x</span>

윷놀이에서 도개걸윷모가 나올 확률은 각각 다르다.
즉, 샘플이 동일한 확률로 발생하지 않기 때문에 경우의 수로 확률을 계산할 수 없다.</code></pre>



<h2 id="the-basic-principle-of-counting">The Basic Principle of Counting</h2>



<h3 id="경우의-수를-세는-기본적인-규칙은-무엇이-있는가">경우의 수를 세는 기본적인 규칙은 무엇이 있는가?</h3>

<ul>
<li>곱의 법칙</li>
<li>합의 법칙</li>
</ul>



<h3 id="곱의-법칙-시행할-때마다-사건이-모두-발생할-때">곱의 법칙 (시행할 때마다 사건이 모두 발생할 때)</h3>



<pre class="prettyprint"><code class=" hljs fix"><span class="hljs-attribute">첫 번째 실험의 경우의 수 x
두 번째 실험의 경우의 수 y

Q. 두 실험이 연속해서 발생할 때, 발생할 수 있는 전체 경우의 수는?

A. x * y </span>=<span class="hljs-string"> xy

연속해서 발생한다는 것은 두 사건이 한번에 모두 발생한다는 뜻이다.</span></code></pre>



<h3 id="합의-법칙-시행할-때마다-사건이-선택적으로-발생할-때">합의 법칙 (시행할 때마다 사건이 선택적으로 발생할 때)</h3>



<pre class="prettyprint"><code class=" hljs autohotkey">첫 번째 실험의 경우의 수 x
두 번째 실험의 경우의 수 y

Q. 두 실험이 둘 중에 하나만 발생할 때, 발생할 수 있는 전체 경우의 수는?

<span class="hljs-literal">A</span>. x+y</code></pre>



<h3 id="소괄호와-중괄호의-차이">소괄호와 중괄호의 차이</h3>

<ul>
<li>(H, H) : 순서가 중요하다.</li>
<li><p>{H, H} : 순서가 중요하지 않다.</p></li>
<li><p>두 개의 동전이 다를 경우, 소괄호 <code>(H, H)</code>로 표시해야 한다.  </p></li>
<li>두 개의 동전이 같을 경우, 중괄호 <code>{H, H}</code>로 표시해야 한다.</li>
</ul>

<p><strong>끝.</strong></p>

<hr>
